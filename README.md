# My Social Agent

An AI social media manager that researches, creates, checks, posts, and reports on content automatically. Each job the agent does is taught as a **skill**.

**This repo is a template.** Everything is built and ready except the brand. Copy it once per brand, fill in the brand and config forms, and the agent works for that brand.

## How to make a copy for a new brand
1. On this repo's GitHub page, click **Use this template → Create a new repository**.
2. Name it after the brand (for example `brandname-social-agent`) and set it to **Private**.
3. Send the brand `skills/intake/templates/intake-form.md` and run the intake agent on their answers. It fills in the `brand/` folder (see `brand/README.md`).
4. Add the brand's logo, fonts and licensed music to `brand/assets/`.
5. Fill in every `[bracket]` in `config/settings.yaml`.
6. Fill in `skills/engagement/templates/replies.md` with the brand's approved answers.
7. Add the keys listed in `config/secrets.md` to the new repo's GitHub Secrets.
8. Make the 7 Google Drive folders for the brand and put their IDs in `settings.yaml`.

## Folders

| Folder | What goes in it |
|---|---|
| `brand/` | Blank brand forms: voice, visuals, audience, pillars, words, brand kit, assets |
| `config/` | Settings and the list of secret names |
| `skills/` | One folder per skill: `SKILL.md`, `examples/`, `templates/` |
| `agent/` | The code that runs the skills in order (not written yet) |
| `.claude/agents/` | One agent per skill, ready to run in Claude Code |
| `CLAUDE.md` | The lead agent that runs the others in order |

## Skills (run in this order)

| Skill | Job |
|---|---|
| intake | Set up a new brand from the intake form (once per brand) |
| audience-voice | Collect the audience's exact words into a phrase bank (monthly) |
| research | Find topics and turn them into post ideas |
| planning | Build the monthly plan and weekly content calendar |
| scripts | Write hooks, scripts, slide text, captions, pin text, alt text |
| video | Hand reel scripts to the team's video editor and check what comes back |
| carousels | Build carousel slides |
| static-posts | Build single-image posts |
| pins | Build Pinterest pins |
| stories | Build story frames |
| quality-check | Approve, send back for fixes, or hold each post |
| posting | Publish approved posts on schedule |
| reporting | Measure results and write the weekly report |
| engagement | Reply to comments and messages, hide spam, flag sensitive ones |

How the skills pass work to each other is explained in `skills/README.md`.

## Every SKILL.md has 7 parts
1. Job
2. Inputs
3. Tools
4. Steps
5. Examples
6. Output
7. Checks

## Content library (Google Drive)
01 Research → 02 Ideas → 03 Drafts → 04 Review → 05 Approved → 06 Posted → 07 Reports

## Keys and secrets
API keys are stored in **GitHub → Settings → Secrets and variables → Actions**. They are never saved in this repo.
