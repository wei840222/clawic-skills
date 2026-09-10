# Core Rules & Common Traps

## Core Rules

### 1. Platform Detection
Detect from context which platform(s) the app targets:
- iOS only → focus on App Store Connect + Firebase
- Android only → focus on Play Console + Firebase
- Cross-platform → cover both stores + unified Firebase

### 2. Metric Hierarchy
Always prioritize metrics in this order:
1. **Revenue metrics** (LTV, ARPU, conversion) — what pays the bills
2. **Retention metrics** (D1, D7, D30) — determines long-term success
3. **Engagement metrics** (DAU/MAU, session length) — leading indicators
4. **Acquisition metrics** (installs, sources) — growth levers

### 3. Cohort-First Analysis
Always segment numbers by:
- Install cohort (when users joined)
- Acquisition source (organic, paid, referral)
- User tier (free, trial, paid)
- Platform (iOS vs Android)

### 4. Alert Thresholds
Proactively flag anomalies:
| Metric | Alert if |
|--------|----------|
| D1 retention | < 25% (below industry floor) |
| Crash-free rate | < 99% |
| DAU/MAU ratio | Drops > 10% week-over-week |
| LTV:CAC ratio | < 3:1 |

### 5. Data Freshness
Know platform data delays:
| Source | Typical Delay |
|--------|---------------|
| Firebase real-time | Minutes |
| Firebase daily reports | 24-48h for full data |
| App Store Connect | 24-48h |
| Play Console | 24-48h |

### 6. Privacy Compliance
- Ensure custom events exclude PII
- Respect ATT (iOS) and consent requirements
- User properties: ensure demographics are used while excluding personal identifiers
- GDPR: support data deletion requests

### 7. Event Naming Conventions
Enforce consistent naming across platforms:
```
{verb}_{noun}[_{qualifier}]

Examples:
- view_screen_home
- tap_button_subscribe
- complete_purchase_annual
- start_onboarding_step1
```

## Common Traps

- **Vanity metrics obsession** → Total downloads means nothing; track active users and retention instead
- **Ignoring platform differences** → iOS users often have 20-30% higher LTV; analyze iOS and Android data separately before merging
- **Wrong attribution window** → 7-day attribution misses subscription conversions; use 30-day for subscriptions
- **Survivorship bias** → Analyzing only current users ignores why churned users left
- **Timezone mismatches** → Firebase uses UTC by default; App Store uses your configured timezone
