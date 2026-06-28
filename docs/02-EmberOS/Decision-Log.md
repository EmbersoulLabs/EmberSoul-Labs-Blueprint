# EmberOS V1 Decision Log

This file is the canonical index and summary of locked Product Decisions. Individual PD files remain the detailed historical record when they exist.

## PD-001: Product Positioning

Status: Locked

Decision:
EmberOS is an AI Marketing Operating System.

It is not a video editor, ChatGPT replacement, CapCut replacement or Canva replacement.

## PD-002: Target Customer

Status: Locked

Decision:
V1 targets SMEs in Singapore and Malaysia, starting with industries such as florists, software companies, pet businesses, car dealers and restaurants.

## PD-003: Core Value

Status: Locked

Decision:
The core value is not AI generation itself. The core value is saving SME owners time by completing the marketing workflow from one uploaded video.

## PD-004: First-Time Flow

Status: Locked

Decision:
Register -> Business Profile -> Campaign -> Upload Video -> Optional Description -> Generate

## PD-005: Campaign Input

Status: Locked

Decision:
Required:

- Campaign Name
- Campaign Objective / Expected Outcome
- Output Language

Optional:

- Description

Platform selection should not block V1.

## PD-006: AI Workflow

Status: Locked

Decision:
Business Profile -> Campaign -> Content Analysis -> Marketing Objective -> Marketing Angle -> Hook -> Subtitle -> Caption -> CTA -> Marketing Report

## PD-007: Low Confidence Handling

Status: Locked

Decision:
If AI lacks confidence, it must ask users to supplement key information instead of guessing silently.

## PD-008: Quality Over Speed

Status: Locked

Decision:
V1 prioritizes output quality over speed. Generation must show progress, stage, ETA, error handling, retry guidance and support guidance.

## PD-009: V1 Scope Control

Status: Locked

Decision:
Only items that affect EmberOS V1 launch can enter V1 development. Future ideas go into Roadmap or Parking Lot.

## PD-010: Business Profile Required Fields

Status: Locked

Decision:
Business Profile required fields are Company Name, Industry, Services, Region, Target Audience, and Brand Voice.

## PD-011: Brand Voice

Status: Locked

Decision:
Brand Voice is a campaign-level multi-select setting.

## PD-012: Low Confidence Confirmation Flow

Status: Locked

Decision:
AI may infer, but must ask user to confirm when key context is missing or confidence is low. AI must not silently assume critical facts.

## PD-013: AI Brain Thinking Order

Status: Locked

Decision:
AI Thinking Order is Video -> User Description -> Campaign -> Business Profile -> AI Reasoning.

Rules:
- Video is the primary object being marketed.
- Business Profile is background context.
- If video and Business Profile conflict, ask user to confirm.
- Current Campaign context can override generic Business Profile assumptions.

## PD-014: Marketing Score Framework

Status: Locked

Decision:
Marketing Score evaluates marketing effectiveness, not AI capability.

Dimensions:
- Video Quality
- Editing Quality
- Marketing Quality
- Brand Match
- Viewer Perspective

## PD-015: Critical Error Detection

Status: Locked

Decision:
AI should recommend regeneration or stop workflow when product recognition is wrong, Business Profile conflicts severely with video and user has not confirmed, audience is clearly wrong, Content Analysis fails, or Critical Understanding Error occurs.

## PD-016: Marketing Success Prediction

Status: Locked

Decision:
Marketing Success Prediction is included in V1 and measures Marketing Potential. It does not guarantee views, likes, revenue, sales, or orders.

## PD-017: AI Self Challenge

Status: Locked

Decision:
If Marketing Score is below 80, AI must challenge its own output, re-plan, regenerate weak parts, and re-score.

Stop only if material is too poor, product cannot be identified, user input is insufficient, or AI Confidence is too low.

## PD-018: AI Confidence

Status: Locked

Decision:
AI must output confidence level for product understanding, Business Profile match, Campaign match, audio / visual clarity, and context completeness.

If confidence is low, AI must explain why, ask for more information, and suggest re-upload if needed.

## PD-019: Estimated Time Saved

Status: Locked

Decision:
V1 should show estimated time saved to remind users that EmberOS sells time and workflow automation, not AI tools.

## PD-020: Schema First Development

Status: Locked

Decision:
Development order is Schema -> Workflow -> AI Skills -> Prompt Library -> Workflow Engine -> API -> Frontend -> Testing -> Release.

## PD-021: Documentation Before Development

Status: Locked

Decision:
Any development must be supported by Blueprint, Specification, Schema, Workflow, AI Skill, and Prompt before coding.

## PD-022: EmberOS Is Not a Chat Application

Status: Locked

Decision:
End-user UI must not be ChatGPT-style chat.

User flow:
Upload Video -> Campaign Information -> Generate -> Marketing Report -> Export / Schedule / Regenerate

Reason:
SME users do not want to learn prompting. They want an automatic AI Marketing Team.

## PD-023: Workflow Engine Architecture

Status: Locked

Decision:
Architecture is Frontend -> Workflow Engine -> AI Skills -> Prompt Library -> OpenAI.

Rules:
- Frontend must not contain prompt logic.
- Workflow Engine controls execution order.
- Workflow Engine controls retry.
- Workflow Engine controls failure handling.
- Workflow Engine controls Self Challenge.
- AI Skills must remain modular.
- Prompt Library must be version controlled.

## PD-024: V1 Specification-First Development

Status: Locked

Decision:
EmberOS V1 has entered Product Specification stage. Feature expansion is frozen. No new V1 features unless required to unblock launch.
