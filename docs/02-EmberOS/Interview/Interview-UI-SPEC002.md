# Interview Record: UI-SPEC-002 Campaign Workspace

UI Specification: UI-SPEC-002 Campaign Workspace

Status: Locked

## Interview Goal

Record completed UI decisions for Campaign Workspace.

## Completed Topics

### Topic 001: Workspace Mode

User Decisions:

- Workspace mode is Hybrid.
- First campaign uses Create Campaign Wizard.
- Returning users use Campaign Workspace.

### Topic 002: Create Flow

User Decisions:

Create Flow:

1. Campaign Name
2. Campaign Objective
3. Upload Assets
4. Campaign Brief Optional
5. AI Language Suggestion
6. Generate

### Topic 003: Workspace Tabs

User Decisions:

Workspace Tabs:

1. Overview
2. AI Video Studio
3. Marketing Package
4. Activity

### Topic 004: Generate

User Decisions:

- Single sticky Generate button.
- Generate creates complete Marketing Package only.
- Generate Summary shown before execution.
- No split button for first Generate.

### Topic 005: Regenerate

User Decisions:

- Regenerate uses split menu.
- Regenerate All is supported.
- Regenerate Strategy, Caption, CTA, Hashtags, Subtitle, Video, and Marketing Report is supported.

### Topic 006: Workflow Progress

User Decisions:

Workflow Progress includes:

- Timeline
- Current Step
- Percentage
- Estimated Remaining Time

### Topic 007: Background Generation

User Decisions:

- User does not need to wait.
- User can continue using EmberOS.
- Notify when ready.

### Topic 008: Failure

User Decisions:

- Show user-friendly reason.
- Retry Section.
- Retry All.
- Cancel.
- Keep completed outputs.

### Topic 009: AI Queue

User Decisions:

- Normal Tenant sees simplified running status.
- Agency / Super Admin sees Running, Waiting, Completed Today, and Estimated Finish.

### Topic 010: Marketing Package Cards

User Decisions:

Text cards support:

- Copy
- Edit
- Regenerate
- Export
- Mark as Approved reserved

### Topic 011: User Edited Version

User Decisions:

- Normal user sees edited version.
- Super Admin can compare AI Original vs User Edited Diff.

### Topic 012: Approval

User Decisions:

- Field reserved.
- V1 does not emphasize approval flow.

### Topic 013: Video Studio

User Decisions:

- Desktop uses right drawer.
- Mobile uses dedicated page.
- Includes Cover, Caption, Subtitle, Voice, BGM, Style, and Target Platform.

### Topic 014: Cover

User Decisions:

Cover options:

- Auto Select
- Choose Frame
- Upload Cover
- AI Cover Generation future

### Topic 015: Caption

User Decisions:

Caption supports:

- Edit
- Rewrite
- Regenerate
- Multi-language

### Topic 016: Subtitle

User Decisions:

Subtitle supports:

- Edit
- Regenerate
- Multi-language

### Topic 017: TTS

User Decisions:

TTS supports:

- Multiple Voices
- Multiple Languages
- Preview
- Regenerate TTS Only

### Topic 018: BGM

User Decisions:

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

### Topic 019: AI Style

User Decisions:

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

### Topic 020: Target Platform

User Decisions:

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

### Topic 021: Notifications

User Decisions:

Supported:

- In-App Notification
- Notification Center
- Browser Notification with permission

Future:

- Email
- WhatsApp
- Mobile Push

### Topic 022: Dashboard

User Decisions:

Dashboard includes:

- Campaign Overview
- Recent Activity
- AI Queue Widget

## Architect Recommendations

No additional architect recommendations are recorded as accepted Product Decisions in this interview record.

## Interview Summary

UI-SPEC-002 Campaign Workspace is completed and Locked.
