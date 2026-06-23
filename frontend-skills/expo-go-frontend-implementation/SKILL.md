---
name: expo-go-frontend-implementation
description: Use when implementing Expo Go-compatible React Native/TypeScript screens, components, animations, navigation, local state, and simulated data for the mobile prototype.
---

# Expo Go Frontend Implementation

## Purpose

Implement polished mobile UI in Expo, React Native, and TypeScript while staying compatible with Expo Go during the prototype phase.

## Guardrails

- Prefer Expo Go-compatible libraries.
- Avoid custom native modules unless the user approves a development build.
- Keep domain logic separate from screen components.
- Use TypeScript types for patient, health, game, mission, score, and companion state.
- Use simulated/local data only in v1.
- Do not add a production backend, real auth, real PHI storage, hardware ingestion, or AI features unless explicitly requested.

## Suggested Structure

```text
app/
  _layout.tsx
  index.tsx
  missions.tsx
  progress.tsx
  rewards.tsx
  stats.tsx
  profile.tsx

src/
  components/
  data/
  domain/
    companion/
    gamification/
    scoring/
  theme/
  types/
```

## Implementation Style

- Compose screens from reusable cards and focused components.
- Keep screens thin; calculations belong in `src/domain`.
- Keep demo data in `src/data` and label it clearly as simulated.
- Build mobile-first layouts with safe areas and large touch targets.
- Use simple, reliable animations before adding complex effects.

## Validation

When practical, run the relevant TypeScript, lint, and Expo checks. If a runnable UI changes, capture a screenshot when the environment supports it.
