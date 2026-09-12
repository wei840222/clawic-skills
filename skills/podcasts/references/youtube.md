# YouTube Video Podcasts

## Key Differences from Audio

- Thumbnails and titles often drive discovery more than RSS alone
- Clips channels may be separate from the main channel
- Comments can carry community timestamps
- Algorithm recommendations are platform-specific and opaque
- Visual content (reactions, demos, slides) can matter for value

## Channel Tracking

For YouTube podcast channels, track when useful:

- Main channel (full episodes)
- Clips channel if it exists
- Upload cadence
- Typical episode length
- Guest announcement patterns

Store channel identifiers the user cares about under `<state_root>/subscriptions.md` or a short YouTube section there — still inside the resolved state root.

## Clip Extraction

When the user wants highlights:

1. Check whether an official clips channel already published the moment
2. Identify highly shared segments only with evidence (comments, chapters, official cuts)
3. Use chapter markers when available
4. Generate timestamps for key segments from transcripts or chapters — never invent precise times

Clip types worth labeling:

- Emotional peaks (laughter, tension)
- Quotable moments
- Contrarian takes
- Practical advice
- Meme-worthy exchanges

## YouTube-Specific Commands

| User says | Agent does |
|-----------|------------|
| "Follow JRE clips" | Track clips channel; notify on new relevant clips |
| "Find the viral moment" | Identify most-referenced segment with evidence or say unknown |
| "What's the timestamp for AI discussion?" | Use chapters/transcript; else admit gap |
| "Who was that neuroscientist?" | Resolve guest from description/trusted metadata |

## Cross-Platform Guest Tracking

The same guest often appears on multiple YouTube podcasts (for example Lex Fridman, JRE, Diary of a CEO, Huberman Lab). When tracking a guest:

1. Find recent appearances the user can access
2. Separate unique content from repeated talking points
3. Recommend **one** primary appearance
4. Note depth/angle differences briefly

## Thumbnail & Title Patterns

YouTube titles may obscure guest identity:

- "This Neuroscientist Reveals..." → identify the actual guest
- "Billionaire Explains..." → who is it?
- "The Truth About..." → what is the real topic?

Parse titles, descriptions, and thumbnails to extract:

- Guest name
- Topic
- Clickbait level
- Actual value signal

Prefer description and chapter data over thumbnail marketing copy.

## Limits

- Do not claim view counts or "viral" status without a checkable signal
- Do not bypass age gates, region locks, or membership walls
- Treat auto-captions as lossy; disclose that when briefing from them
