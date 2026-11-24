---
name: scripts
description: Writes all the words for each post idea in the brand's voice — hooks, video scripts, slide text, captions, hashtags, pin titles and descriptions, and alt text.
---

# Scripts Skill

## 1. Job
Turn each idea into every piece of writing the post needs, in the brand's voice and within each platform's limits.

## 2. Inputs
- Post packages in **02 Ideas**
- `brand/voice.md` — tone, sample captions, calls to action, hashtag rules
- `brand/words.md` — words to use and avoid, claims not allowed
- `brand/audience.md` — who is reading
- `brand/phrase-bank.md` — the audience's exact words, from audience-voice
- `brand/visuals.md` — max words on screen at once
- `config/settings.yaml` — video length range, slide count
- Templates in `templates/`

## 3. Tools
- Claude (writing)
- Google Drive (read and save)

## 4. Steps
1. Read `voice.md`, `words.md`, `audience.md`, `phrase-bank.md` and `visuals.md`.
2. Open the next post package in 02 Ideas that has a `planned_date` (set by planning).
3. Write the hook.
   1. 10 words or fewer (8 or fewer for a carousel's first slide).
   2. Speaks to one pain, want or doubt, using the audience's words from `phrase-bank.md` where it fits.
   3. Write 3 hooks and keep the strongest one.
   4. Use the `cta` planning chose for the post.
4. Write the body based on the format.
   - **Reel** (use `templates/reel-script.md`):
     1. Scene 1 is the hook, on screen for 2–3 seconds.
     2. Middle scenes give the value, one point per scene.
     3. Last scene is the call to action.
     4. Each scene's on-screen text stays under the max words in `visuals.md`.
     5. Give each scene a length in seconds so the total fits the video length range in `settings.yaml`.
   - **Carousel** (use `templates/carousel.md`):
     1. Pick one layout: list, step by step, myth vs. truth, before and after, or checklist.
     2. Slide 1 is the hook: 8 words or fewer, and it makes people want to swipe to see the answer.
     3. Slide 2 says why this matters or sets up the problem.
     4. Middle slides give one point each with a short heading and 1–3 lines of text.
     5. Second-to-last slide is a quick recap of every point.
     6. Last slide is the call to action. Ask for a save or a share ("Save this for later," "Send this to someone who needs it").
     7. Aim for 7–10 slides, inside the slide count in `settings.yaml`.
   - **Static image** (use `templates/static.md`):
     1. Pick the `static_type`: tip, quote, stat, offer or testimonial.
     2. Main text: 12 words or fewer.
     3. Supporting text: 1–2 short lines.
     4. Stats need a source. Testimonials use the customer's real words, first name or initials only.
     5. Save it as one slide in `slides` and set `static_type`.
   - **Pin** (use `templates/pin.md`):
     1. Text on the pin image: 3–8 words.
     2. Title: up to 100 characters, starts with the main search word.
     3. Description: up to 500 characters, includes 2–4 search words people actually type.
     4. Link: from `settings.yaml` or `brand-kit.yaml`.
   - **Story** (use `templates/story.md`):
     1. 3–7 frames.
     2. Frame 1 is the hook.
     3. One idea per frame.
     4. Last frame is the call to action.
5. Write the caption (use `templates/caption.md`).
   1. First line is the hook, rewritten to work as text.
   2. Body gives the value in short lines.
   3. Call to action chosen from `voice.md`.
   4. Hashtags: the number set in `voice.md`, including the "always include" ones.
   5. Instagram caption: 2,200 characters max.
6. Write alt text for every image or slide: one plain sentence describing what is shown.
7. Read everything back against `voice.md` and fix anything that doesn't sound like the sample captions.
8. Check every line against `words.md` and remove anything not allowed.
9. Fill in the package's `hook`, `script` or `slides`, `caption`, `hashtags`, `cta`, `title`, `description`, `link` and `alt_text` fields.
10. Set `status: "draft"` and move the package to **03 Drafts**.
11. Repeat for every package in 02 Ideas.

## 5. Examples
Put strong hooks, scripts and captions in `examples/`. Under each one, write why it works.

## 6. Output
Post packages in 03 Drafts with `status: "draft"` and all writing fields filled in.

## 7. Checks
- [ ] Hook is 10 words or fewer.
- [ ] Sounds like the sample captions in `voice.md`.
- [ ] Nothing from the "never use" or "not allowed" lists in `words.md`.
- [ ] On-screen text is under the max words per screen.
- [ ] Caption, title and description are under platform limits.
- [ ] Hashtag count matches `voice.md`.
- [ ] Every image or slide has alt text.
- [ ] Brand words are spelled exactly as in `words.md`.
