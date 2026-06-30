# FOUNDATION-002 Design System

Status: Locked

## Purpose

Records the accepted Design System Product Decisions for EmberSoul Labs and EmberOS.

Only accepted Product Decisions are listed as Product Decisions.

## Core Design Principles

- AI should adapt to people, not people to AI.
- Software should deliver value before requiring training.
- Users should learn their business, not the software.
- Good design makes the next step obvious.
- Software should guide users, not test them.
- Keep common tasks simple while keeping advanced capabilities available.
- Users own the intent. AI owns the execution.
- Consistency builds trust.

## Product Decisions

### FOUNDATION-002-001 Brand Visual Identity

Brand Canvas:

- Dark Professional Canvas

Brand Gradient:

- Blue -> Cyan -> Gold

Primary Brand Symbol:

- Ember Flame

The Ember Flame is the primary visual identity across all EmberSoul Labs products.

### FOUNDATION-002-002 Color Philosophy

Colors communicate meaning.

Never use colors only for decoration.

Functional colors:

- Primary
- Success
- Warning
- Error
- Neutral

### FOUNDATION-002-003 Motion

Motion style:

- Minimal Motion

Rules:

- Animations only support communication.
- Avoid decorative animations.

### FOUNDATION-002-004 Icons

Icons support text.

Rules:

- Primary navigation must include text labels.
- Avoid icon-only primary navigation.

### FOUNDATION-002-005 One Primary Action Principle

Each page should have only one Primary Action.

Examples:

- Business Profile -> Analyze Business
- Campaign -> Generate
- Video Studio -> Regenerate

### FOUNDATION-002-006 Card First Architecture

Business modules should be separated into reusable Cards.

### FOUNDATION-002-007 Empty State Principle

Every Empty State should explain:

- Why there is no data
- What the next step is
- Provide a CTA

### FOUNDATION-002-008 Screen Orientation Principle

Every screen should answer:

- Where am I?
- What's happening?
- What's next?

### FOUNDATION-002-009 Zero Confusion Principle

Good design makes the next step obvious.

Avoid making users guess.

### FOUNDATION-002-010 Cross-Platform Principle

One Workspace.

Any Device.

Desktop, Tablet and Mobile provide the same product.

Only presentation adapts.

Do not reduce product capability based on device.

Adapt:

- Layout
- Navigation
- Grid
- Drawer
- Typography
- Spacing

Do not change:

- Business Logic
- Workflow
- Features
- Permissions

### FOUNDATION-002-011 Device Independence Principle

People change devices.

Their work should not have to.

### FOUNDATION-002-012 Familiarity Over Creativity

Prefer interactions users already understand.

Do not redesign common interaction patterns without strong justification.

### FOUNDATION-002-013 AI Components

Use one consistent AI visual language.

Rules:

- Use Ember Flame as the AI identity.
- Avoid robot mascots.

### FOUNDATION-002-014 AI Assessment Principle

AI evaluates quality.

AI does not guarantee business outcomes.

Display the following disclaimer whenever AI assessment or scores are shown:

```text
Predictions only.

Actual results depend on market feedback.
```

### FOUNDATION-002-015 AI Suggestions

AI must explain recommendations before asking users to accept changes.

### FOUNDATION-002-016 Feedback Principles

Success:

- Explain what completed.
- Explain the next step.

Error:

- Explain what happened.
- Explain what users can do.
- Do not expose technical errors to normal users.

### FOUNDATION-002-017 Background AI Principle

Background AI jobs must display:

- Progress
- Estimated time
- Notifications

Users may continue working.

### FOUNDATION-002-018 Never Leave Users Wondering

Users should always know:

- Whether the request was received
- What the system is doing
- Whether they need to wait
- What happens next

### FOUNDATION-002-019 Never Lose User Work

Once users submit a task:

- The system should protect it.

If AI services are temporarily unavailable:

- Queue the request.
- Resume automatically once services recover.

Recommended UX copy:

```text
Request Saved

Your request has been queued.

We'll process it automatically once the service is available.

No action required.
```

This UX copy originated as an Architect Recommendation and was later accepted as a Product Decision.

## Architect Recommendations

No additional architect recommendations are recorded as accepted Product Decisions in this foundation record.

## Status

FOUNDATION-002 Design System is Locked.
