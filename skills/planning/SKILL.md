---
name: planning
description: Turns research ideas into a monthly content strategy and a dated content calendar, choosing which posts go on which platform and day. Runs after research and before scripts.
---

# Planning Skill

## 1. Job
Decide what the brand posts, where and when, so every week has the right mix of pillars, formats and goals, and nothing is random.

## 2. Inputs
- Post packages in **02 Ideas** with `status: "idea"`
- `brand/pillars.md` — pillars and content mix
- `brand/voice.md` — calls to action
- Intake answers in **01 Research** — goals, launches, sales, busy seasons
- `config/settings.yaml` — platforms, posts per week, posting times
- Latest `learnings.json` in **07 Reports**
- `templates/monthly-plan.md` and `templates/calendar.md`

## 3. Tools
- Claude (planning)
- Google Drive (read and save)

## 4. Steps
1. Write the monthly plan (first run of each month) with `templates/monthly-plan.md`.
   1. Pick the month's 1–2 main goals from the intake answers.
   2. List launches, sales, holidays and busy seasons this month.
   3. Set the content mix for the month from `pillars.md`. Shift it toward what worked in `learnings.json`, by no more than 10% per pillar.
   4. Set the goal mix for posts:
      - Reach (new people find the brand): reels and shareable carousels
      - Trust (people believe the brand): tips, proof, behind the scenes
      - Sales (people act): offers, testimonials, clear calls to action
   5. Save it to **01 Research** as `plan_YYYY-MM.md`.
2. Build the week's calendar with `templates/calendar.md`.
   1. Count the posts needed for each platform and format from `settings.yaml`.
   2. Pick ideas from 02 Ideas, highest score first, until the pillar mix and goal mix match the plan.
   3. Put launch and sale posts a few days before the date they're about.
   4. Don't put two posts from the same pillar back to back on the same platform.
   5. Mix formats across the week. No platform gets the same format more than 2 days in a row.
   6. Give each post a day and a posting time from `settings.yaml`.
   7. Give each post one call to action from `voice.md` that fits its goal.
3. Update each chosen package.
   1. Add `planned_date`, `goal` and `cta`.
   2. Keep `status: "idea"` so scripts picks it up.
4. Leave ideas that weren't picked in 02 Ideas as backups.
5. Save the calendar to **01 Research** as `calendar_YYYY-MM-DD.md`.
6. If approval is required in `settings.yaml`, send the calendar to the brand before scripts runs.

## 5. Examples
Put a finished monthly plan and weekly calendar in `examples/`.

## 6. Output
- `plan_YYYY-MM.md` in 01 Research (monthly)
- `calendar_YYYY-MM-DD.md` in 01 Research (weekly)
- Chosen packages in 02 Ideas with `planned_date`, `goal` and `cta` filled in

## 7. Checks
- [ ] Posts per platform and format match `settings.yaml`.
- [ ] Pillar mix matches the monthly plan.
- [ ] Every post has a goal, a day, a time and a call to action.
- [ ] Launches and sales are covered before their dates.
- [ ] No two same-pillar posts in a row on one platform.
