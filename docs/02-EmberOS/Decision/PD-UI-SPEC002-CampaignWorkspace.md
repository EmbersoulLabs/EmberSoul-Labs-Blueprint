# Product Decision: PD-UI-SPEC002 Campaign Workspace

ID: PD-UI-SPEC002

UI Specification: UI-SPEC-002 Campaign Workspace

Status: Locked

## Purpose

Records accepted UI decisions for the Campaign Workspace.

## User Decisions

### PD-UI-SPEC002-001 Workspace Mode

Workspace mode:

- Hybrid

Rules:

- First campaign uses Create Campaign Wizard.
- Returning users use Campaign Workspace.

### PD-UI-SPEC002-002 Create Flow

Create Flow:

1. Campaign Name
2. Campaign Objective
3. Upload Assets
4. Campaign Brief Optional
5. AI Language Suggestion
6. Generate

### PD-UI-SPEC002-003 Workspace Tabs

Workspace Tabs:

1. Overview
2. AI Video Studio
3. Marketing Package
4. Activity

### PD-UI-SPEC002-004 Generate

Rules:

- Single sticky Generate button.
- Generate creates complete Marketing Package only.
- Generate Summary shown before execution.
- No split button for first Generate.

### PD-UI-SPEC002-005 Regenerate

Regenerate uses split menu.

Options:

- Regenerate All
- Strategy
- Caption
- CTA
- Hashtags
- Subtitle
- Video
- Marketing Report

### PD-UI-SPEC002-006 Workflow Progress

Workflow Progress includes:

- Timeline
- Current Step
- Percentage
- Estimated Remaining Time

### PD-UI-SPEC002-007 Background Generation

Rules:

- User does not need to wait.
- User can continue using EmberOS.
- Notify when ready.

### PD-UI-SPEC002-008 Failure

Failure UI includes:

- User-friendly reason
- Retry Section
- Retry All
- Cancel
- Keep completed outputs

### PD-UI-SPEC002-009 AI Queue

Rules:

- Normal Tenant sees simplified running status.
- Agency / Super Admin sees Running, Waiting, Completed Today, and Estimated Finish.

### PD-UI-SPEC002-010 Marketing Package Cards

Text cards support:

- Copy
- Edit
- Regenerate
- Export
- Mark as Approved reserved

### PD-UI-SPEC002-011 User Edited Version

Rules:

- Normal user sees edited version.
- Super Admin can compare AI Original vs User Edited Diff.

### PD-UI-SPEC002-012 Approval

Rules:

- Field reserved.
- V1 does not emphasize approval flow.

### PD-UI-SPEC002-013 Video Studio

Rules:

- Desktop uses right drawer.
- Mobile uses dedicated page.
- Includes Cover, Caption, Subtitle, Voice, BGM, Style, and Target Platform.

### PD-UI-SPEC002-014 Cover

Cover options:

- Auto Select
- Choose Frame
- Upload Cover
- AI Cover Generation future

### PD-UI-SPEC002-015 Caption

Caption supports:

- Edit
- Rewrite
- Regenerate
- Multi-language

### PD-UI-SPEC002-016 Subtitle

Subtitle supports:

- Edit
- Regenerate
- Multi-language

### PD-UI-SPEC002-017 TTS

TTS supports:

- Multiple Voices
- Multiple Languages
- Preview
- Regenerate TTS Only

### PD-UI-SPEC002-018 BGM

Rules:

- BGM Library currently has about 60 tracks.
- Category then track selection.
- Preview.
- Start Offset.
- BGM Volume.
- Original Video Volume.

BGM Categories:

- Happy
- Luxury
- Romantic
- Elegant
- Emotional
- Fast
- Slow
- Trending

### PD-UI-SPEC002-019 AI Style

AI Style options:

- Elegant
- Luxury
- Minimal
- Modern
- Warm
- Professional
- Cinematic
- Fast-paced

AI Style controls:

- Subtitle style
- Animation
- Zoom
- Transition
- Filter
- BGM style

### PD-UI-SPEC002-020 Target Platform

Target Platform options:

- TikTok
- Instagram Reels
- Facebook Reels
- YouTube Shorts
- XiaoHongShu

AI adapts:

- Safe Area
- Subtitle Size
- CTA Position
- Cover Ratio
- Caption Style
- Hashtag Style

### PD-UI-SPEC002-021 Notifications

Supported:

- In-App Notification
- Notification Center
- Browser Notification with permission

Future:

- Email
- WhatsApp
- Mobile Push

### PD-UI-SPEC002-022 Dashboard

Dashboard includes:

- Campaign Overview
- Recent Activity
- AI Queue Widget

## Architect Recommendations

No additional architect recommendations are accepted as Product Decisions in this update.

## Status

UI-SPEC-002 Campaign Workspace is Locked.
