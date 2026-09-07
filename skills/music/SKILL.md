---
name: music
description: Track and organize music discoveries, favorites, concerts, and playlists. Use when the user shares a song, asks for music recommendations, or mentions a concert.
metadata:
  version: "1.0.0"
  openclaw: '{"emoji":"🎵"}'
---

## State location

Resolve `<state_root>` before reading or writing music data:

1. Use a host- or user-configured music-state path when one is explicitly supplied.
2. Otherwise use the first existing directory in this order: `<workspace>/music/`, `<workspace>/memory/music/`, then `~/music/`.
3. If none exists and the user asks to persist music data, create `<workspace>/music/`.

Use only the selected `<state_root>` for this invocation. Do not hardcode absolute paths.

## Quick Reference

| Resource | Description | When to load |
|----------|-------------|--------------|
| `references/domain-knowledge.md` | Contextual curation and memory tracking principles. | When making recommendations or organizing playlists. |
| `assets/data-templates.md` | Data structure templates for tracking files. | When creating or modifying data files in `<state_root>/`. |

## Core Behavior

- **Save Music:** When the user shares a song or album, offer to save it with context (e.g., mood, activity).
- **Recommend Music:** When the user asks for music, check their saved collection (`<state_root>/favorites/`, `<state_root>/playlists/`) first.
- **Track Concerts:** When the user mentions a concert, track it in `<state_root>/concerts/`.

## File Structure

```text
<state_root>/
├── discover/
│   └── to-listen.md
├── favorites/
│   ├── songs.md
│   ├── albums.md
│   └── artists.md
├── playlists/
│   ├── workout.md
│   ├── focus.md
│   └── road-trip.md
├── concerts/
│   ├── upcoming.md
│   └── attended/
├── collection/
│   └── vinyl.md
└── memories/
    └── YYYY.md
```

## Track Entry Requirements

When logging a new entry, include when known:

- Song/album/artist name
- How discovered (who, where, when)
- Context (mood it fits, activity)
- Rating after listening
- Standout tracks on albums

## Artist Deep Dives

When the user discovers an artist they love:

- Map discography chronologically.
- Note fan-favorite albums.
- Flag essential tracks for sampling.
- Track which albums have been explored vs pending.

## By Mood/Activity Guidelines

- **Workout:** High energy, tempo roughly 120+.
- **Focus:** Instrumental, ambient, lo-fi.
- **Cooking:** Upbeat, familiar favorites.
- **Sad hours:** Cathartic, emotional.
- **Party:** Crowd-pleasers, danceable.
- **Road trip:** Singalongs, classics.

## Surfacing Context

Actively surface saved content when relevant:

- "You saved that album months ago and still have not listened."
- "An artist you like is touring near you."
- "Last time you needed focus music you liked Tycho."
- "This sounds like artists already in your favorites."

## Progressive Enhancement

- **Week 1:** Capture current favorite songs/albums.
- **Ongoing:** Save discoveries with their source.
- **Over time:** Build mood-based playlists and log attended concerts.

## Required Operating Principles

- **Platform Agnostic:** Stay independent of specific streaming platforms unless the user explicitly provides an integration.
- **Respect Preferences:** Recommend only within genres and moods the user has shown interest in.
- **Maintain Simplicity:** Keep organization structures flat and rely on simple markdown lists.
- **Confirm Context:** Ask for the target mood or activity before generating a new playlist when that context is missing.
