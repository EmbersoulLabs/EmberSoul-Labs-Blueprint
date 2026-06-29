# UI-SPEC-002 Campaign Workspace

## Purpose

Defines the Campaign Workspace UI.

This UI specification describes how users create, review, regenerate, and manage campaign work inside EmberOS.

## Scope

This specification covers:

- Upload Area
- Campaign Form
- Marketing Package
- AI Status
- Language Settings
- Timeline
- Version History
- Regenerate Actions
- Responsive Rules

This specification does not define backend implementation, AI prompts, upload storage, or workflow engine behavior.

## Layout

The Campaign Workspace should be organized around the campaign creation and generation workflow:

- Workspace Header
- Upload Area
- Campaign Form
- Language Settings
- AI Status
- Marketing Package
- Timeline
- Version History
- Regenerate Actions

### Workspace Header

The header should show:

- Campaign title or draft name
- Campaign business status
- Save state
- Primary action

Campaign business status and AI job status must be visually separate.

## Upload Area

The Upload Area supports campaign input materials.

The UI should allow users to provide source materials such as:

- Image
- Video
- Document
- URL
- Text brief

The Upload Area should show:

- Empty state
- Selected files or references
- Upload or processing state, if available
- Unsupported file message
- Remove action

The UI must not define the storage provider or upload API.

## Campaign Form

The Campaign Form should include fields for campaign planning and generation.

Recommended fields:

- Campaign Name
- Campaign Objective
- Campaign Brief
- Product or Service focus
- Target Audience override, if allowed
- Campaign Description
- Tags
- Folder
- Favorite state

Campaign Objective should support predefined options and custom input when allowed by the specification.

## Marketing Package

The Marketing Package area shows generated campaign outputs.

It may include:

- Captions
- Hooks
- CTAs
- Marketing Angles
- Suggested Visual Direction
- Posting Recommendations
- Marketing Report
- Success Prediction

Generated outputs should be grouped by content type.

Users should be able to review generated content without losing campaign form context.

## AI Status

AI Status must be separate from Campaign business status.

AI Status UI may show:

- Idle
- Queued
- Generating
- Completed
- Failed
- Canceled

The UI may also show:

- Started time
- Completed time
- Error message
- Retry action

AI Status must not silently change Campaign business status.

## Language Settings

Language Settings should support the campaign language requirements from SPEC-002.

The UI should include:

- Input Language
- Output Language
- Caption Language
- Report Language

If AI suggests language settings, the UI should let the user accept the suggestion or keep the current value.

User-confirmed language settings become the campaign source of truth.

## Timeline

The Timeline should show important campaign events when available:

- Created
- Updated
- First Generated
- Last Generated
- Published
- Archived

Timeline entries should be readable and ordered by time.

## Version History

Version History should show generated output versions when available.

Each version entry may include:

- Version number
- Generation time
- Generation source
- AI status result
- Restore or view action, if supported

Duplicating a campaign must not automatically copy generated AI outputs unless a future Product Decision allows it.

## Regenerate Actions

Regenerate Actions should allow users to regenerate campaign outputs.

Supported UI actions may include:

- Regenerate full Marketing Package
- Regenerate selected output type
- Retry failed generation

The UI should warn users when regeneration may replace visible generated content or create a new version.

## Validation UI

Validation should be shown close to the related field.

Validation UI should support:

- Missing required campaign input
- Missing campaign objective
- Invalid URL
- Unsupported upload type
- Language setting conflict
- Unsaved changes warning

## Error UI

Error UI should support:

- Upload failure
- Save failure
- Generation failure
- Network or sync failure
- Invalid campaign input

Errors should clearly separate user-fixable input issues from system or AI generation failures.

## Responsive Rules

### Desktop

Desktop layout may use multiple working areas:

- Left or primary area for input and form editing
- Right or secondary area for AI status, timeline, and version history
- Main output area for Marketing Package review

### Tablet

Tablet layout should stack secondary panels below the active workspace section.

### Mobile

Mobile layout should use a single-column flow.

Rules:

- No horizontal scrolling
- Upload Area must remain tappable
- Form fields must remain readable
- AI Status must remain visible during generation
- Marketing Package content should be grouped into collapsible sections when needed
- Regenerate actions must not cover editable fields

## Version History

### v1.0

Initial Campaign Workspace UI specification created.
