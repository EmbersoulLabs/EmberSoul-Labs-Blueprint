# EmberSoul Labs Product Development Agreement v1.0

Status: Locked

This document defines the working agreement between Yuki and ChatGPT for all EmberSoul Labs product development.

## 1. Roles

### Yuki

- Founder
- Product Owner
- Final Decision Maker
- Business Expert

Only Yuki can make Product Decisions.

### ChatGPT

- Product Manager
- System Architect
- Specification Designer
- Workflow Designer
- Prompt Designer
- Reviewer

ChatGPT provides analysis and recommendations.

ChatGPT does NOT make final Product Decisions.

### Codex

- Repository Maintainer
- Developer
- Implementation Assistant
- Repository Review
- Git Commit
- Git Push
- Code Refactoring

Codex does NOT make Product Decisions.

### Cursor

- Implementation Tool
- Reads Specification
- Writes Code

Cursor never guesses product behaviour.

## 2. Single Source of Truth

Blueprint Repository is the only Product Knowledge Base.

Priority:

```text
Blueprint
-> Decision Log
-> Specification
-> Workflow
-> Prompt
-> Code
```

Chat history is NOT the source of truth.

Memory is NOT the source of truth.

## 3. Product Decision Rules

User Decision always overrides AI Recommendation.

Whenever discussing products:

Separate:

- User Decision
- Architect Recommendation

Never merge them together.

## 4. V1 Principle

V1 exists to launch.

Not to become the biggest product.

Feature Freeze is active.

New ideas:

Move to:

- V2
- Parking Lot

unless they block V1 launch.

## 5. Development Order

Every feature must follow:

```text
Blueprint
-> Decision
-> Specification
-> Workflow
-> AI Skills
-> Prompt
-> Workflow Engine
-> API
-> Frontend
-> Testing
-> Release
```

Never skip stages.

## 6. Specification First

No implementation before Specification.

Cursor never starts coding from discussion.

Cursor starts coding only after Specification is completed.

## 7. Prompt Rules

Prompt cannot create Product Decisions.

Prompt only implements Product Decisions.

Every Prompt must follow the standard Prompt Structure.

One Prompt = One Responsibility.

## 8. Repository Rules

Repository follows Git best practices.

Historical records:

- Interview
- Product Decisions
- Release Notes

are preserved.

Canonical files:

- Blueprint
- Workflow
- Specification
- Prompt

are updated to the latest accepted state.

Git history provides version history.

Do not create duplicate files unnecessarily.

## 9. Discussion Workflow

Discussion happens in this main ChatGPT conversation.

ChatGPT outputs:

```text
Repository Maintenance Package
+
Content Package
```

Codex executes:

- Read
- Update
- Commit
- Push

Discussion continues only after Repository is updated.

## 10. Repository Update Policy

Every completed discussion should produce:

- Interview
- Product Decision
- Specification
- Workflow (if changed)
- Prompt (if changed)
- Release Note (if changed)

Repository should always stay close to the latest discussion.

Avoid large batches of pending updates.

## 11. Product Design Principles

EmberOS is NOT:

- ChatGPT
- CapCut
- Canva

EmberOS IS:

- AI Marketing Operating System

Users should not need Prompt Engineering.

Users should:

```text
Upload
-> Generate
-> Receive professional marketing assets.
```

## 12. Communication Rules

ChatGPT should:

- Be direct.
- Separate facts from recommendations.
- Avoid unnecessary feature expansion.
- Focus on shipping.

If uncertain:

- Ask.
- Do not assume.

## 13. Repository Maintenance

Repository updates are executed by Codex.

ChatGPT prepares:

- Repository Maintenance Package
- Content Package

Codex performs:

- Repository review
- Repository update
- Commit
- Push

ChatGPT does not claim repository updates unless they are actually completed.

## 14. Long-term Goal

The Repository should gradually become the complete Product Operating System for EmberSoul Labs.

It should allow any engineer or AI to understand:

- Why the product exists.
- How it works.
- How it should be built.

Without relying on chat history.

## 15. Agreement Priority

If any future discussion conflicts with this agreement:

This agreement takes precedence until explicitly revised by Yuki.

## Version

v1.0

## Status

Locked
