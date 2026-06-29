# EmberSoul Labs Blueprint Release Notes

Version: v1.0.0

Date: 2026-06-29

## Completed

### SPEC-001 Business Profile

Status: Locked

## Added

### Business Information

- Company Name
- Industry
- Services
- Business Description
- Target Audience
- Business Hours

### Contact Information

- Business Email
- Business Phone
- WhatsApp Business
- Website
- Facebook
- Instagram
- TikTok
- YouTube
- RedNote
- LinkedIn

### Location

- Country
- State / Province
- City
- Address
- Postal Code
- Timezone

Timezone supports:

- Auto Detection
- Manual Selection (Fallback)

### Brand Identity

- Brand Personality
- Brand Style
- Brand Values
- Brand Keywords

Supports:

- Multi-select
- Custom Values
- Tag Input

### Business Assets

- Logo
- Brand Colors
- Brand Fonts
- Brand Images

### Language Architecture

Added three independent language layers:

- UI Language
- Business Languages
- Campaign Language

### Validation Rules

Business Profile completion requirements defined.

### AI Usage

- Business Profile is now the shared business context for AI Skills.
- Each AI Skill reads only the fields required for the current task.

### Database

Platform:

- Supabase

Audit Fields added.

### Workspace Architecture

Workspace and Company Profile relationship finalized.

Normal Tenant:

```text
1 Workspace
-> 1 Company Profile
```

Agency Tenant:

```text
Multiple Workspaces
-> One Company Profile per Workspace
```

## Blueprint Updates

Added:

- AP-001 Workspace Architecture
- AP-002 Language Separation
- AP-003 AI Provider Architecture

AP-003 Status:
Future Specification

## Repository

Updated:

- Blueprint
- Specification
- Decision Log
- Interview
- Release Notes

## Next Specification

SPEC-002 Campaign Schema
