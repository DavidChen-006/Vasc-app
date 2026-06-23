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

Do not build these in v1 unless the user explicitly changes the scope:

- Real patient authentication
- Production backend
- Real hardware integration
- Real doctor portal
- Social network
- Public leaderboards
- AI recommendations
- Medical diagnosis or treatment guidance
- EHR integration
- Payment system
- Real patient health data storage
- Realistic 3D anatomical heart visualization

## Later Phase Foreshadowing

The v1 architecture should leave room for later phases:

- Hardware data ingestion can replace simulated metrics later.
- Doctor-assigned missions can replace or augment demo missions later.
- Social/community features can use ranks, badges, and progress summaries later.
- AI features may be added later for summaries or coaching only after safety requirements are defined.
- Real health data requires a separate privacy, security, and compliance plan.

Keep v1 code modular so later phases can connect to the same core concepts: metrics, scoring, missions, character state, rewards, and progress history.

## Suggested Code Organization Once the App Is Scaffolded

When the Expo app is created, prefer a structure like:

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
    CardioCompanion/
    HeartRings/
    MissionCard.tsx
    ProgressHeatmap.tsx
    RewardBadge.tsx
    StreakCard.tsx

  data/
    demoMissions.ts
    demoProfile.ts
    simulatedHealthData.ts

  domain/
    gamification/
    scoring/
    companion/

  theme/
    colors.ts
    spacing.ts
    typography.ts

  types/
    game.ts
    health.ts
    patient.ts
```

Keep domain logic separate from UI components. For example, scoring and gamification calculations should live outside screens so they can later be reused with real hardware or backend data.

## Development Practices

- Prefer TypeScript with clear domain types.
- Keep components small and focused.
- Keep simulated data obvious and easy to replace.
- Do not wrap imports in try/catch blocks.
- Favor readable, maintainable code over premature abstraction.
- When adding UI, prioritize mobile-first layout and Expo Go compatibility.
- When adding copy, keep it encouraging, clear, and medically cautious.

## Frontend Skill Packs

Repo-local frontend skills live in `frontend-skills/`. Use them as task-specific guidance when designing or implementing the app:

- `cardio-companion-visual-design`: 2D cardiovascular companion, mascot states, color/expression language, and emotionally clear heart visuals.
- `mobile-design-system`: theme tokens, mobile layout, reusable cards, typography, spacing, and core design components.
- `gamified-health-ui`: missions, XP, streaks, recovery freezes, progress rings, badges, weekly recaps, and safe habit loops.
- `expo-go-frontend-implementation`: Expo Go-compatible React Native/TypeScript implementation structure and guardrails.
- `motion-microinteractions`: Expo-compatible animation, companion motion, reward celebrations, progress transitions, and reduced-motion behavior.
- `health-accessibility-review`: accessibility, health-safety, privacy, copy tone, and emotional-safety review.

When multiple skills apply, load only the specific skill files needed for the current task. These skills are intentionally curated from the frontend-design, taste-skill, aesthetic-anchor, component-system, and health-safety ideas discussed for this project rather than copying full external repositories into the app.
