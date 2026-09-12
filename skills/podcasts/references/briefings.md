# Briefings & Summaries

## Episode Briefing Format

For each episode, generate:

```text
## [Show Name] - Episode Title
Guest: Name (who they are, why they matter)

### TL;DR (2-3 sentences)
What this episode is about and why it matters.

### Key Points
- Main insight 1
- Main insight 2
- Main insight 3

### Quotable Moments
> "Exact quote" — Guest, timestamp

### Action Items
- [ ] Specific thing to try
- [ ] Book/resource recommended

### Skip or Listen?
[MUST LISTEN / WORTH IT / SKIP] — reasoning in one line
```

## Briefing Triggers

Generate briefings when:

- A new episode from a subscribed show drops
- The user asks what an episode is about
- The user has limited time and needs to prioritize
- An episode is 2+ hours and the user wants highlights

Store durable briefings under `<state_root>/briefings/` when the user wants them kept.

## Time-Constrained Mode

When the user mentions time limits:

1. Compare episode length vs available time
2. Identify essential segments with timestamps when chapters or transcripts exist
3. Suggest ranges such as: "Listen to 15:00–32:00 and 1:45:00–2:10:00 — covers the main insights"
4. Offer a text summary for the remainder

If timestamps are unknown, say so and fall back to section-level guidance from the official show notes.

## Multi-Episode Digests

Weekly digest format:

```text
## This Week in Podcasts

### Must Listen (2)
- [Show] Episode about X — Guest Y did groundbreaking thing
- [Show] Episode about Z — Contrarian take worth hearing

### Worth Skimming (3)
- Brief descriptions...

### Safe to Skip (4)
- Why each can be skipped (repeat content, off-topic, outdated)
```

## Guest Context

Always provide guest context when known:

- Who they are (1 line)
- Why they are relevant (expertise, recent work)
- Previous appearances if useful
- Red flags when claims are disputed (note the dispute; do not invent controversy)

## Sources for Transcripts

Priority order:

1. Official transcript from the podcast website or CMS
2. Platform-provided transcripts (Apple Podcasts, Spotify when available)
3. YouTube captions (prefer human-reviewed over pure auto-captions)
4. Local Whisper / user-owned audio transcription
5. Third-party indexes (Podcast Index, Taddy) only as discovery aids

Always disclose when a summary comes from auto-generated captions; they may contain errors. Never present guessed quotes as exact.

## Operating Checks

- Prefer primary show notes and official transcripts over secondary recap blogs
- Mark confidence low when only title/description is available
- Keep briefing files portable under `<state_root>/briefings/`; do not hardcode machine-specific paths
