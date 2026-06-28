# EmberOS Blueprint v1.3

## Update Mode

Append-only.

Do not overwrite existing files.

## Blueprint v1.3 Scope

EmberOS V1 officially enters Product Specification stage.

V1 product feature expansion is frozen.

No new V1 features should be added unless they block launch.

Development must now follow:

1. Schema
2. Workflow
3. AI Skills
4. Prompt Library
5. Workflow Engine
6. API
7. Frontend
8. Testing
9. Release

## Core Principle

EmberOS is not an AI chat application.

EmberOS is an AI Marketing Operating System that orchestrates specialized AI Skills through structured workflow to deliver marketing assets with minimal user input.

## Runtime Architecture

```text
Frontend
  ↓
Workflow Engine
  ↓
AI Skills
  ↓
Prompt Library
  ↓
OpenAI
```

## V1 Feature Freeze

Locked V1 includes:

- Business Profile
- Campaign
- Upload Video
- Content Analysis
- Business Strategy
- Marketing Angle
- Hook
- Subtitle
- Caption
- Hashtag
- Marketing Report
- Marketing Score
- Marketing Success Prediction
- AI Confidence
- AI Self Challenge
- Estimated Time Saved
- Export
- Schedule Posting

No additional V1 features unless required for launch.

## Development Rule

Blueprint and Product Decision are the Single Source of Truth.

Implementation must follow locked decisions before Cursor, frontend, backend, or prompt changes are made.
