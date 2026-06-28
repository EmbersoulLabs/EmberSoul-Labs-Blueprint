# EmberSoul Labs Blueprint

This repository is the product knowledge base for EmberSoul Labs.

It is used as the single source of truth for:

- Product vision
- Product roadmap
- EmberOS V1 Blueprint
- Product decisions
- Founder notes
- AI workflow
- Prompt library
- Cursor development instructions

## Current Focus

The current development focus is **EmberOS V1**.

Other products and future versions are recorded for long-term planning only. They must not expand or delay EmberOS V1 launch scope.

## Core Principle

Ship V1 first. Run into real user pain. Improve after launch.

## Repository Structure

```text
docs/
  00-Founder/
  01-Roadmap/
  02-EmberOS/
  03-EmberCore/
  99-Parking-Lot/
prompts/
```

## Development Rule

Before implementing any EmberOS feature, Cursor or any developer must read:

1. `docs/02-EmberOS/V1-Blueprint.md`
2. `docs/02-EmberOS/Decision-Log.md`
3. Related files in `prompts/`

Locked decisions must not be changed unless the founder explicitly unlocks them.
