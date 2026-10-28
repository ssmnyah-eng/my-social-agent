---
name: quality-check
description: The final gate before anything posts. Checks every draft against the brand, the platform rules, copyright and facts, then approves it, sends it back to be fixed, or holds it for review.
---

# Quality-Check Skill

## 1. Job
Make sure nothing posts unless it is on-brand, correct, safe to use and built to each platform's rules. Because posting is automatic, this skill decides what goes out.

## 2. Inputs
- Post packages in **03 Drafts**
- Every file in `brand/`
- `config/settings.yaml` — limits, schedule, platforms
- Packages in **06 Posted** from the last 30 days
- `templates/checklist.md`

## 3. Tools
- Claude (reading and judging)
- FFprobe (checking video files)
- Image checks (size and format)
- Link checker (makes sure links open)
- Google Drive (read and move)

## 4. Steps
1. Open the next package in 03 Drafts.
2. Run every check in `templates/checklist.md` and record pass or fail with a reason in the package's `checks` field.
3. Brand checks.
   1. Writing sounds like the sample captions in `voice.md`.
   2. Nothing from the "never use," "not allowed" or "names never to mention" lists in `words.md`.
   3. Brand words spelled exactly right.
   4. Only brand colors and fonts in the media.
   5. Logo used the way `visuals.md` says.
4. Fact checks.
   1. Every fact, number or quote has a source in the package.
   2. Every quote is checked word for word against its source and has the right person's name.
   3. No health, money or legal promises.
5. Rights checks.
   1. Every stock clip and photo is listed in `credits`.
   2. Music is only from `brand/assets/music/`.
   3. No clips or images taken from other creators, TV, movies or YouTube.
6. Platform checks.
   1. Media size is right for the format (Reel and story 1080 × 1920, carousel 1080 × 1350, pin 1000 × 1500).
   2. Video length is inside the range in `settings.yaml`.
   3. Caption, title and description are under platform limits.
   4. Hashtag count matches `voice.md`.
   5. Alt text is there for every image.
7. File checks.
   1. Every file in `media` opens.
   2. Videos have no black or frozen sections and have sound.
   3. Every link opens.
8. Repeat check: the topic and hook are not too close to anything in 06 Posted from the last 30 days.
9. Decide.
   - **Everything passes**
     1. Pick the next open posting time for that platform from the schedule in `settings.yaml`.
     2. Put it in `scheduled_time`.
     3. Set `status: "approved"`.
     4. Move the package to **05 Approved**.
   - **Something fails that can be fixed**
     1. Write exactly what to fix in `checks`.
     2. Send it back to the skill that made that part (scripts, video, carousels, pins or stories).
     3. Run quality-check again after the fix.
     4. Allow 2 fix rounds.
   - **Still failing after 2 fix rounds, or a fact, rights or safety check fails**
     1. Set `status: "needs_review"`.
     2. Move the package to **04 Review**.
     3. Pull a backup idea from 02 Ideas so the schedule stays full.
10. Repeat for every package in 03 Drafts.

## 5. Examples
Put examples of posts that passed and posts that failed (with the reason) in `examples/`.

## 6. Output
- Approved packages in 05 Approved with `scheduled_time` set
- Packages that need a person in 04 Review
- A filled-in `checks` field in every package

## 7. Checks
- [ ] Every package in 03 Drafts has been checked.
- [ ] Nothing reaches 05 Approved with a failed check.
- [ ] Every approved package has a `scheduled_time`.
- [ ] Every package in 04 Review says why it is there.
