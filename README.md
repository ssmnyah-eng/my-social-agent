# My Social Agent

An AI social media manager that researches, creates, checks, posts, and reports on content automatically. Each job the agent does is taught as a **skill**.

## Folders

| Folder | What goes in it |
|---|---|
| `skills/` | One folder per skill. Each has a `SKILL.md` (the instructions), `examples/` and `templates/`. |
| `brand/` | Brand voice, colors, fonts, audience, content pillars, words to use and avoid. |
| `config/` | Settings: platforms, posting schedule, folder IDs. **No passwords or API keys.** |
| `agent/` | The code that runs the skills in order. |

## Skills

| Skill | Job |
|---|---|
| research | Find trends and topics |
| scripts | Write video scripts and captions |
| video | Build short videos |
| carousels | Build carousel posts |
| pins | Build Pinterest pins |
| stories | Build stories |
| quality-check | Check every post before it goes out |
| posting | Post to each platform |
| reporting | Pull results and write reports |
| engagement | Draft replies to comments and DMs |

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
