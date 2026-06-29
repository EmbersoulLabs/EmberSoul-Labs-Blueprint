# UI-SPEC-001 Business Profile Page

Status: Locked

## Purpose

Defines the Business Profile page layout.

This UI specification explains how users view, complete, analyze, and maintain Business Profile information in EmberOS.

## Page Layout

Page Mode:

- Single Page
- Card Sections
- Auto Save

Navigation:

```text
Workspace -> Settings -> Business Profile
```

The page is organized as vertical cards.

Card order:

1. Business Overview
2. Contact & Location
3. Brand Identity
4. Business Assets
5. Languages
6. Business Hours

## Header

Header includes:

- Business Profile title
- Completion percentage
- Save Status
- Analyze Business button
- Language Switch

## Progress

Completion progress should update as users complete required or recommended fields.

Rules:

- Incomplete cards show warning state.
- Optional fields do not block progress entirely.
- Generate is not blocked by incomplete profile.
- Show notice that incomplete profile may reduce AI quality.

## Sections

### Business Overview

Includes:

- Company Name
- Industry
- Services
- Business Description
- Target Audience

### Contact & Location

Includes:

- Website
- Social links
- Country
- City
- Timezone

### Brand Identity

Includes:

- Logo reference
- Brand colors
- Brand style
- Brand voice

### Business Assets

Rules:

- Logo upload is separate.
- Business Assets use one Upload Area.
- No AI auto-classification in V1.

### Languages

Includes business language context and UI language switch placement.

### Business Hours

Includes optional structured business hours.

## Save Experience

Save mode:

- Auto Save

Save Status values:

- Saving...
- Saved
- Save Failed

Rules:

- Never clear user input after save failure.
- Retry should be available after save failure.

## Validation

Required Field UI:

- Red *
- Card warning when incomplete
- Completion progress updates
- Generate is not blocked

Validation should be shown near the relevant field.

## AI Analysis

AI Analysis uses one button:

- Analyze Business

Rules:

- No multiple AI buttons per field.
- AI suggests; user accepts, rejects, or edits.
- AI never auto-overwrites user input.
- AI should not run during loading UI.

## Upload

Business Profile UI may reference upload areas, but upload implementation belongs to the Asset Upload specification.

Rules:

- Logo upload is separate.
- Business Assets use one Upload Area.
- No AI auto-classification in V1.

## Card Behaviour

Cards should support:

- Complete state
- Incomplete warning state
- Save failed state
- Collapsed or expanded state when useful

Cards must not hide validation errors from the user.

## Loading

Loading UI uses Skeleton Loading.

Rules:

- No AI call during loading.
- No spinner-only loading state.

## Empty State

Empty states should guide users without blocking them.

Onboarding rules:

- User can skip.
- Show notice that incomplete profile may reduce AI quality.

## Success State

Success state:

- Business Profile Complete

CTA:

- Create Campaign

## Error State

Error state:

- Save Failed
- Retry
- Never clear user input

Errors should be user-friendly and should not expose raw infrastructure failures to normal users.

## Responsive

Desktop:

- Sidebar + vertical cards

Mobile:

- Vertical cards

Rules:

- No horizontal scrolling.
- Primary actions remain reachable.
- Cards remain readable on small screens.

## Components

Components may include:

- Text input
- Text area
- Dropdown
- Custom input
- Tag input
- Upload area
- Progress indicator
- Card warning indicator
- Save status indicator
- Analyze Business button
- Language switch

## Accessibility

Rules:

- Required fields must not rely on color only.
- Error messages should be readable by assistive technology.
- Buttons must have clear labels.
- Keyboard navigation must remain possible through all cards.

## UX Principles

- Guide users instead of blocking them.
- Keep Business Profile setup low-friction.
- Do not force users to complete optional fields.
- Preserve user input during errors.
- Let AI suggest improvements without overwriting user decisions.

## Status

UI-SPEC-001 Business Profile Page is Locked.
