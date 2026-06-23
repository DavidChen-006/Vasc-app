---
name: motion-microinteractions
description: Use when designing or implementing Expo-compatible animation, companion motion, reward celebrations, progress transitions, reduced-motion behavior, or mobile microinteractions.
---

# Motion Microinteractions

## Purpose

Make the app feel delightful and alive without creating urgency, pressure, or inaccessible motion. Motion should reinforce safe habit loops and the 2D companion's emotional state.

## Preferred Motion Moments

- Companion idle breathing or gentle pulse.
- Mission completion bounce.
- Ring progress sweep.
- Pulse Points/XP count-up.
- Badge unlock pop.
- Streak preserved glow.
- Recovery freeze/rest day soft shimmer.
- Weekly recap reveal.
- Gentle restart animation after missed days.

## Motion Tone

- Warm, brief, readable, and playful.
- More like encouragement than alarm.
- Celebrate consistency and comeback behavior.
- Avoid frantic urgency, flashing danger states, or pressure-inducing countdowns.

## Expo Go Guidance

- Start with React Native `Animated` and lightweight transform/opacity animations.
- Use `react-native-svg` for simple progress rings, badges, and character shapes when available.
- Add heavier animation libraries only when needed and only after checking Expo Go compatibility.
- Keep animation logic isolated from scoring and domain calculations.

## Accessibility

- Keep important information available as text, not motion alone.
- Keep animations short and non-blocking.
- Honor reduced-motion preferences where feasible.
- Avoid flashing and rapid pulsing.
