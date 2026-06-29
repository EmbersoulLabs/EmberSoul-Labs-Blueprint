# UI-SPEC-001 Business Profile Page

## Purpose

Defines the Business Profile page layout.

This UI specification describes how users review and maintain Business Profile data in EmberOS.

## Scope

This specification covers:

- Layout
- Components
- Validation UI
- Error UI
- Responsive Rules

This specification does not redefine Business Profile data rules. Data rules remain in SPEC-001 Business Profile.

## Layout

The Business Profile page should be organized into clear editing sections:

- Page Header
- Profile Completion Summary
- Business Information
- Services
- Brand Identity
- Business Assets
- Social Links
- Business Hours
- Languages and Region
- Save Actions

### Page Header

The header should show:

- Page title
- Business profile status
- Last updated time, if available
- Primary save action

### Profile Completion Summary

The summary should show whether important profile sections are complete, incomplete, or optional.

The summary must not block the user from saving optional fields.

### Business Information

This section includes:

- Company Name
- Industry
- Region
- Business Description
- Target Audience

### Services

This section includes:

- Service List editor
- Service Description field

The UI should make the Service List visually primary.

The Description field is supporting context.

### Brand Identity

This section includes:

- Logo reference
- Brand color detection result
- Workspace Default Theme fallback indicator

The UI should not define upload behavior.

### Business Assets

This section includes references to:

- Logo
- Brand Images
- Brand Fonts

Upload workflow belongs to SPEC-003 Asset Upload.

### Social Links

This section includes optional fields for:

- Website
- Facebook
- Instagram
- TikTok
- LinkedIn
- YouTube
- Xiaohongshu
- WhatsApp Business

### Business Hours

Business Hours should be shown as structured weekly entries.

Each day should support:

- Open or Closed state
- Open Time
- Close Time

Business Hours remain optional.

### Languages and Region

This section should support:

- Country
- City
- Timezone
- Workspace language context, if available

Timezone UI should follow SPEC-001 detection behavior:

1. Browser Timezone
2. Country + City
3. Manual Selection

## Components

The page may use the following component types:

- Text input
- Text area
- Dropdown
- Custom value input
- Service list editor
- Weekly hours editor
- Link input
- Timezone selector
- Asset reference selector
- Section status indicator
- Save button
- Cancel or discard button

## Validation UI

Validation should be shown close to the related field.

Validation UI should support:

- Required field message
- Invalid URL message
- Invalid time range message
- Duplicate service warning
- Unsaved changes warning
- Company Name change warning

Optional fields should be clearly marked as optional.

Company Name changes should warn the user that future AI outputs may be affected and existing campaigns are not regenerated automatically.

## Error UI

Error UI should support:

- Save failure
- Network or sync failure
- Validation failure
- Asset reference unavailable
- Timezone detection unavailable

Errors should explain what the user can do next.

Errors should not imply that optional fields are required.

## Responsive Rules

### Desktop

Desktop layout may use two columns when space allows:

- Main editing sections
- Completion summary and status panel

Primary actions should remain visible near the top or bottom of the editing flow.

### Tablet

Tablet layout should collapse secondary panels below the active editing section.

### Mobile

Mobile layout should use a single-column flow.

Rules:

- No horizontal scrolling
- Fields must remain readable
- Buttons must remain tappable
- Section status should not cover form content
- Save actions may become a bottom action bar

## Version History

### v1.0

Initial Business Profile UI specification created.
