---
name: stories
description: Builds Instagram and Facebook story frames from finished story text, using the brand's colors, fonts and logo.
---

# Stories Skill

## 1. Job
Turn story text into a set of finished 1080 × 1920 story frames.

## 2. Inputs
- Post packages in **03 Drafts** with `format: "story"` and finished frame text
- `brand/brand-kit.yaml` — colors, fonts, logo
- `brand/visuals.md` — text rules
- `templates/story.html` — the story layout

## 3. Tools
- HTML story template
- Playwright (turns each frame into an image)
- Pexels API (optional background photos or clips)
- Google Drive (read and save)

## 4. Steps
1. Read `brand-kit.yaml` and `visuals.md`.
2. Open the next story package in 03 Drafts.
3. Load `templates/story.html` and fill in brand colors and fonts.
4. Build each frame.
   1. Frame text in the heading font.
   2. Background in a brand color or a brand-style photo.
   3. Text inside the safe area: not in the top 250 pixels or bottom 340 pixels.
5. Polls, question boxes and link stickers cannot be added by the posting tools. Write any question as text on the frame instead, for example "Reply and tell me ___".
6. Put the logo small on the last frame.
7. Turn each frame into a 1080 × 1920 JPG named `story-01.jpg`, `story-02.jpg`, and so on.
8. If a photo was used, save its ID and creator to `credits`.
9. Add the frame file names to the package's `media` field in order.
10. Leave the package in 03 Drafts with `status: "draft"` for quality-check.

## 5. Examples
Put story sets that look right in `examples/`.

## 6. Output
`story-01.jpg` to `story-NN.jpg`, 1080 × 1920, in the post package folder.

## 7. Checks
- [ ] Every frame is 1080 × 1920.
- [ ] Text is inside the safe area.
- [ ] 3–7 frames.
- [ ] Last frame has the call to action.
- [ ] No frame depends on a sticker.
