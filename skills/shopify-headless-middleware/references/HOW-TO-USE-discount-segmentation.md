# How to Use: Discount Segmentation Reference

## File This Guide Supports

```text
skills/shopify-headless-middleware/references/discount-segmentation.md
```

This guide explains how to use the `discount-segmentation.md` reference during an **AI-SDLC Mob Programming** session for Shopify Headless middleware teams.

The focus is specific:

```text
Guest and logged-in customer discount segmentation
for Shopify Headless middleware architecture
```

This is not a traditional SDLC handoff document. It is a working guide for a live collaborative session where the team uses AI, GitHub Copilot, Shopify knowledge, middleware architecture, and testing practices together.

## How to Use With GitHub Copilot

Open the repository in VS Code.

Open this file:

```text
skills/shopify-headless-middleware/references/discount-segmentation.md
```

Then use GitHub Copilot Chat with a prompt like:

```text
Use the open file discount-segmentation.md as context.

Act as an AI-SDLC mob programming assistant for a Shopify Headless middleware team.

Help us run a mob session for guest and logged-in customer discount segmentation.

Generate:
- required tools
- required logins
- required Shopify scopes to review
- ideal mob roles
- session scope
- customer segments
- discount rule table
- middleware API contract for /discount/evaluate
- edge cases
- test scenario matrix
- expected session outcomes
- implementation checklist
```

## Expected Outcomes

By the end of the mob session, the team should have:

- Confirmed customer segment model
- Guest vs logged-in discount behavior
- VIP / wholesale handling
- Discount stacking policy
- Middleware API contract for `/discount/evaluate`
- Shopify dependency list
- Shopify API scopes to review
- Frontend display behavior
- Cache and performance assumptions
- Error handling strategy
- Security considerations
- Test scenario matrix
- Backlog-ready implementation checklist
