# EmberOS V1 Blueprint

## Current State

EmberOS V1 is in Product Specification stage.

V1 Feature Freeze is active. No new V1 features should be added unless required to unblock launch.

Blueprint v1.2 and v1.3 have been merged into this canonical V1 Blueprint. Historical blueprint, interview, decision, and release files remain as archive.

## Product Positioning

EmberOS is an AI Marketing Operating System for SMEs.

It is not:

- A video editor
- A ChatGPT replacement
- A CapCut replacement
- A Canva replacement
- A ChatGPT-style chat application

EmberOS acts as an automatic AI Marketing Team for Small Businesses.

## Core Problem

SME owners often handle sales, customer service, purchasing, inventory, delivery, admin work and operations.

They may know marketing matters, but they usually do not have time to plan campaigns, edit videos, write captions, generate hashtags or analyse marketing performance.

## Core Value

Users are not paying for AI tools.

They are paying to save time and turn that time into business growth.

One Upload. Complete Marketing Workflow.

V1 should show estimated time saved to remind users that EmberOS sells time and workflow automation, not AI tools.

## Target Customers

V1 target industries:

- Florists
- Software companies
- Pet businesses
- Car dealers
- Restaurants

Business size:

- SMEs

Initial markets:

- Singapore
- Malaysia

Long-term market:

- Global expansion

## End-User Flow

EmberOS must not use a ChatGPT-style prompt-first UI.

User flow:

```text
Upload Video
-> Campaign Information
-> Generate
-> Marketing Report
-> Export / Schedule / Regenerate
```

First-time setup flow:

```text
Register
-> Create Business Profile
-> Create Campaign
-> Upload Video
-> Optional Description
-> Generate
```

Reason:

SME users do not want to learn prompting. They want an automatic AI Marketing Team.

## Business Profile Rules

Required fields:

- Company Name
- Industry
- Services
- Region
- Target Audience
- Brand Voice

Brand Voice:

- Campaign-level setting
- Multi-select

Low Confidence Confirmation Flow:

- AI may infer.
- AI must ask user to confirm.
- AI must not silently assume critical facts.

## V1 Campaign Input

Required:

- Campaign Name
- Campaign Objective / Expected Outcome
- Output Language

Optional:

- Description

Platform selection is hidden in V1 because EmberOS generates assets for supported platforms by default.

Current Campaign context can override generic Business Profile assumptions.

## V1 Output

- AI marketing videos
- Platform captions
- Hashtags
- Marketing Report
- Marketing Score
- Marketing Success Prediction
- AI Confidence
- AI Self Challenge result when required
- Estimated Time Saved

## AI Brain Thinking Order

```text
Video
-> User Description
-> Campaign
-> Business Profile
-> AI Reasoning
```

Rules:

- Video is the primary object being marketed.
- Business Profile is background context.
- If video and Business Profile conflict, ask user to confirm.
- Current Campaign context can override generic Business Profile assumptions.

## AI Runtime Workflow

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

## Content Analysis

Content Analysis must understand:

- Product
- People
- Brand
- Target customer of the product
- Emotional tone

Content Analysis does not generate marketing content directly.

## Marketing Report

The report must answer three questions:

1. Who is the audience?
2. Why is this marketing plan recommended?
3. What business impact is expected?

## Marketing Score Framework

Marketing Score evaluates marketing effectiveness, not AI capability.

Dimensions:

- Video Quality
- Editing Quality
- Marketing Quality
- Brand Match
- Viewer Perspective

## Marketing Success Prediction

Marketing Success Prediction is included in V1.

Prediction measures:

- Marketing Potential

Prediction does not guarantee:

- Views
- Likes
- Revenue
- Sales
- Orders

The prediction must include a disclaimer that actual performance depends on platform algorithm, audience, posting time, and external factors.

## Critical Error Detection

AI should recommend regeneration or stop workflow when:

- Product recognition is wrong.
- Business Profile conflicts severely with video and user has not confirmed.
- Audience is clearly wrong.
- Content Analysis fails.
- Critical Understanding Error occurs.

## AI Confidence

AI must output confidence level based on how certain it is about:

- Product understanding
- Business Profile match
- Campaign match
- Audio / visual clarity
- Context completeness

If AI Confidence is low:

- Explain why.
- Ask for more information.
- Suggest re-upload if needed.

## AI Self Challenge

If Marketing Score is below 80:

- AI must challenge its own output.
- Re-plan.
- Regenerate weak parts.
- Re-score.

Stop only if:

- Material is too poor.
- Product cannot be identified.
- User input is insufficient.
- AI Confidence is too low.

## Quality and Progress Principle

V1 prioritizes output quality over speed.

During generation, users must see:

- Current progress
- Current stage
- Estimated waiting time
- Clear error message
- Retry guidance
- Support guidance

Users can accept waiting, but they should not feel the system is stuck.

## Workflow Engine Architecture

```text
Frontend
-> Workflow Engine
-> AI Skills
-> Prompt Library
-> OpenAI
```

Rules:

- Frontend must not contain prompt logic.
- Workflow Engine controls execution order.
- Workflow Engine controls retry.
- Workflow Engine controls failure handling.
- Workflow Engine controls Self Challenge.
- AI Skills must remain modular.
- Prompt Library must be version controlled.

## Development Order

```text
Schema
-> Workflow
-> AI Skills
-> Prompt Library
-> Workflow Engine
-> API
-> Frontend
-> Testing
-> Release
```

## Documentation Before Development

Any development must be supported by:

- Blueprint
- Specification
- Schema
- Workflow
- AI Skill
- Prompt

before coding.

## Design Principles

### Sensible Defaults With AI Recommendations

Use sensible defaults, then let AI recommend improvements instead of asking users to configure everything upfront.

This principle applies to:

- Campaign Language
- Future subtitle style
- Future CTA
- Future hashtags
- Future posting time

## Architecture Principles

### AP-001 Workspace Architecture

Purpose:
Define the permanent multi-tenant architecture of EmberOS.

Workspace is the primary data isolation boundary.

Each Workspace owns exactly one Company Profile.

Architecture:

```text
Tenant
-> Workspace
-> Company Profile
-> Campaigns
```

Normal Tenant:

```text
1 Tenant
-> 1 Workspace
-> 1 Company Profile
```

Rules:

- One Tenant owns one Workspace.
- One Workspace owns one Company Profile.
- One Company Profile is shared by all Campaigns inside the Workspace.

Agency / Admin Tenant:

```text
Agency Tenant
-> Workspace A -> Company Profile A
-> Workspace B -> Company Profile B
-> Workspace C -> Company Profile C
```

Rules:

- One Agency Tenant may own multiple Workspaces.
- Each Workspace owns exactly one Company Profile.
- Data must never be shared across Workspaces unless explicitly implemented in future specifications.

Design Principles:

- Workspace is the security boundary.
- Company Profile belongs to Workspace.
- Campaign belongs to Workspace.
- AI Context belongs to Workspace.
- Assets belong to Workspace.
- Billing may belong to Workspace.

### AP-002 Language Separation

Language responsibilities are separated into three independent layers.

#### UI Language

Owner:
User Settings

Purpose:

- Application Interface
- Navigation
- Labels
- Buttons
- Error Messages

Rules:

- User can switch language anytime.
- Language switch is available from the application header.
- UI Language never affects AI output.

#### Business Languages

Owner:
Company Profile

Purpose:
Represents the long-term languages supported by the business.

Examples:

- English
- Chinese
- Bahasa Melayu
- Japanese

Rules:

- Used as business context.
- Available to AI Skills.
- Does not determine Campaign output language.

#### Campaign Language

Owner:
Campaign

Purpose:
Determines language for the current marketing task.

May include:

- Output Language
- Subtitle Language
- CTA Language
- Marketing Copy Language

Rules:

- Campaign Language is determined by Campaign Goal, Uploaded Assets, Target Audience, and AI Analysis.
- It is independent from UI Language and Business Languages.

### AP-003 AI Provider Architecture

Status:
Future

Target Specification:
SPEC-010 Workflow Engine

Principle:
Workflow is stable. AI Providers are replaceable.

Architecture:

```text
Workflow Engine
-> AI Router
-> Provider
```

Rules:

- Users never select AI Providers.
- AI Router automatically selects the appropriate Provider.
- Workflow must remain unchanged when Providers change.
- Business Logic belongs to Workflow.
- Provider implementation is replaceable.

Admin Override:
Admin may manually choose a Provider for:

- Testing
- Benchmarking
- Cost comparison
- Failover

This option is hidden from normal users.

Long-term Goal:
Future Provider selection may consider:

- Quality
- Cost
- Latency
- Availability
- Success Rate

without requiring any UI changes.

## Competitive Strategy

EmberOS does not compete feature-by-feature with ChatGPT, CapCut or Canva.

It competes against the fragmented workflow where owners must switch between multiple tools.

The main value is workflow consolidation and time savings.
