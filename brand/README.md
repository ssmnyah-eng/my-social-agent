# Brand Folder

This folder is the only part of the agent that belongs to one brand. Every skill reads these files before it creates anything, so the agent always sounds and looks like the brand it is working for.

**Right now every file is a blank form.** Anything in `[brackets]` gets replaced when you set up a brand.

| File | What it holds |
|---|---|
| `brand-kit.yaml` | Exact values the code uses: name, handles, colors, fonts, logo files, links |
| `voice.md` | How the brand sounds |
| `visuals.md` | How the brand looks in photos, videos and graphics |
| `audience.md` | Who the content is for |
| `pillars.md` | The main content themes and the content mix |
| `words.md` | Words to use, words to avoid, claims that are not allowed |
| `assets/` | Logo files, font files and licensed music |

## Setting up a brand
1. Fill in `brand-kit.yaml`.
2. Fill in every `[bracket]` in the five `.md` files.
3. Put the logo files in `assets/` using the file names in `brand-kit.yaml`.
4. Put the font files in `assets/fonts/`.
5. Put licensed music in `assets/music/` (only music you have the rights to use).
6. Delete any example lines you did not use.
