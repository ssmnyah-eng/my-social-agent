---
name: static-posts
description: Builds single-image posts (quote, tip, stat, offer and testimonial graphics) for Instagram and Facebook from finished post text, using the brand's colors, fonts and logo.
---

# Static Posts Skill

## 1. Job
Turn a static post's text into one finished 1080 × 1350 image that stops the scroll and looks like the brand.

## 2. Inputs
- Post packages in **03 Drafts** with `format: "image"` and finished `slides` (one slide)
- `brand/brand-kit.yaml` — colors, fonts, logo
- `brand/visuals.md` — style, text and logo rules
- Brand photos in `brand/assets/` or the brand's Drive folder
- `templates/static.html` — the layout

## 3. Tools
- HTML template
- Playwright (turns the page into an image)
- Pexels API (optional background photos)
- Google Drive (read and save)

## 4. Steps
1. Read `brand-kit.yaml` and `visuals.md`.
2. Open the next image package in 03 Drafts.
3. Pick the layout from the package's `static_type`:
   - **tip**: big heading, 1–2 lines of text below
   - **quote**: large quote text, name under it
   - **stat**: one big number, one line explaining it, source in small text
   - **offer**: offer name, price or deal, call to action
   - **testimonial**: customer's words, first name or initials only, star rating
4. Load `templates/static.html` and fill in the brand colors, fonts and logo.
5. Background.
   1. Use a real brand photo first if one fits.
   2. If not, use a brand color or a Pexels photo in the style from `visuals.md`.
   3. Put a dark or light layer over photos so the text is easy to read.
6. Text.
   1. Main text no more than 12 words.
   2. Main text large enough to read on a phone without tapping (at least 64 pixels).
   3. At least 80 pixels from every edge.
7. Put the logo where `visuals.md` says.
8. If a photo from Pexels is used, save its ID and creator to `credits`.
9. Save the image as `image-01.jpg` (1080 × 1350) and add it to `media`.
10. Leave the package in 03 Drafts with `status: "draft"` for quality-check.

## 5. Examples
Put one finished image of each layout in `examples/` with a note on why it works.

## 6. Output
`image-01.jpg`, 1080 × 1350, in the post package folder.

## 7. Checks
- [ ] Image is 1080 × 1350.
- [ ] Main text is 12 words or fewer and easy to read on a phone.
- [ ] Only brand colors and fonts are used.
- [ ] Testimonials use real customer words with first name or initials only.
- [ ] Stats show their source.
- [ ] Any Pexels photo is in `credits`.
