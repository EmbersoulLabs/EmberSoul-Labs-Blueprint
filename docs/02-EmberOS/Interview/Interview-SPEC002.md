# Interview Record: SPEC-002 Campaign Schema

Specification: SPEC-002 Campaign Schema

Status: Locked

## Interview Goal

Record completed Campaign Schema decisions until SPEC-002 can be implemented without guessing.

## Completed Topics

### Topic 001: Campaign Information

User Decisions:

- Campaign Name is required.
- Campaign Objective is required.
- Campaign Description is optional.
- Target Audience Override is optional.

### Topic 002: Campaign Objective

User Decisions:

- Campaign Objective supports Dropdown.
- Campaign Objective supports Custom input.

### Topic 003: Campaign Status

User Decisions:

- Campaign Status values are Draft, Active, Completed, and Archived.
- Campaign Status is business status only.
- AI status belongs to AI Job.

### Topic 004: Campaign Assets

User Decisions:

- Campaign uses one unified Upload / Drag & Drop area.
- Supported inputs are Videos, Images, Documents, and External URL.
- Asset type is recorded internally.
- At least one input source is required before AI Generate.

### Topic 005: Campaign Brief

User Decisions:

- Campaign Brief is optional.
- Campaign Brief is preferred.
- AI prioritizes Campaign Brief when available.

### Topic 006: Campaign Timeline

User Decisions:

- Campaign records Created At, Updated At, First Generated At, Last Generated At, Published At, and Archived At.
- Publishing schedule is not part of SPEC-002.

### Topic 007: Campaign Outputs

User Decisions:

- Campaign stores output references only.
- Large AI output content is not stored directly in Campaign table.

### Topic 008: Campaign Management

User Decisions:

- Campaign supports Tags, Folder, and Favorite.

### Topic 009: Duplicate Campaign

User Decisions:

- Duplicate Campaign is supported.
- AI outputs are not copied.
- Duplicated campaign regenerates new AI output.

### Topic 010: Campaign Language

User Decisions:

- Output Language is required.
- Subtitle Language is required.
- CTA Language is required.
- Hashtag Language is required.
- Current UI Language is used as initial default.
- AI may suggest better language.
- User confirms final language.

### Topic 011: AI Analysis Priority

User Decisions:

AI analysis order:

1. Campaign Name
2. Campaign Objective
3. Campaign Brief
4. Uploaded Assets
5. Business Profile
6. Generate Marketing Plan

### Topic 012: Marketing Package

User Decisions:

- Campaign has one unified Marketing Package.
- Marketing Package includes Strategy, Report, Hook, Caption, CTA, Hashtags, Subtitle, Video Reference, and Marketing Score.
- Marketing Package is stored separately from Campaign.

### Topic 013: Regenerate

User Decisions:

- Regenerate All is supported.
- Regenerate by Strategy, Caption, CTA, Hashtags, Subtitle, Video, and Marketing Report is supported.

### Topic 014: Version Policy

User Decisions:

- Keep Current Version.
- Keep Previous Version.
- Maximum 2 versions.
- Delete older AI outputs permanently.
- Keep audit logs.

### Topic 015: Ownership

User Decisions:

- workspaceId is automatic.
- companyProfileId is automatic.
- createdBy is automatic.
- assignedTo is optional.

### Topic 016: Delete Policy

User Decisions:

- Campaign uses Soft Delete.
- Retention period is 7 days.
- System auto hard deletes after retention.
- deletedAt and deletedBy are recorded.

### Topic 017: Permission

User Decisions:

- Campaign supports Create, Read, Update, Delete, Duplicate, Export, Generate, and Regenerate.
- Actual permission comes from Permission Matrix.

### Topic 018: Database and Audit

User Decisions:

- Database platform is Supabase.
- Campaign includes standard audit fields.

## Architect Recommendations

No additional architect recommendations are recorded as accepted Product Decisions in this interview record.

## Interview Summary

SPEC-002 Campaign Schema is completed and Locked.
