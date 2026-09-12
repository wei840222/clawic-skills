# Discovery & Recommendations

## Finding New Shows

Base suggestions on demonstrated listening patterns:

- Similar topics to current subscriptions
- Guests that appeared on shows the user likes
- Hosts the user already trusts
- Different perspectives on topics the user cares about

Do not invent chart rankings. If external trend data is unavailable, say so and recommend from the user's own history first.

## Guest Watchlist

Track VIP guests across podcasts in `<state_root>/guests.md`:

```text
## My Guest Watchlist
- Naval Ravikant
- Andrew Huberman
- Tim Ferriss
```

Alert when any appear on **any** podcast, including unsubscribed ones, when the user asks for guest monitoring or when a watchlist entry matches a new episode.

## Topic Alerts

Track topics across shows when the user opts in:

- "AI safety discussed"
- "New longevity research"
- Including unsubscribed shows when discovery mode is on

Record durable topic filters beside the watchlist or in a short note under `<state_root>/`.

## Managing Duplicates

When the same guest does a podcast tour:

- Identify overlapping talking points
- Recommend the **best single** appearance for depth or unique angle
- Note what is unique on each show
- Prefer "Skip X, it largely repeats Y" over forcing every listen

## Trending Detection

Surface episodes that, with evidence:

- Spike discussion within ~24 hours
- Get referenced by other trusted shows
- Show unusually high engagement on platforms the user already uses

If engagement signals are unavailable, skip trend claims rather than fabricating virality.

## Backlog Management

When the user is falling behind:

- Identify skippable episodes (outdated, filler, pure repeat guests)
- Find catch-up or highlights episodes some shows publish
- Create a bankruptcy plan for massive backlogs
- Suggest a concrete restart point and a time-boxed first batch

Tie plans to the actual `queue.md` and available hours.

## Discovery Commands

| User says | Agent does |
|-----------|------------|
| "Find podcasts like Huberman" | Suggest similar educational shows from patterns + stated interests |
| "What's trending this week?" | Surface discussed episodes only with evidence; else say unknown |
| "I'm too far behind on X" | Build a catch-up plan against `queue.md` |
| "Anything new from [guest]?" | Check watchlist + recent appearances |

## Safety and Scope

- Recommendations are curation aids, not medical, legal, or financial advice
- Do not scrape or bypass paid feeds the user does not own access to
- Keep discovery state under the resolved `<state_root>`
