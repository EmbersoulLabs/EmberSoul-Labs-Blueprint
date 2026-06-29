# UI-SPEC-002 Campaign Workspace

Status: Locked

## Purpose

Defines the Campaign Workspace UI.

This UI specification explains how users create campaigns, upload inputs, generate marketing packages, regenerate outputs, and manage campaign activity.

## Workspace Flow

Workspace mode:

- Hybrid

Rules:

- First campaign uses Create Campaign Wizard.
- Returning users use Campaign Workspace.

Create Flow:

1. Campaign Name
2. Campaign Objective
3. Upload Assets
4. Campaign Brief Optional
5. AI Language Suggestion
6. Generate

## Navigation

Campaign Workspace belongs inside the EmberOS workspace experience.

Expected areas:

- Campaign list
- Create Campaign Wizard
- Campaign Workspace
- Campaign detail tabs

## Workspace Layout

Workspace Tabs:

1. Overview
2. AI Video Studio
3. Marketing Package
4. Activity

The layout should separate Campaign business status from AI generation status.

## Campaign Creation

Campaign creation UI includes:

- Campaign Name
- Campaign Objective
- Upload Assets
- Campaign Brief Optional
- AI Language Suggestion
- Generate Summary

Campaign Objective supports dropdown and custom input.

## Generate

Rules:

- Single sticky Generate button.
- Generate creates complete Marketing Package only.
- Generate Summary is shown before execution.
- No split button for first Generate.

## Regenerate

Regenerate uses a split menu.

Options:

- Regenerate All
- Strategy
- Caption
- CTA
- Hashtags
- Subtitle
- Video
- Marketing Report

Regenerate should preserve completed outputs when possible.

## Workflow Progress

Workflow Progress includes:

- Timeline
- Current Step
- Percentage
- Estimated Remaining Time

Users should understand that the system is working and what stage is currently active.

## Background Generation

Rules:

- User does not need to wait on the page.
- User can continue using EmberOS.
- System notifies user when output is ready.

## Notification

Supported V1 notifications:

- In-App Notification
- Notification Center
- Browser Notification with permission

Future notification channels:

- Email
- WhatsApp
- Mobile Push

## AI Failure

Failure UI should show:

- User-friendly reason
- Retry Section
- Retry All
- Cancel
- Completed outputs remain visible

Normal users should not see raw infrastructure errors.

## AI Queue

Normal Tenant sees simplified running status.

Agency / Super Admin sees:

- Running
- Waiting
- Completed Today
- Estimated Finish

## Marketing Package Cards

Text cards support:

- Copy
- Edit
- Regenerate
- Export
- Mark as Approved reserved

User Edited Version:

- Normal user sees edited version.
- Super Admin can compare AI Original vs User Edited Diff.

Approval:

- Field reserved.
- V1 does not emphasize approval flow.

## Video Studio

Desktop:

- Right drawer

Mobile:

- Dedicated page

Video Studio includes:

- Cover
- Caption
- Subtitle
- Voice
- BGM
- Style
- Target Platform

### Cover

Cover options:

- Auto Select
- Choose Frame
- Upload Cover
- AI Cover Generation future

### Caption

Caption supports:

- Edit
- Rewrite
- Regenerate
- Multi-language

### Subtitle

Subtitle supports:

- Edit
- Regenerate
- Multi-language

### TTS

TTS supports:

- Multiple Voices
- Multiple Languages
- Preview
- Regenerate TTS Only

### BGM

BGM rules:

- BGM Library currently has about 60 tracks.
- User selects category then track.
- Preview is supported.
- Start Offset is supported.
- BGM Volume is supported.
- Original Video Volume is supported.

BGM Categories:

- Happy
- Luxury
- Romantic
- Elegant
- Emotional
- Fast
- Slow
- Trending

### AI Style

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

### Target Platform

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

## Empty States

Empty states should guide the user to the next action.

Examples:

- No campaign selected
- No assets uploaded
- No Marketing Package generated yet
- No activity yet

## Loading

Loading states should show progress where possible.

AI should not be invoked for static loading UI.

## Success

Success state should show that the complete Marketing Package is ready.

User can then:

- Review
- Edit
- Export
- Regenerate

## Error

Errors should be friendly and actionable.

Rules:

- Preserve completed outputs.
- Allow retry by section.
- Allow Retry All.
- Allow Cancel.

## Responsive

Desktop:

- Overview and editing areas may sit beside status or activity panels.
- AI Video Studio opens in a right drawer.

Mobile:

- Single-column flow.
- AI Video Studio uses a dedicated page.
- Sticky actions must not cover editable fields.

## UX Principles

- Generate should feel simple.
- Regenerate should feel controlled.
- AI progress should be visible.
- Users should not be forced to wait on long AI jobs.
- Completed outputs should not disappear after partial failure.

## Dashboard

Campaign dashboard may include:

- Campaign Overview
- Recent Activity
- AI Queue Widget

## Status

UI-SPEC-002 Campaign Workspace is Locked.
