# EmberOS V1 Interview Log

This file records founder answers and product decisions from the V1 discovery interview. Separate Session files remain the detailed historical record when they exist.

## Foundation Interview

Reference:
docs/02-EmberOS/Interview/Interview-FOUNDATION.md

Summary:
Foundation interview completed and locked FOUNDATION-001 Brand System and FOUNDATION-002 Design System.

Key points:
- Company, tagline, brand positioning, brand belief, product philosophy, product naming, module naming, target users, AI visibility, human control, and automation principle were accepted.
- Core Design Principles, brand visual identity, color philosophy, motion, icons, one primary action, card first architecture, empty states, screen orientation, cross-platform behavior, device independence, AI components, AI assessment, feedback, background AI, and Never Lose User Work were accepted.
- Architect Recommendations are not attributed to the user unless explicitly accepted.

## Session 001

Summary:
EmberOS is an AI Marketing Operating System that helps SMEs solve marketing and content creation manpower shortages through AI-powered planning, generation and optimization.

Key points:
- V1 target customers include florists, software companies, pet businesses, car dealers and restaurants.
- Initial markets are Singapore and Malaysia.
- V1 output includes AI marketing videos, platform captions, hashtags, and Marketing Report.

## Session 002

Summary:
First-time user flow and campaign input were defined.

Key points:
- Register -> Business Profile -> Campaign -> Upload Video -> Optional Description -> Generate.
- Required campaign inputs include Campaign Name and Output Language.
- Platform selection should not block V1.
- Marketing Score should be shown after generation.

## Session 003

Summary:
Content Analysis, Marketing Report, and workflow consolidation were clarified.

Key points:
- Content Analysis should understand product, people, emotion, brand, and target customer.
- Marketing Report explains audience, recommendation rationale, and expected business improvement.
- EmberOS centralizes fragmented marketing tasks into one workflow.

## Session 004

Summary:
Campaign objective, low confidence handling, and quality-over-speed rules were locked.

Key points:
- Campaign requires Campaign Name and Expected Outcome / Campaign Objective.
- AI should ask users to supplement information when uncertain.
- Product must show progress, stage, ETA, errors, retry guidance, and support guidance.

## Session 005

Summary:
Video Planning was identified as the most important V1 feature and the value proposition was tied to time savings.

Key points:
- Video Planning / Auto Marketing Video Planning is the feature to keep if only one remains.
- Users value EmberOS when content brings exposure, customers, or viral performance.
- EmberOS should feel like an AI marketing team with a simple workflow.

## Session 006

Reference:
docs/02-EmberOS/Interview/Session-006.md

Summary:
Business Profile required fields, Brand Voice, and Low Confidence Confirmation Flow were accepted.

Key points:
- Business Profile required fields: Company Name, Industry, Services, Region, Target Audience, Brand Voice.
- Brand Voice is campaign-level and multi-select.
- AI may infer but must ask user to confirm when confidence is low or critical facts are missing.

## Session 007

Reference:
docs/02-EmberOS/Interview/Session-007.md

Summary:
AI Brain Thinking Order, Marketing Score Framework, Marketing Success Prediction, and Critical Error Detection were accepted.

Key points:
- Thinking Order: Video -> User Description -> Campaign -> Business Profile -> AI Reasoning.
- Marketing Score evaluates marketing effectiveness, not AI capability.
- Marketing Success Prediction measures marketing potential, not guaranteed performance.
- AI should recommend regeneration or stop workflow when critical understanding errors occur.

## Session 008

Reference:
docs/02-EmberOS/Interview/Session-008.md

Summary:
AI Self Challenge, AI Confidence, Estimated Time Saved, Schema First Development, and Documentation Before Development were accepted.

Key points:
- If Marketing Score is below 80, AI must challenge, improve, and re-score.
- AI Confidence evaluates product understanding, Business Profile match, Campaign match, clarity, and context completeness.
- V1 should show estimated time saved.
- Development follows Schema -> Workflow -> AI Skills -> Prompt Library -> Workflow Engine -> API -> Frontend -> Testing -> Release.
- Documentation must exist before coding.

## Session 009

Reference:
docs/02-EmberOS/Interview/Session-009.md

Summary:
V1 entered Product Specification stage, Feature Freeze was preserved, and Workflow Engine architecture was accepted.

Key points:
- EmberOS is not a ChatGPT-style chat application.
- End-user flow: Upload Video -> Campaign Information -> Generate -> Marketing Report -> Export / Schedule / Regenerate.
- Workflow Engine orchestrates AI Skills, Prompt Library, OpenAI calls, retries, failure handling, and Self Challenge.
- Prompt logic must not live in the frontend.
