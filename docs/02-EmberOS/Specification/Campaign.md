# SPEC-002 Campaign Schema

Status: In Progress

Update Type: Specification Partial Update

## Scope

This document records the accepted SPEC-002 Campaign Schema decisions so far.

SPEC-002 is not locked.

Do not implement code from this draft until SPEC-002 is completed and locked.

## 1. Campaign Information

Campaign stores the following fields:

| Field | Save | Required |
| --- | --- | --- |
| Campaign Name | Yes | Yes |
| Campaign Objective | Yes | Yes |
| Campaign Description | Yes | No |
| Target Audience Override | Yes | No |

Campaign Objective input type:

- Dropdown
- Custom

Campaign Objective examples:

- Brand Awareness
- Lead Generation
- Sales
- Promotion
- Event
- Product Launch
- Seasonal Campaign
- Custom

## 2. Campaign Status vs AI Job Status

Campaign Status and AI Job Status must be separated.

Campaign Status represents business status only.

Campaign Status values:

- Draft
- Active
- Completed
- Archived

AI generation progress does not belong to Campaign Status.

AI Job will be handled by a future separate specification.

AI Job may include:

- Job Status
- Progress %
- Started At
- Finished At
- Error Message

## 3. Campaign Assets

Campaign supports input sources:

- Uploaded Videos
- Uploaded Images
- Uploaded Documents
- External URL

UI Rule:

- All input sources should be handled through one unified upload box or drag-and-drop area.
- The user should not see four separate upload sections.
- Schema must still record asset type internally.

Validation Rule:

At least one input source is required before AI Generate.

Input source may be:

- Video
- Image
- Document
- External URL

## 4. Campaign Brief

Campaign Brief is saved.

Required:
No

Preferred:
Yes

Rules:

- AI should prioritize Campaign Brief when it exists.
- If Campaign Brief does not exist, AI should continue using Campaign Name, Campaign Objective, Uploaded Assets, and Business Profile.

## 5. Campaign Timeline

Campaign Scheduling is not part of SPEC-002.

Campaign should record audit timeline fields instead.

Campaign Timeline fields:

- Created At
- Updated At
- First Generated At
- Last Generated At
- Published At
- Archived At

Future publishing schedule should be defined in a separate Publishing Specification.

## 6. Campaign Outputs

Campaign should store references to generated outputs.

Campaign should NOT store full generated output content directly in the Campaign table.

Output references include:

- Generated Videos
- Generated Captions
- Generated Strategies
- Generated Reports

## 7. Campaign Management

Campaign supports:

- Tags
- Folder
- Favorite

Purpose:

Allow users to manage larger numbers of Campaigns in the future.

## 8. Duplicate Campaign

Duplicate Campaign is supported.

Duplicate may preserve:

- Campaign Objective
- Campaign Description
- Target Audience Override
- Campaign Brief
- Assets (optional)
- Tags (optional)

Campaign Name may be automatically suffixed with "Copy".

AI Outputs must not be copied.

Duplicated Campaign must generate fresh AI Outputs.

## 9. Campaign Language

Campaign stores language configuration:

| Field | Required |
| --- | --- |
| Output Language | Yes |
| Subtitle Language | Yes |
| CTA Language | Yes |
| Hashtag Language | Yes |

Language selection behavior:

- AI suggests language based on Campaign and Assets.
- User may modify the suggested language.
- Current UI Language may be used as the initial default.

Language Suggestion Priority:

1. Current UI Language is used as the initial default.
2. AI analyzes Campaign Name, Campaign Objective, Campaign Brief, Uploaded Assets, and Business Profile.
3. If AI detects a better language, it should suggest switching.
4. User decides whether to accept AI suggestion or keep current language.

Example:

If UI Language is English, default campaign language is English.

If uploaded video is mostly Chinese, AI may suggest Chinese.

User can choose:

- Accept
- Keep Current

## 10. AI Analysis Priority

AI must not generate marketing plans from a single data point.

AI analysis should follow this priority:

1. Campaign Name
2. Campaign Objective
3. Campaign Brief
4. Uploaded Assets
5. Business Profile
6. Generate Marketing Plan

If one layer is missing, continue with the next available layer.

## 11. Super Admin AI Execution Console

Future/admin-only requirement:

Super Admin should have access to an AI Execution Console.

Purpose:

Allow Super Admin to inspect AI execution traces and improve prompts, workflow, and product quality.

Rules:

- This is not visible to normal users.
- It should not expose raw private chain-of-thought.
- It may expose execution traces and summaries.

It may expose:

- AI Inputs
- Input Summary
- Detected Industry
- Target Audience
- Tone of Voice
- Marketing Angle
- Missing Information
- Confidence Score
- Workflow Step Trace
- Intermediate Outputs
- Final Outputs
- Error Messages

Future fields may include:

- Cost
- Tokens
- Duration
- Provider
- Retry Count

Preferred name:

- AI Execution Console

Not:

- AI Thinking Console

Reason:

The system should expose execution traces and summaries, not depend on hidden model reasoning.

## 12. Blueprint Design Principle

Use sensible defaults, then let AI recommend improvements instead of asking users to configure everything upfront.

This principle applies to:

- Campaign Language
- Future subtitle style
- Future CTA
- Future hashtags
- Future posting time

## Status

SPEC-002 remains In Progress.
