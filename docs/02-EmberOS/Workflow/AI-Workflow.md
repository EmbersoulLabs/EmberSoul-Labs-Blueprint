# AI-Workflow.md

## Purpose

Define the canonical EmberOS V1 AI runtime flow and reasoning order.

## Runtime Flow

```text
Business Profile
-> Campaign
-> Upload Video
-> User Description
-> Content Analysis
-> Business Strategy
-> Marketing Angle
-> Hook
-> Subtitle
-> Caption
-> Hashtag
-> Marketing Report
-> Marketing Score
-> Marketing Success Prediction
-> AI Confidence
-> AI Self Challenge
-> Export
-> Schedule Posting
```

## AI Brain Thinking Order

```text
Video
-> User Description
-> Campaign
-> Business Profile
-> AI Reasoning
```

## Rules

- Video is the primary object being marketed.
- Business Profile is background context.
- Current Campaign context can override generic Business Profile assumptions.
- If video and Business Profile conflict, ask user to confirm.
- AI must not silently assume critical facts.
- Low confidence requires explanation and confirmation.

## Critical Error Detection

AI should recommend regeneration or stop workflow when:

- Product recognition is wrong.
- Business Profile conflicts severely with video and user has not confirmed.
- Audience is clearly wrong.
- Content Analysis fails.
- Critical Understanding Error occurs.

## Marketing Score Gate

Marketing Score evaluates marketing effectiveness, not AI capability.

Dimensions:

- Video Quality
- Editing Quality
- Marketing Quality
- Brand Match
- Viewer Perspective

If Marketing Score is below 80, AI Self Challenge must run.

## AI Self Challenge Gate

If Marketing Score is below 80:

- Identify weakest parts.
- Re-plan.
- Regenerate weak parts.
- Re-score.

Stop only if:

- Material is too poor.
- Product cannot be identified.
- User input is insufficient.
- AI Confidence is too low.

## Marketing Success Prediction

Prediction measures Marketing Potential only.

Prediction does not guarantee views, likes, revenue, sales, or orders.

The output must include a disclaimer that actual performance depends on platform algorithm, audience, posting time, and external factors.

## AI Confidence

AI must output confidence level based on:

- Product understanding
- Business Profile match
- Campaign match
- Audio / visual clarity
- Context completeness

If AI Confidence is low:

- Explain why.
- Ask for more information.
- Suggest re-upload if needed.

## Version History

- v1.0 - Added in Blueprint v1.3.
- v1.1 - Merged Blueprint v1.2 and v1.3 runtime, reasoning, score, prediction, confidence, and self challenge rules.
