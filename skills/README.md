# Skills

Each folder teaches the agent one job. The agent runs them in this order:

1. **intake** → sets up a new brand (once per brand)
2. **audience-voice** → saves the audience's exact words in `brand/phrase-bank.md` (monthly)
3. **research** → finds topics and turns them into post ideas
4. **planning** → builds the monthly plan and weekly calendar, picks which ideas get made
5. **scripts** → writes the words for each post
6. **video** (handoff to the team's editor), **carousels**, **static-posts**, **pins**, **stories** → build the media
7. **quality-check** → approves, sends back for fixes, or holds each post
8. **posting** → publishes approved posts on schedule
9. **reporting** → measures results and writes the weekly report
10. **engagement** → handles comments and messages

## Rules every skill follows
- Read the `brand/` files before creating anything.
- Read `config/settings.yaml` for platforms, schedule and limits.
- Never put API keys in files. Keys come from GitHub Secrets.
- Pass work along as a **post package** (below).

## The post package
Every post is one folder named `YYYY-MM-DD_platform_format_short-title` with:
- `post.json` — everything about the post
- the media files (video, images)

`post.json` looks like this:

```json
{
  "id": "2026-11-03_instagram_reel_morning-routine",
  "status": "idea | draft | editing | approved | needs_review | posted | failed",
  "pillar": "Pillar name from brand/pillars.md",
  "platform": "instagram | facebook | pinterest | tiktok | youtube | linkedin",
  "format": "reel | carousel | pin | story | image",
  "static_type": "tip | quote | stat | offer | testimonial",
  "goal": "reach | trust | sales",
  "planned_date": "",
  "idea": { "angle": "", "why_now": "", "source": "" },
  "hook": "",
  "script": [ { "scene": 1, "on_screen_text": "", "seconds": 3 } ],
  "slides": [ { "slide": 1, "heading": "", "body": "" } ],
  "caption": "",
  "hashtags": [],
  "cta": "",
  "title": "",
  "description": "",
  "link": "",
  "board": "",
  "alt_text": [],
  "media": [],
  "credits": [],
  "scheduled_time": "",
  "checks": {},
  "posted": { "post_id": "", "permalink": "", "time": "" },
  "results": {}
}
```

Only the fields that fit the format get filled in.

## Where packages live (Google Drive)
| Folder | Status |
|---|---|
| 01 Research | raw research notes |
| 02 Ideas | `idea` |
| 03 Drafts | `draft` |
| 04 Review | `needs_review` |
| 05 Approved | `approved` |
| 06 Posted | `posted` |
| 07 Reports | weekly reports and learnings |
