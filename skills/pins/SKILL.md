---
name: pins
description: Builds Pinterest pin images and fills in the pin's title, description, link and board so it can be found in Pinterest search.
---

# Pins Skill

## 1. Job
Turn pin text into a finished 1000 × 1500 pin image, ready to post to the right board with the right link.

## 2. Inputs
- Post packages in **03 Drafts** with `format: "pin"` and a finished `title`, `description` and pin text
- `brand/brand-kit.yaml` — colors, fonts, logo, website
- `brand/visuals.md` — style and text rules
- `config/settings.yaml` — which board each pillar goes to and the default link
- `templates/pin.html` — the pin layout

## 3. Tools
- HTML pin template
- Playwright (turns the pin into an image)
- Pexels API (background photos)
- Google Drive (read and save)

## 4. Steps
1. Read `brand-kit.yaml`, `visuals.md` and `settings.yaml`.
2. Open the next pin package in 03 Drafts.
3. Find a background photo.
   1. Search Pexels with words from the pin topic plus the stock footage search words in `visuals.md`.
   2. Pick a portrait photo with space for text.
   3. Save the photo ID and creator to the package's `credits`.
4. Load `templates/pin.html` and fill in brand colors and fonts.
5. Place the pin text.
   1. 3–8 words, large, in the heading font.
   2. On a text box in a brand color if the photo is busy.
   3. In the top or middle third of the pin.
6. Add the website or logo small at the bottom.
7. Turn it into a 1000 × 1500 JPG named `pin.jpg`.
8. Fill in the board.
   1. Look up the package's pillar in the `pinterest.boards` list in `settings.yaml`.
   2. Put that board ID in the package's `board` field.
9. Fill in the link if it is empty, using the default link in `settings.yaml`.
10. Add `pin.jpg` to the package's `media` field.
11. Leave the package in 03 Drafts with `status: "draft"` for quality-check.

## 5. Examples
Put pins that look right in `examples/`. Under each one, write why it would get clicks.

## 6. Output
`pin.jpg` (1000 × 1500) in the post package, with `title`, `description`, `link` and `board` filled in.

## 7. Checks
- [ ] Image is 1000 × 1500.
- [ ] Pin text is 3–8 words and easy to read.
- [ ] Title is 100 characters or fewer.
- [ ] Description is 500 characters or fewer.
- [ ] Link is filled in.
- [ ] Board is filled in.
- [ ] Photo is in `credits`.
