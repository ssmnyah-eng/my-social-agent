---
name: intake
description: Sets up a new brand. Sends the intake form, turns the answers into the filled-in brand files and settings, and lists anything still missing. Runs once per brand, before any other skill.
---

# Intake Skill

## 1. Job
Collect everything the agent needs to know about a new brand, then fill in the `brand/` files and `config/settings.yaml` so every other skill can run.

## 2. Inputs
- `templates/intake-form.md` — the questions the brand answers
- The brand's answers (pasted in, or the filled-in form saved in **01 Research**)
- The brand's website and current social accounts
- Logo files, fonts and photos the brand sends

## 3. Tools
- Claude (reading and writing)
- Web search and web fetch (reading the brand's site and accounts)
- Google Drive (read and save)

## 4. Steps
1. Send the brand `templates/intake-form.md` and ask them to answer every question.
2. When the answers come back, read them all once before writing anything.
3. Read the brand's website and last 30 posts on each account they gave.
   1. Write down how they already talk: words, emojis, sentence length.
   2. Copy 3 captions that sound most like them for `voice.md`.
   3. Write down their colors and fonts if the answers left them out.
4. Fill in the brand files from the answers.
   1. `brand-kit.yaml`: name, tagline, website, handles, colors, fonts, logo file names.
   2. `voice.md`: what they do, personality, how they sound, always, never, sample captions, calls to action, hashtags.
   3. `audience.md`: who they are, wants, struggles, beliefs, reasons they might not buy, questions they ask, where they spend time.
   4. `pillars.md`: 3–4 pillars from their goals and offers, content mix, off-limits topics.
   5. `words.md`: brand words and spellings, words to avoid, claims not allowed, names never to mention.
   6. `visuals.md`: style, photo and footage search words, text and logo rules.
5. Fill in `config/settings.yaml`.
   1. Turn on only the platforms they said yes to.
   2. Set posts per week and posting times from their answers.
   3. Set `approval_required` to what they chose.
6. Put the logo, font and photo files they sent into `brand/assets/`.
7. Make the 7 Drive folders for the brand and add the folder IDs to `settings.yaml`.
8. Write `intake-gaps.md` in 01 Research listing every `[bracket]` still empty and the question to ask to fill it.
9. Do not make up answers. If something wasn't answered and can't be found on their site or accounts, leave it in `intake-gaps.md`.

## 5. Examples
Put a finished intake form and the brand files it produced in `examples/`.

## 6. Output
- Filled-in `brand/` files and `config/settings.yaml`
- Brand files in `brand/assets/`
- `intake-gaps.md` in 01 Research

## 7. Checks
- [ ] Every answer from the form landed in the right file.
- [ ] Nothing in the brand files was made up.
- [ ] Sample captions are real captions from the brand.
- [ ] Only the platforms they said yes to are turned on.
- [ ] Content mix in `pillars.md` adds up to 100.
- [ ] Every empty bracket is listed in `intake-gaps.md`.
