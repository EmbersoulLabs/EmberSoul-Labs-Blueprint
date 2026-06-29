# SPEC-001 Business Profile

Status: Locked (Patch)

Version: 1.1

## Purpose

Business Profile stores the long-term business information for a Workspace.

It represents the business identity and provides shared context for all AI Skills.

Business Profile does NOT store Campaign-specific configuration.

Business Profile does NOT store UI preferences.

Business Profile remains a data specification only.

## Scope

- One Workspace owns exactly one Business Profile.
- One Business Profile may be shared by multiple Campaigns.
- Business Profile defines stored business data and cross-specification boundaries.

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

Industry dropdown values shall come from an Industry Dictionary.

Future shared dictionary location:

`Shared/Dictionaries/IndustryDictionary.md`

Rules:

- Business Profile must not hardcode industry values.
- Industry Dictionary supports localization.
- Industry Dictionary supports future expansion.
- Custom industries are supported.
- Business Profile stores Industry ID when selected.
- Business Profile stores Display Name.
- Business Profile stores Custom Value when applicable.

Implementation must not hardcode the industry list inside Business Profile.

### Services

- Supports multiple selections.
- Custom services allowed.

### Business Description

- Editable.
- Business Profile stores the Business Description value.

AI enhancement functions such as Improve Description are NOT part of SPEC-001.

They belong to:

- AI Skills
- Prompt Library
- Workflow

### Target Audience

- Editable.
- Business Profile stores the Target Audience value.

AI enhancement functions such as Suggest Target Audience are NOT part of SPEC-001.

They belong to:

- AI Skills
- Prompt Library
- Workflow

### Business Hours

- Optional.
- Stored as structured JSON.
- Compatible with Supabase JSONB.

Recommended schema:

```json
[
  {
    "day": "Monday",
    "isOpen": true,
    "openTime": "09:00",
    "closeTime": "18:00"
  },
  {
    "day": "Tuesday",
    "isOpen": false
  }
]
```

Purpose:

- Easier validation
- Easier frontend binding
- Easier API
- Compatible with Supabase JSONB

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

- Automatically detected when possible.
- If detection fails, user manually selects Timezone.
- Timezone is stored after confirmation.

Detection priority:

1. Browser Timezone
2. Country + City
3. Manual Selection

Specification defines behavior only.

SPEC-001 does NOT mandate any API implementation.

Implementation technology is left to development.

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
- Business Profile stores only references to Logo, Brand Images, and Brand Fonts.
- Business Profile does NOT define Upload API.
- Business Profile does NOT define Storage Provider.
- Business Profile does NOT define Upload Workflow.

Upload behavior belongs to future specification:

- SPEC-003 Asset Upload

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

Business Profile stores data only.

AI functions are NOT part of SPEC-001.

Examples of AI functions outside SPEC-001:

- Improve Description
- Suggest Target Audience
- Prompt Design
- Workflow Engine execution

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

## Dependencies

### Depends On

- Workspace
- Industry Dictionary

### Referenced By

- Campaign
- Marketing
- AI Skills
- Workflow Engine
- Marketing Report
- Business Strategy
- Subtitle Generation
- Caption Generation
- Translation
- Future AI Router

Purpose:

Clarify cross-specification relationships.

## Future Shared Resources

Shared dictionaries should eventually move to a shared location.

Future repository architecture note:

```text
Shared/
  Dictionaries/
    IndustryDictionary.md
    CountryDictionary.md
    TimezoneDictionary.md
    LanguageDictionary.md
    CampaignObjectiveDictionary.md
    ToneDictionary.md
```

This is a future repository architecture note only.

Do not create these files until explicitly requested or until the shared resource specification is accepted.

## Out of Scope

Business Profile does NOT include:

- Campaign Settings
- Output Language
- Subtitle Language
- CTA Language
- Hashtag Language
- AI Model Selection
- UI Language
- Upload API
- Storage Provider
- Upload Workflow
- Prompt Design
- Workflow Engine
- Frontend UI
- Frontend Layout
- Components
- Responsive Design
- Navigation
- AI Skills

These belong to other Specifications.

Known future specifications:

- SPEC-003 Asset Upload
- UI-SPEC-001 Business Profile Page

Purpose:

Prevent implementation guessing.

## Version History

- v1.0 - SPEC-001 Business Profile locked.
- v1.1 - Patch added Industry Dictionary, structured Business Hours, Timezone detection behavior, Upload dependency clarification, AI enhancement separation, UI dependency clarification, Dependencies, Out of Scope, and Future Shared Resources notes.
