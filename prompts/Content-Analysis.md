# Content Analysis Prompt Specification

## Purpose

Analyse the uploaded video and understand what is inside the content before generating any marketing output.

## Input

- Uploaded video metadata
- Transcript if available
- Visual analysis if available
- Business Profile
- Campaign Objective
- Optional user description

## Output

Structured JSON including:

- Product
- People
- Brand elements
- Target customer of the product
- Emotional tone
- Visual highlights
- Main selling points
- Confidence level
- Missing information

## Rules

- Do not generate captions.
- Do not generate subtitles.
- Do not generate strategy.
- Do not guess silently when confidence is low.
- If key information is missing, return suggested options and allow custom user input.

## V1 Scope

Content Analysis exists to understand the video. It does not create marketing assets directly.
