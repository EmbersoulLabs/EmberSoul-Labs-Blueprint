# Product Decision: PD-UI-SPEC001 Business Profile Page

ID: PD-UI-SPEC001

UI Specification: UI-SPEC-001 Business Profile Page

Status: Locked

## Purpose

Records accepted UI decisions for the Business Profile Page.

## User Decisions

### PD-UI-SPEC001-001 Page Mode

Business Profile page uses:

- Single Page
- Card Sections
- Auto Save

### PD-UI-SPEC001-002 Navigation

Navigation path:

```text
Workspace -> Settings -> Business Profile
```

### PD-UI-SPEC001-003 Header

Header includes:

- Business Profile title
- Completion %
- Save Status
- Analyze Business button
- Language Switch

### PD-UI-SPEC001-004 Save Status

Save Status values:

- Saving...
- Saved
- Save Failed

### PD-UI-SPEC001-005 Sections

Business Profile page sections:

1. Business Overview
2. Contact & Location
3. Brand Identity
4. Business Assets
5. Languages
6. Business Hours

### PD-UI-SPEC001-006 Business Assets

Rules:

- Logo upload is separate.
- Business Assets use one Upload Area.
- No AI auto-classification in V1.

### PD-UI-SPEC001-007 AI Analysis

Rules:

- One button: Analyze Business.
- No multiple AI buttons per field.
- AI suggests; user accepts, rejects, or edits.
- AI never auto-overwrites user input.

### PD-UI-SPEC001-008 Required Field UI

Required field UI includes:

- Red *
- Card warning when incomplete
- Completion progress updates
- Generate is not blocked

### PD-UI-SPEC001-009 Onboarding

Rules:

- User can skip onboarding.
- Show notice that incomplete profile may reduce AI quality.

### PD-UI-SPEC001-010 Loading

Rules:

- Skeleton Loading.
- No AI call.
- No spinner-only loading state.

### PD-UI-SPEC001-011 Success

Success state:

- Business Profile Complete

CTA:

- Create Campaign

### PD-UI-SPEC001-012 Error

Error state:

- Save Failed
- Retry
- Never clear user input

### PD-UI-SPEC001-013 Responsive

Responsive rules:

- Desktop: sidebar + vertical cards.
- Mobile: vertical cards.

## Architect Recommendations

No additional architect recommendations are accepted as Product Decisions in this update.

## Status

UI-SPEC-001 Business Profile Page is Locked.
