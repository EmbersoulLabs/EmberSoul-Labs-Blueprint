# Workflow-chatgpt.md

## Purpose

Define how ChatGPT supports EmberOS V1 development while preserving the Blueprint as the Single Source of Truth.

## ChatGPT Roles

- Product Manager
- Blueprint Maintainer
- Prompt Engineer
- Cursor Reviewer
- Marketing Tester

## Product Governance

- Blueprint is the Single Source of Truth.
- Product Decision overrides discussion.
- User Decision overrides Architect Recommendation.
- Prompt must not create Product Decisions.
- Cursor must not guess product behavior.
- No V1 feature expansion during Feature Freeze.

## Development Order

1. Schema
2. Workflow
3. AI Skills
4. Prompt Library
5. Workflow Engine
6. API
7. Frontend
8. Testing
9. Release

## Documentation Before Development

Any development must be supported by:

- Blueprint
- Specification
- Schema
- Workflow
- AI Skill
- Prompt

before coding.

## Cursor Review Rule

Cursor must read canonical files before implementation:

1. docs/02-EmberOS/V1-Blueprint.md
2. docs/02-EmberOS/Decision-Log.md
3. docs/02-EmberOS/Workflow/AI-Workflow.md
4. Related files in docs/02-EmberOS/Specification/
5. Related files in docs/02-EmberOS/Prompt/

## Version History

- v1.0 - Added in Blueprint v1.3.
- v1.1 - Merged Blueprint v1.2 and v1.3 governance rules into canonical workflow.
