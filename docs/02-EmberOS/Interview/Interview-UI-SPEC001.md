# Interview Record: UI-SPEC-001 Business Profile Page

UI Specification: UI-SPEC-001 Business Profile Page

Status: Locked

## Interview Goal

Record completed UI decisions for the Business Profile Page.

## Completed Topics

### Topic 001: Page Mode

User Decisions:

- Business Profile page is a single page.
- Business Profile page uses card sections.
- Business Profile page uses Auto Save.

### Topic 002: Navigation

User Decision:

```text
Workspace -> Settings -> Business Profile
```

### Topic 003: Header

User Decisions:

Header includes:

- Business Profile title
- Completion %
- Save Status
- Analyze Business button
- Language Switch

### Topic 004: Save Status

User Decisions:

Save Status values:

- Saving...
- Saved
- Save Failed

### Topic 005: Sections

User Decisions:

Business Profile sections:

1. Business Overview
2. Contact & Location
3. Brand Identity
4. Business Assets
5. Languages
6. Business Hours

### Topic 006: Business Assets

User Decisions:

- Logo upload is separate.
- Business Assets use one Upload Area.
- No AI auto-classification in V1.

### Topic 007: AI Analysis

User Decisions:

- One button: Analyze Business.
- No multiple AI buttons per field.
- AI suggests; user accepts, rejects, or edits.
- AI never auto-overwrites user input.

### Topic 008: Required Field UI

User Decisions:

- Red * marks required fields.
- Cards warn when incomplete.
- Completion progress updates.
- Generate is not blocked.

### Topic 009: Onboarding

User Decisions:

- User can skip.
- Show notice that incomplete profile may reduce AI quality.

### Topic 010: Loading

User Decisions:

- Use Skeleton Loading.
- Do not call AI during loading.
- Do not use spinner-only loading state.

### Topic 011: Success

User Decisions:

- Success state is Business Profile Complete.
- CTA is Create Campaign.

### Topic 012: Error

User Decisions:

- Error state is Save Failed.
- Retry is available.
- User input is never cleared.

### Topic 013: Responsive

User Decisions:

- Desktop uses sidebar + vertical cards.
- Mobile uses vertical cards.

## Architect Recommendations

No additional architect recommendations are recorded as accepted Product Decisions in this interview record.

## Interview Summary

UI-SPEC-001 Business Profile Page is completed and Locked.
