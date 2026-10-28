---
name: posting
description: Publishes approved posts to Instagram, Facebook and Pinterest at their scheduled times, records the live link, and moves each post to Posted.
---

# Posting Skill

## 1. Job
Publish every approved post at its scheduled time on the right platform, with no manual steps.

## 2. Inputs
- Post packages in **05 Approved** with `status: "approved"` and a `scheduled_time`
- `config/settings.yaml` — accounts turned on, time zone, public media location
- GitHub Secrets — access tokens and account IDs (see `config/secrets.md`)

## 3. Tools
- Instagram Graph API (Reels, carousels, images, stories)
- Facebook Pages API (Page posts and videos)
- Pinterest API v5 (pins)
- Public media storage (gives each file a web link the platforms can download from)
- Google Drive (read and move)

## 4. Steps
1. List every package in 05 Approved whose `scheduled_time` is now or earlier.
2. For each package, confirm `status` is still `"approved"`. Skip anything else.
3. Upload the package's media files to the public media storage set in `settings.yaml` and save each file's web link.
4. Post based on platform and format.
   - **Instagram Reel**
     1. Create a media container with `media_type=REELS`, the video link, the caption plus hashtags, and the cover image link.
     2. Check the container's status every 30 seconds until it says `FINISHED`.
     3. Publish the container.
   - **Instagram carousel**
     1. Create one item container per slide image (with `is_carousel_item=true`).
     2. Create a carousel container listing those items, with the caption plus hashtags.
     3. Publish the carousel container.
   - **Instagram story**
     1. Create a media container with `media_type=STORIES` for each frame.
     2. Publish each frame in order.
   - **Facebook**
     1. Video posts go to the Page's videos with the caption.
     2. Image and carousel posts go to the Page's photos (several photos become one post).
   - **Pinterest**
     1. Create the pin with the board ID, title, description, link, alt text and image.
     2. For video pins, upload the video first, wait until it is ready, then create the pin.
5. Before posting to Instagram, check the account's publishing limit and stop for the day if it has been reached.
6. Save the platform's post ID, live link and time to the package's `posted` field.
7. Set `status: "posted"` and move the package to **06 Posted**.
8. If a post fails:
   1. Try again up to 3 times, waiting longer each time.
   2. If it still fails, set `status: "failed"`, save the error message in `posted`, and leave it in 05 Approved.
9. Write a posting log for the run: what posted, what failed and why.

## 5. Examples
Put example posting logs in `examples/`.

## 6. Output
- Posted packages in 06 Posted with the `posted` field filled in
- Failed packages left in 05 Approved with the error saved
- A posting log for each run

## 7. Checks
- [ ] Nothing posts unless its status is `"approved"`.
- [ ] Every posted package has a post ID and live link.
- [ ] Every failure has its error saved.
- [ ] No access token or key is written in any file or log.
