---
name: cardio-companion-visual-design
description: Use when designing or implementing the app's 2D cardiovascular companion, visual health states, character expressions, mascot-like feedback, or playful heart-themed UI moments.
---

# Cardio Companion Visual Design

## Purpose

Create a playful 2D cardiovascular companion that acts like both a pet and a virtual twin of the patient. It should make cardiovascular status understandable through color, expression, motion, warmth, and celebration instead of realistic anatomy.

## Design Principles

- Use a friendly 2D heart/cardio character, not a realistic anatomical heart.
- Communicate state with universal signals: color temperature, posture, facial expression, glow, motion, and energy.
- Make the companion supportive and emotionally warm; never judgmental or scary.
- Prefer delightful Duolingo/Finch-like clarity over clinical realism.
- The user should understand the character's state without medical expertise.

## Suggested Character States

| State | Visual cues | Copy tone |
| --- | --- | --- |
| Cold / low | blue tint, droopy posture, slow pulse, sleepy eyes | gentle, supportive |
| Recovering | purple/pink transition, small smile, soft pulse | encouraging |
| Stable | warm pink/red, relaxed smile, steady pulse | calm confidence |
| Energized | bright red/orange, glow, bounce, sparkles | celebratory |
| Rest day | blanket, moon, soft blue/pink, relaxed face | restorative, not negative |

## Implementation Guidance

- Drive the character from domain state, not hardcoded screen logic.
- Create a small `CompanionState` type that maps score, streak, mission completion, and rest mode to visual states.
- Keep the first version simple: static SVG-like shapes, emoji-like facial expressions, gradients, and lightweight animations.
- Add richer animation only after the core loop works.

## Avoid

- Gore, anatomical realism, plaque imagery, or fear-based visuals.
- Making the character look punished, dying, or neglected.
- Red/blue meanings that conflict with the current app legend.
