# Interview Record: SPEC-001 Business Profile

Interview ID: INT-SPEC001

Specification: SPEC-001 Business Profile

Status: Completed

Result: Accepted

Date: 2026-06-29

## Interview Goal

Complete the Business Profile Specification until Cursor can implement it without guessing.

## Participants

### Founder

Yuki

Role:

- Product Owner
- Business Expert
- Final Decision Maker

### Architect

ChatGPT

Role:

- Product Manager
- System Architect
- Specification Designer

## Interview Topics

### Topic 001: Business Information

Status: Completed

User Decisions:

Business Profile stores:

- Company Name
- Industry
- Services
- Business Description
- Target Audience
- Business Hours

Additional decisions:

- Company Name is editable.
- Industry supports Dropdown and Custom.
- Services support multiple values.
- Business Description may be AI enhanced.
- Target Audience may be AI suggested.
- Business Hours are optional.

### Topic 002: Contact Information

Status: Completed

User Decisions:

Required:

- Business Email
- Business Phone

Optional:

- WhatsApp Business
- Website
- Facebook
- Instagram
- TikTok
- YouTube
- RedNote
- LinkedIn

Social links store full URLs.

### Topic 003: Location

Status: Completed

User Decisions:

Required:

- Country
- Address
- Postal Code

Optional:

- State
- City

Timezone:

- Automatically detected.
- If detection fails, manual selection is allowed.

### Topic 004: Brand Identity

Status: Completed

User Decisions:

- Brand Personality: Optional
- Brand Style: Optional
- Brand Values: Optional
- Brand Keywords: Required

Input:

- Multi-select
- Custom
- Keywords
- Tag Input

Minimum:

- 1 keyword

### Topic 005: Business Assets

Status: Completed

User Decisions:

Business Assets include:

- Logo
- Brand Colors
- Brand Fonts
- Brand Images

All assets are optional.

### Topic 006: Language Architecture

Status: Completed

User Decisions:

Language is separated into:

```text
UI Language -> User Settings
Business Languages -> Business Profile
Campaign Language -> Campaign
```

Three independent responsibilities.

### Topic 007: Validation Rules

Status: Completed

User Decisions:

Campaign creation requires:

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

### Topic 008: AI Usage

Status: Completed

User Decisions:

- Business Profile provides shared context.
- AI Skills read only the fields required for the current task.

### Topic 009: Database

Status: Completed

User Decisions:

Platform:

- Supabase

Audit Fields:

- id
- workspaceId
- createdAt
- updatedAt
- createdBy
- updatedBy
- deletedAt
- version

### Topic 010: Workspace Architecture

Status: Completed

User Decisions:

Normal Tenant:

```text
1 Tenant
-> 1 Workspace
-> 1 Company Profile
```

Agency Tenant:

```text
1 Tenant
-> Multiple Workspaces
-> Each Workspace
-> One Company Profile
```

## Patch v1.1 Implementation Review

Status: Completed

Result: Accepted as specification patch

Purpose:

Complete missing specifications discovered during implementation review.

Patch v1.1 does not redesign Business Profile and does not change accepted Product Decisions.

Accepted clarifications:

- Industry values come from Industry Dictionary and are not hardcoded inside Business Profile.
- Business Hours use structured JSON and remain optional.
- Timezone detection behavior is Browser Timezone, then Country + City, then Manual Selection.
- Business Profile stores only asset references and does not define upload behavior.
- AI enhancement functions are outside SPEC-001.
- Frontend UI behavior is outside SPEC-001.
- Dependencies section clarifies cross-specification relationships.
- Out of Scope section prevents implementation guessing.
- Shared dictionaries are a future repository architecture note only.

## Interview Summary

Completed Topics: 10

Open Topics: 0

Specification Status: Completed

SPEC-001 Status: Locked

Patch v1.1 Status: Locked

Next Stage: SPEC-002 Campaign Schema

Repository Actions:

- Update Specification
- Update Decision Log
- Update Interview
- Update Release Notes

Commit Ready: Yes
