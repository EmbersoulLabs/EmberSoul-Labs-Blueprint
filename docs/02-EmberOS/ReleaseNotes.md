# EmberSoul Labs Blueprint Release Notes

Version: v1.0.0

Date: 2026-06-29

## Completed

### SPEC-001 Business Profile

Status: Locked

### SPEC-002 Campaign Schema

Status: Locked

Completed:

- Campaign Information
- Campaign Objective
- Campaign Status
- Campaign Assets
- Campaign Brief
- Campaign Timeline
- Campaign Outputs
- Campaign Management
- Duplicate Campaign
- Campaign Language
- AI Analysis Priority
- Marketing Package
- Regenerate
- Version Policy
- Ownership
- Delete Policy
- Permission
- Database Platform
- Audit Fields
- Relationships
- Dependencies
- Out of Scope

### UI-SPEC-001 Business Profile Page

Status: Locked

Completed:

- Purpose
- Page Layout
- Header
- Progress
- Sections
- Save Experience
- Validation
- AI Analysis
- Upload
- Card Behaviour
- Loading
- Empty State
- Success State
- Error State
- Responsive
- Components
- Accessibility
- UX Principles

### UI-SPEC-002 Campaign Workspace

Status: Locked

Completed:

- Purpose
- Workspace Flow
- Navigation
- Workspace Layout
- Campaign Creation
- Generate
- Regenerate
- Workflow Progress
- Background Generation
- Notification
- AI Failure
- AI Queue
- Marketing Package Cards
- Video Studio
- Empty States
- Loading
- Success
- Error
- Responsive
- UX Principles

## Added Principles

- UI Specification Rule
- AI Cost Control Principle
- Background AI Work Principle
- User-Friendly Failure Principle
- Progressive Guidance Principle

## Added Decision Logs

- PD-SPEC002 Campaign
- PD-UI-SPEC001 Business Profile Page
- PD-UI-SPEC002 Campaign Workspace

## Added Interview Records

- Interview-SPEC002
- Interview-UI-SPEC001
- Interview-UI-SPEC002

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
- UI Specification Rule
- AI Cost Control Principle
- Background AI Work Principle
- User-Friendly Failure Principle
- Progressive Guidance Principle

AP-003 Status:
Future Specification

## Repository

Updated:

- Blueprint
- Specification
- Decision Log
- Interview
- UI Specifications
- Release Notes

## Patch

### SPEC-001 Patch v1.1

Status: Locked (Patch)

Completed:

- Industry Dictionary definition
- Business Hours schema
- Timezone detection behavior
- Upload dependency clarification
- AI enhancement separation
- UI dependency clarification
- Dependencies section
- Out of Scope section

## Next Specification

SPEC-003 Asset Upload
