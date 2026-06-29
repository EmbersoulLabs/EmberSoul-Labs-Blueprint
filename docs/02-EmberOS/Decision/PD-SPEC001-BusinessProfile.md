# Product Decision: PD-SPEC001 Business Profile

ID: PD-SPEC001

Specification: SPEC-001 Business Profile

Status: Accepted

Version: 1.0

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

Next Specification: SPEC-002 Campaign Schema
