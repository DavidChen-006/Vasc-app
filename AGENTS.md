# AGENTS.md

## Project Mission

This repository is for a mobile prototype that motivates cardiovascular patients to build safer, more consistent health habits through a playful, gamified experience.

The v1 product should feel like a Duolingo-style health companion: approachable, colorful, encouraging, and interactive. The central visual metaphor is a 2D cardiovascular health character that acts like both a pet and a virtual twin of the patient. The character should communicate health state through universally understandable cues such as warmth, color, expression, energy, posture, and celebration rather than realistic anatomy.

## Current V1 Scope

Focus v1 on an individual patient experience using simulated data only.

Build toward these core loops:

1. The user opens the app.
2. The user sees a 2D heart/cardio companion whose mood reflects today’s simulated cardiovascular status.
3. The user sees a daily Cardio Score or Heart Score.
4. The user completes one or more safe daily missions.
5. The user earns XP, maintains a streak, closes progress rings, unlocks badges, and sees progress over time.
6. The app encourages the user to return tomorrow without shame or unsafe pressure.

## Technical Direction

Use Expo, React Native, and TypeScript for the mobile app unless the user explicitly changes the stack.

Prioritize Expo Go-compatible solutions while the app is a prototype. Avoid dependencies that require custom native code unless the user explicitly approves moving to a development build.

Expected stack direction:

- Expo
- React Native
- TypeScript
- Expo Router when navigation is introduced
- Local simulated data for v1
- No production backend for v1
- No real patient data for v1
- No AI features for v1
- No hardware integration for v1

## Visual and UX Direction

The app should use a playful 2D style, not a realistic anatomical heart.

Use the 2D cardiovascular character to communicate status clearly:

- Blue, cold, tired, or low-energy states can represent poor or concerning performance.
- Warm red, pink, orange, glowing, smiling, or energetic states can represent better performance.
- Expressions, motion, warmth, and celebration should make the status understandable without medical expertise.
- The character should feel supportive and companion-like, not judgmental.

The user should not need to understand medical anatomy to understand whether they are improving.

## Gamification Mechanics for V1

Implement or design toward these v1 mechanics:

- 2D cardiovascular companion character
- Daily Cardio Score or Heart Score
- Daily missions
- XP or Pulse Points
- Levels or Vitality Levels
- Heart streaks
- Streak freezes, rest days, or recovery pauses
- Progress rings for categories such as movement, monitoring, medication, learning, or recovery
- Calendar or heatmap-style progress visualization
- Badges and milestone rewards
- Weekly recap
- Personal-best progress against the user’s own baseline

Reward consistency, safe adherence, and comeback behavior more than intensity.

## Health and Safety Rules

This app is a prototype and must use simulated data only until the user explicitly asks to add real data handling.

Do not present the app as diagnosing, treating, preventing, or curing disease. Avoid medical claims.

Do not encourage users to push through symptoms or compete on raw exertion. Avoid mechanics that reward unsafe intensity, speed, distance, or extreme activity.

Use compassionate language. Prefer terms such as:

- small win
- back on track
- recovery day
- rest day
- gentle restart
- building momentum
- consistency

Avoid shame-based language such as:

- failure
- weak patient
- bad score because you failed
- punishment
- lost because you rested

If future work introduces real health data, clinician workflows, hardware ingestion, social features, or AI recommendations, pause and revisit privacy, security, compliance, and medical safety requirements first.

## V1 Non-Goals

The following are explicitly out of scope for v1:

- No production backend
- No real patient data
- No AI features or AI recommendations
- No hardware or device integration
- No clinician workflows
- No social or multiplayer features
- No medical diagnosis, treatment, or claims
