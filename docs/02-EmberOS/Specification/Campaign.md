# SPEC-002 Campaign Schema

Status: Locked

Update Type: Specification + UI Specification Update

## Purpose

Defines the Campaign data specification for EmberOS V1.

SPEC-002 describes the accepted Campaign fields, relationships, lifecycle rules, output references, language rules, ownership rules, delete policy, and out-of-scope boundaries.

## Scope

This specification covers:

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
- Future Specifications

## Campaign Information

Campaign stores the following fields:

| Field | Required | Notes |
| --- | --- | --- |
| Campaign Name | Yes | Primary campaign display name. |
| Campaign Objective | Yes | Defines expected marketing outcome. |
| Campaign Description | No | Supporting context. |
| Target Audience Override | No | Campaign-specific override of Business Profile target audience. |

## Campaign Objective

Campaign Objective supports:

- Dropdown
- Custom

Implementation must support predefined objective values and user-entered custom objectives.

## Campaign Status

Campaign Status represents business status only.

Accepted values:

- Draft
- Active
- Completed
- Archived

Campaign Status must not be used for AI generation progress.

AI generation progress belongs to AI Job or a future AI execution specification.

## Campaign Assets

Campaign supports one unified Upload / Drag & Drop area.

Supported input sources:

- Videos
- Images
- Documents
- External URL

Rules:

- User sees one unified upload area.
- The system internally records asset type.
- At least one input source is required before AI Generate.
- Upload API and storage behavior are out of scope for SPEC-002.

## Campaign Brief

Campaign Brief is optional but preferred.

Rules:

- AI prioritizes Campaign Brief when available.
- If Campaign Brief is missing, AI continues using Campaign Name, Campaign Objective, Uploaded Assets, and Business Profile.

## Campaign Timeline

Campaign records audit timeline fields:

- Created At
- Updated At
- First Generated At
- Last Generated At
- Published At
- Archived At

Publishing schedule is not part of SPEC-002.

## Campaign Outputs

Campaign stores references only.

Campaign must not store large AI output content directly in the Campaign table.

Output references may include:

- Generated Videos
- Generated Captions
- Generated Strategies
- Generated Reports
- Marketing Package reference

## Campaign Management

Campaign supports:

- Tags
- Folder
- Favorite

Purpose:

Help users manage larger numbers of campaigns over time.

## Duplicate Campaign

Duplicate Campaign is supported.

Rules:

- Campaign settings may be copied.
- AI outputs are not copied.
- Duplicated campaign regenerates new AI output.
- Campaign Name may be suffixed with Copy.

## Campaign Language

Campaign stores the following language fields:

- Output Language
- Subtitle Language
- CTA Language
- Hashtag Language

All four language fields are required.

Rules:

- Current UI Language is used as the initial default.
- AI may suggest a better language based on Campaign and Assets.
- User confirms the final language.
- User-confirmed language becomes the source of truth.

## AI Analysis Priority

AI analysis should follow this order:

1. Campaign Name
2. Campaign Objective
3. Campaign Brief
4. Uploaded Assets
5. Business Profile
6. Generate Marketing Plan

Rules:

- AI must not generate marketing plans from a single data point.
- If one layer is missing, continue with the next available layer.

## Marketing Package

Each Campaign has one unified Marketing Package.

Marketing Package contains:

- Strategy
- Report
- Hook
- Caption
- CTA
- Hashtags
- Subtitle
- Video Reference
- Marketing Score

Marketing Package is stored separately from Campaign.

Campaign stores a reference to the Marketing Package.

## Regenerate

Campaign supports regeneration by output type.

Accepted regenerate actions:

- Regenerate All
- Strategy
- Caption
- CTA
- Hashtags
- Subtitle
- Video
- Marketing Report

## Version Policy

Accepted rules:

- Keep Current Version
- Keep Previous Version
- Maximum 2 versions
- Delete older AI outputs permanently
- Keep audit logs

## Ownership

Ownership fields:

- workspaceId auto
- companyProfileId auto
- createdBy auto
- assignedTo optional

## Delete Policy

Campaign uses Soft Delete.

Rules:

- 7-day retention
- Auto hard delete after retention
- Store deletedAt
- Store deletedBy

## Permission

Campaign supports these actions:

- Create
- Read
- Update
- Delete
- Duplicate
- Export
- Generate
- Regenerate

Actual permission rules come from the Permission Matrix.

Permission Matrix is out of scope for SPEC-002.

## Database Platform

Database platform:

- Supabase

## Audit Fields

Campaign includes:

- id
- workspaceId
- companyProfileId
- createdAt
- updatedAt
- createdBy
- updatedBy
- deletedAt
- deletedBy
- version

## Relationships

Campaign belongs to:

- Workspace
- Company Profile

Campaign references:

- Campaign Assets
- Marketing Package
- AI Outputs
- Audit Logs

## Dependencies

Depends On:

- Workspace
- Business Profile
- Asset Upload future specification
- Permission Matrix future specification

Referenced By:

- Campaign Workspace UI
- Marketing Package
- AI Skills
- Workflow Engine
- Reporting

## Out of Scope

SPEC-002 does not define:

- Upload API
- Workflow Engine
- AI Router
- Prompt Design
- Video Rendering
- Publishing Schedule
- Billing
- Notification
- Analytics Dashboard
- Permission Matrix
- Frontend UI

## Future Specifications

Future specifications may include:

- SPEC-003 Asset Upload
- SPEC-004 Marketing Package
- SPEC-005 AI Job
- SPEC-006 Publishing Schedule
- SPEC-007 Notification
- SPEC-008 Analytics Dashboard
- SPEC-009 Permission Matrix
- SPEC-010 Workflow Engine
- UI-SPEC-002 Campaign Workspace

## Status

SPEC-002 Campaign Schema is Locked.
