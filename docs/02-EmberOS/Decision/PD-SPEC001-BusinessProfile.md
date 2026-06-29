# Product Decision: PD-SPEC001 Business Profile

ID: PD-SPEC001

Specification: SPEC-001 Business Profile

Status: Accepted

Version: 1.1 Patch

Date: 2026-06-29

## Purpose

This document records the product decisions made during the Business Profile interview.

It explains why decisions were made.

This document is historical.

Specification remains the canonical implementation document.

## Decision 001: Business Profile Responsibility

Business Profile stores long-term business information.

It does NOT store:

- Campaign configuration
- UI preferences
- AI Provider settings

Reason:
Separate permanent business data from temporary campaign data.

## Decision 002: Contact Information

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

Reason:
Only Email and Phone are essential for business identity.

Other channels may be added later.

## Decision 003: Location

Required:

- Country
- Address
- Postal Code

Optional:

- State / Province
- City

Timezone:

- Automatically detected.
- If detection fails, allow manual selection.

Reason:
Timezone supports:

- Scheduling
- Holiday recommendation
- AI Marketing timing

## Decision 004: Brand Identity

Optional:

- Brand Personality
- Brand Style
- Brand Values

Required:

- Brand Keywords

Input Method:

- Multi-select
- Custom
- Tag Input

Reason:
Brand Keywords provide the minimum information required for AI understanding.

## Decision 005: Business Assets

Assets include:

- Logo
- Brand Colors
- Brand Fonts
- Brand Images

All assets are optional.

Reason:
Business Assets improve AI quality but should not block first-time onboarding.

## Decision 006: Language Architecture

Language responsibilities are separated into three layers.

```text
UI Language -> User Settings
Business Languages -> Business Profile
Campaign Language -> Campaign
```

Reason:

- Avoid overlapping responsibilities.
- Each layer has a single responsibility.

## Decision 007: Business Profile Completion

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

Reason:
These fields provide sufficient business context for AI.

## Decision 008: AI Usage

Business Profile serves as shared business context.

Each AI Skill reads only the fields required for its task.

Reason:

- Reduce unnecessary token usage.
- Improve maintainability.
- Support future AI Router implementation.

## Decision 009: Database Platform

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

Reason:

- Provide traceability.
- Support optimistic locking.
- Support soft delete.

## Decision 010: Workspace Relationship

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

Reason:
Workspace is the isolation boundary.

Business Profile belongs to exactly one Workspace.

This architecture simplifies:

- Security
- Billing
- AI Context
- Assets
- Campaign ownership

## Patch v1.1 Clarifications

These clarifications complete missing specification details discovered during implementation review.

They do NOT redesign Business Profile and do NOT change accepted Product Decisions.

### Patch 001: Industry Dictionary

Business Profile shall not hardcode industry values.

Industry input remains:

- Dropdown
- Custom

Dropdown values shall come from Industry Dictionary.

Future shared dictionary location:

- `Shared/Dictionaries/IndustryDictionary.md`

Business Profile stores:

- Industry ID when selected
- Display Name
- Custom Value if applicable

Rules:

- Supports localization.
- Supports future expansion.
- Supports custom industries.

### Patch 002: Business Hours Schema

Business Hours shall use structured JSON.

Business Hours remains optional.

Purpose:

- Easier validation
- Easier frontend binding
- Easier API
- Compatible with Supabase JSONB

### Patch 003: Timezone Detection

Timezone detection priority:

1. Browser Timezone
2. Country + City
3. Manual Selection

Specification defines behavior only.

Implementation technology is left to development.

### Patch 004: Upload Dependency

Business Profile stores only references to:

- Logo
- Brand Images
- Brand Fonts

Business Profile does NOT define:

- Upload API
- Storage Provider
- Upload Workflow

These belong to future specification:

- SPEC-003 Asset Upload

### Patch 005: AI Enhancement

Business Profile stores:

- Business Description
- Target Audience

AI functions are NOT part of SPEC-001:

- Improve Description
- Suggest Target Audience

They belong to:

- AI Skills
- Prompt Library
- Workflow

### Patch 006: UI Dependency

Business Profile does NOT define:

- Frontend Layout
- Components
- Responsive Design
- Navigation

These belong to future UI specification:

- UI-SPEC-001 Business Profile Page

### Patch 007: Dependencies Section

SPEC-001 now explicitly defines:

Depends On:

- Workspace
- Industry Dictionary

Referenced By:

- Campaign
- Marketing
- AI Skills

Purpose:

Clarify cross-specification relationships.

### Patch 008: Out of Scope Section

SPEC-001 now explicitly excludes:

- Upload API
- Prompt Design
- Workflow Engine
- Frontend UI
- AI Skills

Purpose:

Prevent implementation guessing.

## Future Shared Resources Note

Shared dictionaries should eventually move to a shared location:

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

No shared dictionary files are created by this patch.

## Future Decisions

Deferred:

- AI Router
- Provider Registry
- Cost Manager
- Retry Engine
- Metrics

Reason:
Belongs to SPEC-010 Workflow Engine.

## Interview Summary

Status: Completed

Result: Accepted

Specification: SPEC-001 Locked

Patch: v1.1 Locked

Next Specification: SPEC-002 Campaign Schema
