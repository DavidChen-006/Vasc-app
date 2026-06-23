---
name: mobile-design-system
description: Use when creating the app's mobile UI foundation, theme tokens, typography, spacing, color palette, cards, navigation surfaces, or reusable design components.
---

# Mobile Design System

## Purpose

Create a cohesive Expo/React Native design system for a playful cardiovascular health app. The UI should feel premium enough for healthcare, but expressive enough to support a Duolingo-like gamified loop.

## Visual Direction

- Mobile-first, iOS and Android compatible.
- Playful 2D health companion aesthetic.
- Warm, optimistic color palette with clear health-state semantics.
- Rounded cards, large touch targets, friendly illustration surfaces, strong hierarchy.
- Avoid generic blue SaaS dashboards and bland white medical portals.

## Token Priorities

Define tokens for:

- semantic colors: success, caution, rest, recovery, low-energy, celebration;
- surface colors: background, elevated card, soft panel, overlay;
- typography scale: display, title, section, body, caption, badge;
- spacing scale: compact mobile rhythm with consistent card gutters;
- radii: pill, card, full circle;
- shadow/elevation: subtle, warm, non-clinical;
- motion durations: fast tap, normal transition, celebration.

## Component Priorities

Start with:

- dashboard cards;
- heart companion stage;
- progress rings;
- mission cards;
- streak card;
- XP/level progress bar;
- badge tiles;
- heatmap/calendar cells;
- stat cards;
- weekly recap panel.

## Quality Bar

- Every screen needs a clear primary action.
- Cards should have visible hierarchy: title, value, context, action.
- The UI must be readable in one-handed mobile use.
- Use empty/loading/demo states intentionally.
- Prefer one strong visual idea per screen over many decorative elements.
