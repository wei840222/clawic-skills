# Progress Tracking & Progression

## Workout Log Format

Store session logs in `<state_root>/workouts/`:

```text
## 2024-01-15 - Push Day
- Bench Press: 80kg 4x8,8,7,6 RPE 8
- OHP: 50kg 3x10,10,9
- Incline DB: 30kg 3x12
- Lateral Raises: 12kg 3x15
Notes: Left shoulder tight on last set of OHP
```

## PR Tracking

Store personal records in `<state_root>/prs/`:

```text
## Bench Press
- 1RM: 100kg (2024-01-01)
- 5RM: 85kg (2024-01-10)
- 10RM: 70kg (2024-01-05)

## Squat
- 1RM: 140kg (2024-01-08)
```

## Progression Methods

### Linear Progression (Beginners)
- Add weight every session: +2.5kg upper, +5kg lower
- When all reps are not completed, keep the same weight
- After 2-3 stalled sessions, deload about 10%

### Double Progression (Intermediate)
- Set a rep range (for example, 3x8-12)
- Start at the bottom of the range with the current weight
- Add reps each session until the top of the range
- When the top of the range is hit for all sets, increase weight and restart

### RPE-Based (Advanced)
| RPE | Meaning | Action |
|---|---|---|
| 6-7 | 3-4 reps in reserve | Warm-up weight, increase |
| 8 | 2 reps in reserve | Target for main sets |
| 9 | 1 rep in reserve | Acceptable for top sets |
| 10 | Max effort | Testing only, not routine training |

## Volume Landmarks

### Sets Per Muscle Group Per Week
| Level | Minimum | Target | Maximum |
|---|---|---|---|
| Beginner | 6 | 10-12 | 15 |
| Intermediate | 10 | 15-18 | 22 |
| Advanced | 12 | 18-22 | 25+ |

### Detecting Over/Under Training
- Under: below minimum volume, strength declining, always feeling fresh
- Optimal: steady progress, moderate soreness, good recovery
- Over: strength plateau, chronic fatigue, joint pain, poor sleep

## Deload Protocol

### When to Deload
- Every 4-6 weeks of hard training
- Persistent fatigue despite good sleep
- Joints aching beyond ordinary muscle soreness
- Motivation crashes
- Strength decline across multiple exercises

### How to Deload
- Volume deload: keep weight, reduce sets by 40-50%
- Intensity deload: keep sets, reduce weight by 40-50%
- Full deload: about 50% volume and 50% intensity
- Duration: 1 week (3-4 sessions)

## Stall Troubleshooting

### If Progress Stops
1. Check sleep — under 7h consistently undermines progress
2. Check calories — confirm intake supports training
3. Check recovery — account for life stress
4. Check volume — too much or too little
5. Change stimulus — rotate an exercise variation after long plateaus

### Breaking Plateaus
- Change rep scheme (5x5 → 3x8)
- Change exercise variation (back squat → front squat)
- Add pause reps or tempo work
- Reduce frequency, increase intensity
- Use a planned deload, then return to progressive loading

## Body Measurements

Store measurements in `<state_root>/measurements/`:

```text
## 2024-01-01
- Weight: 82.5kg (morning, fasted)
- Chest: 102cm
- Waist: 84cm
- Hips: 98cm
- Arms: 38cm
- Thighs: 60cm

## Notes
- Measure same time, same conditions
- Weekly weight, monthly circumferences
- Use 7-day weight average for trends
```

## Progress Indicators

### Good Signs
- Strength increasing, even slowly
- Body composition improving
- Energy levels stable
- Sleep quality maintained
- Training still enjoyable

### Warning Signs
- Same weight/reps for 3+ weeks
- Dreading sessions
- Chronic joint pain beyond muscle soreness
- Sleep getting worse
- Appetite suppressed

## Domain Knowledge: Progressive Overload

Progressive overload means increasing resistance, repetitions, or total volume over time so adaptation continues.
- Raise load, reps, or useful density across successive workouts when recovery allows.
- Keep week-over-week load jumps modest; the skill default caps them at 10%.
- Valid methods include more volume, more intensity, slower tempo, or shorter rest when form stays clean.
