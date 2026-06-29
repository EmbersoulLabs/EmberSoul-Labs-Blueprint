# SPEC-001 Business Profile

Status: Locked

Version: 1.0

## Purpose

Business Profile stores the long-term business information for a Workspace.

It represents the business identity and provides shared context for all AI Skills.

Business Profile does NOT store Campaign-specific configuration.

Business Profile does NOT store UI preferences.

## Scope

- One Workspace owns exactly one Business Profile.
- One Business Profile may be shared by multiple Campaigns.

## Business Information

| Field | Required |
| --- | --- |
| Company Name | Yes |
| Industry | Yes |
| Services | Yes, minimum 1 |
| Business Description | Yes |
| Target Audience | Yes |
| Business Hours | No |

Rules:

### Company Name

- Editable.

### Industry

Input:

- Dropdown
- Custom Value

### Services

- Supports multiple selections.
- Custom services allowed.

### Business Description

- Editable.
- AI may improve the description.

### Target Audience

- Editable.
- AI may suggest audience.

### Business Hours

- Optional.

## Contact Information

| Field | Required |
| --- | --- |
| Business Email | Yes |
| Business Phone | Yes |
| WhatsApp Business | No |
| Website | No |
| Facebook | No |
| Instagram | No |
| TikTok | No |
| YouTube | No |
| RedNote | No |
| LinkedIn | No |

Rules:

- Social links must store complete URLs.
- Example: `https://instagram.com/yourbusiness` instead of `@yourbusiness`.

## Location

| Field | Required |
| --- | --- |
| Country | Yes |
| State / Province | No |
| City | No |
| Address | Yes |
| Postal Code | Yes |
| Timezone | Auto |

Timezone:

- Automatically detected.
- If detection fails, user manually selects Timezone.
- Timezone is stored after confirmation.

## Brand Identity

| Field | Required |
| --- | --- |
| Brand Personality | No |
| Brand Style | No |
| Brand Values | No |
| Brand Keywords | Yes |

Input Type:

| Field | Input |
| --- | --- |
| Brand Personality | Multi Select, Custom |
| Brand Style | Multi Select, Custom |
| Brand Values | Multi Select, Custom |
| Brand Keywords | Tag Input, Custom |

Minimum:

- 1 Keyword

## Business Assets

| Asset | Required |
| --- | --- |
| Logo | No |
| Brand Colors | No |
| Brand Fonts | No |
| Brand Images | No |

Rules:

- Brand Assets represent long-term business resources.
- Campaign uploads are NOT Business Assets.

## Languages

Business Profile stores:

- Supported Languages

Input:

- Multi Select
- Custom

Examples:

- English
- Chinese
- Bahasa Melayu
- Japanese

Rules:

- Business Languages are business capabilities only.
- They do not determine Campaign output.

## Validation Rules

A Business Profile must be completed before creating a Campaign.

Required:

- Company Name
- Industry
- Services
- Business Description
- Target Audience
- Business Email
- Business Phone
- Country
- Address
- Postal Code
- Brand Keywords

Everything else is optional.

## AI Usage

Business Profile provides shared business context.

AI Skills should read only the fields required to complete the current task.

Examples:

### Business Strategy

May use:

- Industry
- Description
- Audience
- Brand Identity

### Translation

May use:

- Supported Languages

### Marketing Analysis

May use:

- Entire Business Profile

## Database Platform

Supabase

## Audit Fields

- id
- workspaceId
- createdAt
- updatedAt
- createdBy
- updatedBy
- deletedAt
- version

## Relationship

```text
Tenant
-> Workspace
-> Business Profile
-> Campaign
```

Rules:

- One Workspace owns one Business Profile.
- Business Profile belongs to exactly one Workspace.
- Campaigns inherit Business Context from Business Profile.

## Out of Scope

Business Profile does NOT include:

- Campaign Settings
- Output Language
- Subtitle Language
- CTA Language
- Hashtag Language
- AI Model Selection
- UI Language

Those belong to other Specifications.

## Dependencies

Depends on:

- Workspace

Referenced by:

- Campaign
- AI Skills
- Workflow Engine
- Marketing Report
- Business Strategy
- Subtitle Generation
- Caption Generation
- Translation
- Future AI Router
