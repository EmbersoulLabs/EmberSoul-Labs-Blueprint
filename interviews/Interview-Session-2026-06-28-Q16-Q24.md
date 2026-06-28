# Interview Session — 2026-06-28 — Q16 to Q24

Repository Policy: Append-only
Related Blueprint: blueprint/Blueprint-v1.2.md

## Q16 — Business Profile Required Fields

Business Profile must collect the minimum context needed for marketing reasoning.

Required fields:

- Company Name
- Industry
- Services
- Region

Reasoning:

Without these fields, AI may produce generic marketing analysis that does not match the actual business.

## Q17 — Brand Voice at Campaign Level

Brand Voice should belong to Campaign configuration.

It should support multi-select.

Reasoning:

The same business may run different campaigns with different tones. A flower business, for example, may use luxury tone for wedding campaigns and friendly tone for daily bouquet campaigns.

## Q18 — Business Profile Low Confidence Flow

AI may infer Business Profile information when context is incomplete.

However, inferred information must be marked as unconfirmed.

If confidence is low, EmberOS must require user confirmation before final use.

Rule:

- AI can guess
- AI must disclose uncertainty
- User must confirm

## Q19 — AI Thinking Order

AI should reason in this order:

1. Video
2. User Description
3. Campaign
4. Business Profile
5. AI Reasoning

Reasoning:

The uploaded video is the strongest immediate evidence. User description clarifies intent. Campaign defines goal. Business Profile gives background. AI reasoning combines the layers after evidence is gathered.

## Q20 — Business Profile and Video Conflict

When Business Profile conflicts with the video, EmberOS should remind the user to confirm.

It should not directly judge that the Business Profile or video is wrong.

Example behavior:

- "The video appears to show Product A, but your Business Profile says the campaign is for Service B. Please confirm which one should be used."

## Q21 — Business Profile and Campaign Fields

Business Profile fields:

- Company Name
- Industry
- Services
- Region

Campaign fields:

- Brand Voice
- Promotion
- Target Audience

Reasoning:

Business Profile should describe the business. Campaign should describe the current marketing push.

## Q22 — Marketing Score Framework

Marketing Score should include:

- Video Quality
- Editing Quality
- Marketing Quality
- Brand Match
- Viewer Perspective

Purpose:

The score should help the user understand why content is strong or weak and what to improve.

## Q23 — Marketing Success Prediction V1

Marketing Success Prediction V1 should predict Marketing Potential.

It must not predict:

- Views
- Likes
- Revenue
- Orders

Reasoning:

Those outcomes depend on external factors such as platform algorithm, audience size, posting time, ad spend, and market demand. EmberOS should not overpromise.

## Q24 — Critical Error Detection

If critical understanding errors appear, EmberOS should recommend regeneration.

Critical cases:

- Product identification is wrong
- Business Profile has serious conflict with content
- Audience is wrong
- Content analysis failed
- Critical Understanding Error is detected

Recommended behavior:

- Explain the issue clearly
- Suggest regeneration
- Ask the user to confirm corrected context before rerunning
