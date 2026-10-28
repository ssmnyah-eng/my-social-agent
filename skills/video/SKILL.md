---
name: video
description: Builds short vertical videos (Reels and video pins) from a finished script using free stock footage, the brand's fonts and colors, on-screen text, logo end card and licensed music.
---

# Video Skill

## 1. Job
Turn a reel script into a finished 9:16 video that looks like the brand.

## 2. Inputs
- Post packages in **03 Drafts** with `format: "reel"` and a finished `script`
- `brand/brand-kit.yaml` — colors, fonts, logo files
- `brand/visuals.md` — style, stock footage search words, text and logo rules
- `brand/assets/` — fonts, logo, music
- `config/settings.yaml` — video length range
- `clip-log.json` — stock clips already used

## 3. Tools
- Pexels API (free stock video)
- FFmpeg (cutting, resizing, text, music, export)
- Google Drive (read and save)

## 4. Steps
1. Read `brand-kit.yaml` and `visuals.md`.
2. Open the next reel package in 03 Drafts.
3. Find footage for each scene.
   1. Write 2–4 search words from what the scene shows.
   2. Add 1–2 of the stock footage search words from `visuals.md`.
   3. Search Pexels for videos with portrait orientation.
   4. Skip any clip that is shorter than the scene, lower than 1080 wide, or already in `clip-log.json` from the last 30 days.
   5. Pick the clip that best matches the scene and the mood in `visuals.md`.
   6. Download it.
   7. Save the Pexels clip ID, creator name and link to the package's `credits` and to `clip-log.json`.
4. Prepare each clip.
   1. Resize and crop to 1080 × 1920.
   2. Cut to the scene's length in seconds.
   3. Remove the clip's own sound.
5. Add the on-screen text to each clip.
   1. Use the heading font from `brand-kit.yaml`.
   2. Use the text colors and text background box from `visuals.md`.
   3. Keep text inside the safe area: not in the top 250 pixels or bottom 400 pixels, and at least 60 pixels from each side.
6. Join the clips in scene order.
7. Add the logo end card.
   1. Brand background color.
   2. Logo from `brand-kit.yaml`, centered.
   3. 1.5 seconds long.
8. Add music.
   1. Pick a track from `brand/assets/music/` that fits the music style in `visuals.md`.
   2. Cut it to the video length and fade out over the last second.
   3. Set the volume from `visuals.md`.
9. Export the video.
   1. MP4, H.264 video, AAC audio.
   2. 1080 × 1920, 30 frames per second.
10. Make the cover image.
    1. Take the clearest frame from scene 1.
    2. Add the hook text in the brand's heading font.
    3. Save as a 1080 × 1920 JPG.
11. Add the video and cover file names to the package's `media` field.
12. Leave the package in 03 Drafts with `status: "draft"` for quality-check.

## 5. Examples
Put finished videos that look right in `examples/`. Under each one, write what makes it on-brand.

## 6. Output
In the post package folder:
- `video.mp4` — 1080 × 1920
- `cover.jpg` — 1080 × 1920
- `credits` filled in for every stock clip

## 7. Checks
- [ ] Video is 1080 × 1920.
- [ ] Length is inside the range in `settings.yaml`.
- [ ] Every scene has text inside the safe area.
- [ ] Text is easy to read against the footage.
- [ ] No watermarks or other logos in the footage.
- [ ] Every clip is logged with its Pexels ID and creator.
- [ ] Music comes only from `brand/assets/music/`.
- [ ] Logo end card is there.
