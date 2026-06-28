# Business Profile Specification

## Purpose

Business Profile stores the core long-term business facts used by EmberOS for AI planning, marketing content generation, campaign creation, reporting, and future publishing workflows.

Business Profile is background context. Campaign context can override generic Business Profile assumptions when the campaign is more specific.

## Required Fields

- Company Name
- Industry
- Services
- Region
- Target Audience
- Brand Voice

## Fields

### companyName

Type:
string

Required:
true

AI Usage:
Used as the business identity for AI outputs.

Rules:
- Editable.
- Warn user before changing.
- Changes may affect future AI outputs.
- Existing Campaigns are not regenerated automatically.

### industry

Type:
string

Required:
true

Input:
Dropdown + Custom

AI Usage:
Used as core business context for Marketing Angle, Hook, Caption, CTA, Marketing Report, and Success Prediction.

Rules:
- User may select from predefined industry options.
- User may enter a custom industry.

### services

Type:
object or array

Required:
true

Structure:
- Service List
- Description

AI Usage:
Used to understand what the business sells or provides.

Rules:
- AI prioritizes Service List.
- Description is supporting context.

### region

Type:
string

Required:
true

AI Usage:
Used for audience, cultural, platform, timing, and market assumptions.

Rules:
- AI may infer from user profile or workspace context only when reasonable.
- If region is missing or uncertain, ask user to confirm.

### targetAudience

Type:
array or string

Required:
true

AI Usage:
Used by Marketing Angle, Hook, Caption, CTA, Marketing Report, and Success Prediction.

Rules:
- AI may infer from Industry, Services, and Region.
- User may edit.
- User-confirmed value becomes source of truth.
- If confidence is low, ask for confirmation.

Flow:
AI Suggest -> User Confirm -> Source of Truth

### brandVoice

Type:
array

Required:
true

Input:
Campaign-level multi-select

AI Usage:
Controls tone and communication style for generated marketing content.

Rules:
- Brand Voice is selected at campaign level.
- Multiple values may be selected.
- Campaign-level Brand Voice can override generic Business Profile tone assumptions.

### businessDescription

Type:
string

Required:
false

AI Usage:
Provides business context for AI planning and marketing content generation.

Rules:
- User can write rough text.
- AI can polish or ask clarification.
- AI cannot invent business facts without confirmation.

### businessHours

Type:
object or array

Required:
false

AI Usage:
May support Schedule Posting, Auto Reply, Marketing Timing, and profile completeness.

Rules:
- Optional.
- Missing value must not block generation.
- Useful for businesses with fixed operating hours.
- Not required for freelancers.

### logo

Type:
string or asset reference

Required:
false

AI Usage:
Used for brand recognition and brand asset context.

Rules:
- Optional.
- Missing Logo must not block Campaign generation.

### brandColors

Type:
array or object

Required:
false

AI Usage:
Used for visual consistency in generated assets and future brand-aware workflows.

Rules:
- AI detects colors from Logo when available.
- If Logo is unavailable, use Workspace Default Theme.

### socialLinks

Type:
object

Required:
false

Stored Links:
- Website
- Facebook
- Instagram
- TikTok
- LinkedIn
- YouTube
- Xiaohongshu
- WhatsApp Business

AI Usage:
May support future Auto Publish, CTA, and Analytics features.

Rules:
- Optional.
- Store for future Auto Publish.
- Missing Social Links must not block Campaign generation.

### businessAssets

Type:
array or object

Required:
false

AI Usage:
Stores additional business brand or marketing assets for future workflows.

Rules:
- Optional.
- May include reusable brand, product, or campaign assets.

## Low Confidence Confirmation Flow

Rules:
- AI may infer from available context.
- AI must ask user to confirm when key context is missing or confidence is low.
- AI must not silently assume critical facts.
- If video and Business Profile conflict, ask user to confirm.

## Version History

- v1.0 - Added Business Profile schema fields from Session 010 and Session 011.
- v1.1 - Merged Blueprint v1.2 required fields, Brand Voice, Region, and Low Confidence Confirmation Flow.
