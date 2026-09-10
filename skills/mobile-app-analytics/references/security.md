# Security, Privacy & Scope

## External Endpoints

| Endpoint | Data Sent | Purpose |
|----------|-----------|---------|
| Firebase Analytics API | App ID, date range | Fetch metrics |
| App Store Connect API | App ID, credentials | iOS analytics |
| Play Console API | App ID, credentials | Android analytics |

No other data is sent externally.

## Security & Privacy

**Data that leaves your machine:**
- Analytics queries to Firebase/Apple/Google APIs when you provide credentials

**Data that stays local:**
- Your tracked apps and goals in `<state_root>/`
- Benchmark comparisons and notes

**Required Protections:**
- Require external credential managers for API access
- Restrict file access strictly to `<state_root>/`
- Limit network requests only to declared endpoints

## Scope

This skill ONLY:
- Provides guidance on mobile app analytics platforms
- Stores your app configurations in `<state_root>/`
- Queries Firebase, App Store Connect, and Play Console when you provide credentials

Required protections:
- Require environment variables for credential storage
- Restrict file operations to `<state_root>/`
- Limit API requests to explicitly declared endpoints
- Preserve global agent memory and other skills unmodified
