# Business Profile Specification

## Purpose

Business Profile stores the core business facts used by EmberOS for AI planning, marketing content generation, campaign creation, reporting, and future publishing workflows.

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

### targetAudience

Type:
array or string

Required:
recommended, but AI may infer

AI Usage:
Used by Marketing Angle, Hook, Caption, CTA, Marketing Report, and Success Prediction.

Rules:
- AI infers from Industry, Services, and Region.
- User may edit.
- User-confirmed value becomes source of truth.

Flow:
AI Suggest
↓
User Confirm
↓
Source of Truth

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

## Fields Added in Session 010

- Company Name
- Industry
- Services

## Fields Added in Session 011

- Logo
- Brand Colors
- Social Links
- Business Description
- Target Audience
- Business Hours
- Business Assets
