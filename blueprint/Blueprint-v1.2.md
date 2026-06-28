# EmberSoul Labs Blueprint v1.2

Date: 2026-06-28
Maintainer: EmberSoul Labs Blueprint Maintainer
Repository Policy: Append-only
Source of Truth: EmberSoul Labs Blueprint Repository

## Version Summary

Blueprint v1.2 adds the product rules for Business Profile, Campaign-level brand voice, AI reasoning order, marketing scoring, critical error detection, and Marketing Success Prediction V1.

This version does not replace previous Blueprint versions. It extends the product knowledge base with new interview findings, product decisions, and prompt library entries.

## Core Product Direction

EmberOS remains an AI Marketing Operating System for small businesses.

The product should not behave like a generic video editor. It should analyze business context, campaign intent, uploaded video content, and user-provided description before generating marketing outputs.

## Business Profile Required Fields

Business Profile must include the minimum fields required for useful AI marketing reasoning:

- Company Name
- Industry
- Services
- Region

These fields are required because marketing analysis needs to understand what the business is, what it sells, who it serves, and where it operates.

## Campaign Required Fields

Campaign configuration should include:

- Brand Voice
- Promotion
- Target Audience

Brand Voice is campaign-level, not only business-level. Different campaigns may require different tones.

## Brand Voice

Brand Voice should support multi-select at campaign level.

Examples:

- Professional
- Friendly
- Luxury
- Warm
- Bold
- Educational
- Emotional
- Urgent
- Minimal

The system should allow a campaign to combine more than one voice when needed.

## Low Confidence Business Profile Flow

AI may infer missing or unclear business information, but inferred information must not be silently treated as confirmed truth.

When confidence is low, EmberOS must require user confirmation before using the inferred Business Profile as final context.

## AI Brain Thinking Order

The AI reasoning order should follow:

1. Video
2. User Description
3. Campaign
4. Business Profile
5. AI Reasoning

This order protects the product from over-relying on static business data when the uploaded video gives more immediate evidence.

## Conflict Between Business Profile and Video

When Business Profile and video content conflict, the system should not directly judge that the user is wrong.

The system should remind the user to confirm the mismatch.

Recommended behavior:

- Show the detected conflict
- Explain why confirmation is needed
- Ask the user to choose which context is correct
- Avoid blaming language

## Marketing Score Framework

Marketing Score should be structured around five dimensions:

1. Video Quality
2. Editing Quality
3. Marketing Quality
4. Brand Match
5. Viewer Perspective

The score should support practical improvement suggestions, not only a number.

## Marketing Success Prediction V1

Marketing Success Prediction V1 predicts Marketing Potential.

It must not claim to predict:

- Views
- Likes
- Revenue
- Orders

The prediction should estimate how strong the content is as marketing material based on available evidence.

## Critical Error Detection

The system should recommend regeneration when critical understanding errors appear.

Critical cases include:

- Product identification is wrong
- Business Profile has serious conflict with the content
- Target audience is wrong
- Content analysis failed
- Critical understanding error is detected

## Linked Records

Interview Session:

- interviews/Interview-Session-2026-06-28-Q16-Q24.md

Decision Log:

- decisions/PD-010-to-PD-016.md

Prompt Library:

- prompts/Business-Profile.md
- prompts/Marketing-Score.md
- prompts/Regeneration.md
