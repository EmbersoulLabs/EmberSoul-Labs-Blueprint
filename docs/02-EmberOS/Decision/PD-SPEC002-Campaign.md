# Product Decision: PD-SPEC002 Campaign

ID: PD-SPEC002

Specification: SPEC-002 Campaign Schema

Status: Locked

## Purpose

Records accepted user decisions for SPEC-002 Campaign Schema.

Only accepted decisions are listed as Product Decisions.

## User Decisions

### PD-SPEC002-001 Campaign Information

Campaign stores:

- Campaign Name
- Campaign Objective
- Campaign Description
- Target Audience Override

Required:

- Campaign Name
- Campaign Objective

Optional:

- Campaign Description
- Target Audience Override

### PD-SPEC002-002 Campaign Objective

Campaign Objective supports:

- Dropdown
- Custom

### PD-SPEC002-003 Campaign Status

Campaign Status values:

- Draft
- Active
- Completed
- Archived

Campaign Status is business status only.

AI status belongs to AI Job.

### PD-SPEC002-004 Campaign Assets

Campaign uses one unified Upload / Drag & Drop area.

Supported assets:

- Videos
- Images
- Documents
- External URL

Rules:

- Asset type is recorded internally.
- At least one input source is required before AI Generate.

### PD-SPEC002-005 Campaign Brief

Campaign Brief is optional but preferred.

AI prioritizes Campaign Brief when available.

### PD-SPEC002-006 Campaign Timeline

Campaign records:

- Created At
- Updated At
- First Generated At
- Last Generated At
- Published At
- Archived At

### PD-SPEC002-007 Campaign Outputs

Campaign stores references only.

Large AI output content is not stored directly in Campaign table.

### PD-SPEC002-008 Campaign Management

Campaign supports:

- Tags
- Folder
- Favorite

### PD-SPEC002-009 Duplicate Campaign

Duplicate Campaign is supported.

Rules:

- AI outputs are not copied.
- Duplicated campaign regenerates new AI output.

### PD-SPEC002-010 Campaign Language

Campaign stores:

- Output Language
- Subtitle Language
- CTA Language
- Hashtag Language

All are required.

Current UI Language is used as initial default.

AI may suggest better language.

User confirms final language.

### PD-SPEC002-011 AI Analysis Priority

AI analysis priority:

1. Campaign Name
2. Campaign Objective
3. Campaign Brief
4. Uploaded Assets
5. Business Profile
6. Generate Marketing Plan

### PD-SPEC002-012 Marketing Package

Campaign has one unified Marketing Package.

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

### PD-SPEC002-013 Regenerate

Campaign supports:

- Regenerate All
- Strategy
- Caption
- CTA
- Hashtags
- Subtitle
- Video
- Marketing Report

### PD-SPEC002-014 Version Policy

Rules:

- Keep Current Version
- Keep Previous Version
- Maximum 2 versions
- Delete older AI outputs permanently
- Keep audit logs

### PD-SPEC002-015 Ownership

Ownership fields:

- workspaceId auto
- companyProfileId auto
- createdBy auto
- assignedTo optional

### PD-SPEC002-016 Delete Policy

Campaign uses Soft Delete.

Rules:

- 7-day retention
- Auto hard delete after retention
- deletedAt
- deletedBy

### PD-SPEC002-017 Permission

Campaign supports:

- Create
- Read
- Update
- Delete
- Duplicate
- Export
- Generate
- Regenerate

Actual permission comes from Permission Matrix.

### PD-SPEC002-018 Database Platform

Database platform:

- Supabase

### PD-SPEC002-019 Audit Fields

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

## Architect Recommendations

No additional architect recommendations are accepted as Product Decisions in this update.

## Status

SPEC-002 Campaign Schema is Locked.
