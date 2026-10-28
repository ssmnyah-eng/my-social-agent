---
name: carousels
description: Builds carousel slide images for Instagram and Facebook from finished slide text, using the brand's colors, fonts and logo.
---

# Carousels Skill

## 1. Job
Turn carousel slide text into finished 1080 × 1350 slide images that look like the brand.

## 2. Inputs
- Post packages in **03 Drafts** with `format: "carousel"` and finished `slides`
- `brand/brand-kit.yaml` — colors, fonts, logo
- `brand/visuals.md` — text and logo rules
- `templates/slide.html` — the slide layout

## 3. Tools
- HTML slide template
- Playwright (turns each slide into an image)
- Pexels API (optional background photos)
- Google Drive (read and save)

## 4. Steps
1. Read `brand-kit.yaml` and `visuals.md`.
2. Open the next carousel package in 03 Drafts.
3. Load `templates/slide.html` and fill in the brand colors, fonts and logo from `brand-kit.yaml`.
4. Build slide 1 (the hook).
   1. Hook text large, in the heading font.
   2. Background in the primary color or a brand-style photo.
   3. A small "swipe" cue on the right edge.
5. Build each middle slide.
   1. Heading in the heading font.
   2. 1–3 lines of text in the body font.
   3. Slide number in a corner (for example "2/7").
6. Build the last slide (call to action).
   1. Call to action text large.
   2. Logo placed as described in `visuals.md`.
   3. Brand handle from `brand-kit.yaml`.
7. If a slide uses a photo, search Pexels, download it, and save the photo ID and creator to the package's `credits`.
8. Turn every slide into a 1080 × 1350 JPG named `slide-01.jpg`, `slide-02.jpg`, and so on.
9. Add the slide file names to the package's `media` field in order.
10. Leave the package in 03 Drafts with `status: "draft"` for quality-check.

## 5. Examples
Put finished carousels that look right in `examples/`. Under each one, write what makes it work.

## 6. Output
`slide-01.jpg` to `slide-NN.jpg`, 1080 × 1350, in the post package folder.

## 7. Checks
- [ ] Every slide is 1080 × 1350.
- [ ] Only brand colors and fonts are used.
- [ ] Text is at least 40 pixels from every edge.
- [ ] No text is cut off.
- [ ] Slide count matches `settings.yaml`.
- [ ] Last slide has the call to action and logo.
- [ ] Any photo used is in `credits`.
