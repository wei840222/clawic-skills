# AI-Tell Sweep

Before delivery, remove structural signals of translated or generated Japanese:

- `〜することができます` when `〜できる／できます` says the same thing.
- Repeated hedges: `〜と言えるでしょう`, `〜ではないでしょうか`.
- Essay scaffolding: `まず／次に／そして／最後に` without a real sequence.
- Repeated subjects (`私は`, `私たちは`) that Japanese would drop.
- Uniform です・ます sentence length, zero particles in casual chat, or document headings in a LINE message.
- Literal English idioms and heavy Sino-Japanese padding (`〜における`, `〜に関して`) where a simple relation works.

Read the result aloud. Keep a deliberate register and the facts from the request; polish must not add claims.
