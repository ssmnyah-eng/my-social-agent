---
name: video
description: Hands finished reel scripts to the team's separate video editor, then picks up the finished video and checks it before quality-check. Does not edit video itself.
---

# Video Handoff Skill

## 1. Job
Give the video editor everything it needs to make each reel, then bring the finished video back into the post package. The editor is a separate tool that is already built. This skill only connects to it.

## 2. Inputs
- Post packages in **03 Drafts** with `format: "reel"` and a finished `script`
- `brand/brand-kit.yaml` and `brand/visuals.md`
- The brand's raw photos and footage in Drive
- `config/settings.yaml` — video length range and the `video_editor` section

## 3. Tools
- Google Drive (read, save and move)
- The video editor (connected later through the `video_editor` section of `settings.yaml`)
- FFprobe (checking the finished video)

## 4. Steps
1. Open the next reel package in 03 Drafts.
2. Write `edit-brief.json` in the package folder. It holds:
   1. Package ID and the video length range from `settings.yaml`.
   2. Every scene: number, seconds, on-screen text, what the scene shows.
   3. Footage to use: links to brand photos or clips in Drive that fit each scene, or search words from `visuals.md` if none fit.
   4. Brand colors, fonts and logo files from `brand-kit.yaml`.
   5. Music: a file from `brand/assets/music/`, or "none."
   6. Caption text, for burned-in captions if the editor adds them.
3. Copy the package folder to the editor's inbox folder named in `settings.yaml` (`video_editor.inbox_folder`).
4. Set `status: "editing"` in the package.
5. On every run, check the editor's outbox folder (`video_editor.outbox_folder`) for finished videos.
6. For each finished video:
   1. Check it with FFprobe: 1080 × 1920, length inside the range, has sound, plays all the way through.
   2. If it passes, save it as `video.mp4` in the package, add it to `media`, add a cover image as `cover.jpg`, and set `status: "draft"` so quality-check picks it up.
   3. If it fails, write what's wrong in `checks` and send it back to the editor's inbox. Allow 2 rounds, then move the package to **04 Review**.
7. If a package has been in `editing` longer than `video_editor.max_wait_hours`, move it to 04 Review and pull a backup idea so the schedule stays full.

## 5. Examples
Put a finished `edit-brief.json` and the video that came back in `examples/`.

## 6. Output
- `edit-brief.json` in each reel package sent to the editor
- Finished `video.mp4` and `cover.jpg` back in the package, `status: "draft"`

## 7. Checks
- [ ] Every reel package sent out has a full `edit-brief.json`.
- [ ] Every video that comes back is 1080 × 1920, inside the length range, and has sound.
- [ ] No package waits in `editing` past the time limit.
