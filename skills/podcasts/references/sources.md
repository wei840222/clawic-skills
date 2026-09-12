# Sources — Podcasts

Primary references used while hardening `podcasts`. Prefer canonical specs and platform docs over secondary recap blogs.

## Feeds, discovery, and indexing

- **RSS 2.0 Specification (Harvard / Berkman)** — baseline feed structure for enclosures and channel metadata via https://www.rssboard.org/rss-specification
- **Apple Podcasts Connect — Podcast RSS feed requirements** — tagging and enclosure expectations for show distribution via https://podcasters.apple.com/support/823-podcast-requirements
- **Podcasting 2.0 / Podcast Namespace** — modern podcast tags (transcripts, chapters, people, locking) via https://github.com/Podcastindex-org/podcast-namespace
- **Podcast Index API docs** — open podcast directory and search patterns via https://podcastindex-org.github.io/docs-api/
- **W3C Media Podcasts CG notes (where applicable)** — broader open media distribution context via https://www.w3.org/community/podcasters/

## Transcripts, chapters, and accessibility

- **Podcast Namespace `transcript` tag** — machine-discoverable transcript links in feeds via https://github.com/Podcastindex-org/podcast-namespace/blob/main/docs/1.0.md
- **Podcast Namespace `chapters` tag** — chapter JSON conventions for timestamped navigation via https://github.com/Podcastindex-org/podcast-namespace/blob/main/docs/1.0.md
- **Apple Podcasts — transcripts overview** — platform transcript availability for listeners via https://support.apple.com/guide/podcasts/see-episode-transcripts-podc6eb5f63/mac
- **Spotify for Podcasters — transcription** — creator-side transcript tooling context via https://support.spotify.com/us/podcasters/article/transcription/
- **W3C WebVTT** — common caption/subtitle format when working from timed text via https://www.w3.org/TR/webvtt1/

## YouTube and video-podcast specifics

- **YouTube Data API (v3) — Searching for content** — channel/video metadata lookup patterns via https://developers.google.com/youtube/v3/guides/searching_for_videos
- **YouTube Help — Add chapters to videos / timestamps** — chapter marker conventions in descriptions via https://support.google.com/youtube/answer/9884579
- **YouTube Help — Captions and subtitles** — caption sources and accuracy caveats via https://support.google.com/youtube/answer/2734796

## Listening hygiene and knowledge capture

- **Nielsen Norman Group — Progressive Disclosure** — load detail only when the task needs it (mirrors reference routing here) via https://www.nngroup.com/articles/progressive-disclosure/
- **FTC — Protecting Personal Information: A Guide for Business** — minimize sensitive personal listening notes; purpose-limit stored detail via https://www.ftc.gov/business-guidance/resources/protecting-personal-information-guide-business

## Usage notes

- Treat feed + official show notes as ground truth for titles, guests, and publish dates.
- Prefer Podcasting 2.0 transcript/chapter tags when present before scraping secondary sites.
- Label auto-captions and ASR output as lossy; never upgrade them to verified quotes without checking.
- When a ranking or "trending" claim depends on a closed platform algorithm, mark confidence limited and avoid inventing placement mechanics.
