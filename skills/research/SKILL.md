---
name: research
description: Finds what the brand's audience cares about right now and turns it into a ranked list of post ideas for the week. Runs first, before any content is written.
---

# Research Skill

## 1. Job
Find timely topics the audience cares about and turn them into the week's post ideas, balanced across the brand's content pillars.

## 2. Inputs
- `brand/audience.md` — who the audience is and what they ask
- `brand/pillars.md` — pillars, content mix and off-limits topics
- `brand/words.md` — claims and names that are not allowed
- `config/settings.yaml` — which platforms are on and how many posts per week
- Latest `learnings.json` in **07 Reports** — what worked and what didn't
- Packages in **06 Posted** from the last 30 days — to avoid repeats

## 3. Tools
- Web search
- Claude (thinking and writing)
- Google Drive (read and save)

## 4. Steps
1. Read `audience.md`, `pillars.md` and `words.md`.
2. Read `settings.yaml` and add up the number of posts needed this week for every platform and format that is turned on.
3. Open the latest `learnings.json` from 07 Reports.
   1. Write down the top 3 topics, formats and hooks.
   2. Write down the bottom 3 and why they did badly.
4. List every package in 06 Posted from the last 30 days so the same topic is not repeated.
5. For each pillar, search for:
   1. Topics people in this niche are talking about this week.
   2. Questions the audience is asking (forums, "People also ask," comments on similar accounts).
   3. Holidays, awareness days and seasonal moments in the next 14 days.
   4. Post formats and styles getting attention on each platform that is turned on.
6. For every finding, save the source link.
7. Save all findings to **01 Research** as `research_YYYY-MM-DD.md`.
8. Turn the findings into ideas. Each idea has:
   1. Pillar
   2. Platform
   3. Format
   4. Angle (the specific point of the post)
   5. Hook (the first line or first 3 seconds)
   6. Why now
   7. Source link
9. Remove any idea that:
   1. Is on the off-limits list in `pillars.md`.
   2. Needs a claim that `words.md` does not allow.
   3. Repeats a topic posted in the last 30 days.
10. Score each idea from 1 to 5 on:
    1. Fits the audience's wants and struggles
    2. Fits the pillar
    3. Timely
    4. Matches what worked in `learnings.json`
11. Sort ideas by total score.
12. Keep enough ideas to match the content mix percentages in `pillars.md`.
13. Keep the number of posts needed plus 20% extra as backups.
14. Save each idea as a post package with `status: "idea"` in **02 Ideas**.

## 5. Examples
Put good and weak idea examples in `examples/`. Under each one, write why it is good or weak.

## 6. Output
- `research_YYYY-MM-DD.md` in 01 Research
- One post package per idea in 02 Ideas, `status: "idea"`, with the `idea`, `pillar`, `platform`, `format` and `hook` fields filled in

## 7. Checks
- [ ] Every idea has a source link.
- [ ] Every idea fits one pillar.
- [ ] The pillar mix matches `pillars.md`.
- [ ] No idea repeats a topic from the last 30 days.
- [ ] No idea breaks `words.md` or the off-limits list.
- [ ] The number of ideas equals posts needed plus 20%.
