# Interview Record: SPEC-002 Campaign Schema

Specification: SPEC-002 Campaign Schema

Status: In Progress

Update Type: Specification Partial Update

## Interview Goal

Record accepted Campaign Schema decisions until SPEC-002 can be completed without guessing.

## Accepted Decisions So Far

### Topic 001: Campaign Information

User Decisions:

- Campaign stores Campaign Name, Campaign Objective, Campaign Description, and Target Audience Override.
- Campaign Name is required.
- Campaign Objective is required.
- Campaign Description is optional.
- Target Audience Override is optional.
- Campaign Objective supports Dropdown and Custom input.

Campaign Objective examples:

- Brand Awareness
- Lead Generation
- Sales
- Promotion
- Event
- Product Launch
- Seasonal Campaign
- Custom

### Topic 002: Campaign Status vs AI Job Status

User Decisions:

- Campaign Status and AI Job Status must be separated.
- Campaign Status represents business status only.
- AI generation progress does not belong to Campaign Status.
- AI Job will be handled by a future separate specification.

Campaign Status values:

- Draft
- Active
- Completed
- Archived

### Topic 003: Campaign Assets

User Decisions:

- Campaign supports Uploaded Videos, Uploaded Images, Uploaded Documents, and External URL.
- All input sources should be handled through one unified upload box or drag-and-drop area.
- The user should not see four separate upload sections.
- Schema must still record asset type internally.
- At least one input source is required before AI Generate.

### Topic 004: Campaign Brief

User Decisions:

- Campaign Brief is saved.
- Campaign Brief is not required.
- Campaign Brief is preferred.
- AI should prioritize Campaign Brief when it exists.
- If Campaign Brief does not exist, AI should continue using Campaign Name, Campaign Objective, Uploaded Assets, and Business Profile.

### Topic 005: Campaign Timeline

User Decisions:

- Campaign Scheduling is not part of SPEC-002.
- Campaign should record audit timeline fields instead.
- Future publishing schedule should be defined in a separate Publishing Specification.

Timeline fields:

- Created At
- Updated At
- First Generated At
- Last Generated At
- Published At
- Archived At

### Topic 006: Campaign Outputs

User Decisions:

- Campaign should store references to generated outputs.
- Campaign should NOT store full generated output content directly in the Campaign table.

Output references include:

- Generated Videos
- Generated Captions
- Generated Strategies
- Generated Reports

### Topic 007: Campaign Management

User Decisions:

- Campaign supports Tags, Folder, and Favorite.
- Purpose is to allow users to manage larger numbers of Campaigns in the future.

### Topic 008: Duplicate Campaign

User Decisions:

- Duplicate Campaign is supported.
- Duplicate may preserve Campaign Objective, Campaign Description, Target Audience Override, Campaign Brief, Assets, and Tags.
- Campaign Name may be automatically suffixed with "Copy".
- AI Outputs must not be copied.
- Duplicated Campaign must generate fresh AI Outputs.

### Topic 009: Campaign Language

User Decisions:

- Campaign stores Output Language, Subtitle Language, CTA Language, and Hashtag Language.
- All four language fields are required.
- AI suggests language based on Campaign and Assets.
- User may modify the suggested language.
- Current UI Language may be used as the initial default.

Language Suggestion Priority:

1. Current UI Language is used as the initial default.
2. AI analyzes Campaign Name, Campaign Objective, Campaign Brief, Uploaded Assets, and Business Profile.
3. If AI detects a better language, it should suggest switching.
4. User decides whether to accept AI suggestion or keep current language.

### Topic 010: AI Analysis Priority

User Decisions:

AI analysis should follow this priority:

1. Campaign Name
2. Campaign Objective
3. Campaign Brief
4. Uploaded Assets
5. Business Profile
6. Generate Marketing Plan

AI must not generate marketing plans from a single data point.

If one layer is missing, continue with the next available layer.

### Topic 011: Super Admin AI Execution Console

User Decisions:

- Super Admin should have access to an AI Execution Console.
- This is not visible to normal users.
- It should not expose raw private chain-of-thought.
- It may expose execution traces and summaries.

Preferred name:

- AI Execution Console

Not:

- AI Thinking Console

Reason:

The system should expose execution traces and summaries, not depend on hidden model reasoning.

### Topic 012: Blueprint Design Principle

User Decision:

Use sensible defaults, then let AI recommend improvements instead of asking users to configure everything upfront.

This principle applies to:

- Campaign Language
- Future subtitle style
- Future CTA
- Future hashtags
- Future posting time

## Interview Summary

Status: In Progress

SPEC-002 is not locked.
