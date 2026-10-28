---
name: reporting
description: Pulls results for every posted piece of content, finds what worked and what didn't, writes the weekly report, and saves learnings the research skill uses next week.
---

# Reporting Skill

## 1. Job
Measure every post, explain what the numbers mean, and feed the lessons back into next week's research.

## 2. Inputs
- Packages in **06 Posted** from the last 30 days
- Last week's report in **07 Reports**
- `brand/pillars.md` — to group results by pillar
- `templates/weekly-report.md`

## 3. Tools
- Instagram Graph API insights
- Facebook Pages insights
- Pinterest API v5 analytics
- Claude (finding patterns and writing)
- Google Drive (read and save)

## 4. Steps
1. List every package in 06 Posted from the last 30 days.
2. Pull results for each post.
   - **Instagram:** views, reach, likes, comments, saves, shares
   - **Facebook:** views, reach, reactions, comments, shares
   - **Pinterest:** impressions, saves, pin clicks, outbound clicks
3. Save the results in each package's `results` field with the date pulled.
4. Work out the engagement rate for each post: (likes + comments + saves + shares) ÷ reach.
5. Pull follower counts for each account.
6. Find the top 3 and bottom 3 posts from the last 7 days on each platform.
7. Look for patterns by:
   1. Pillar
   2. Format
   3. Type of hook
   4. Day and time posted
   5. Video length
8. Compare this week to last week's report.
9. Write the report using `templates/weekly-report.md`.
10. Save it to **07 Reports** as `report_YYYY-MM-DD.md`.
11. Save `learnings.json` to 07 Reports with:
    1. Top topics, formats and hooks
    2. Bottom topics, formats and hooks
    3. Best posting times
    4. What to do more of and less of next week

## 5. Examples
Put example reports in `examples/`.

## 6. Output
- `report_YYYY-MM-DD.md` in 07 Reports
- `learnings.json` in 07 Reports
- `results` filled in for every recent post

## 7. Checks
- [ ] Every post from the last 7 days has results.
- [ ] Engagement rate is worked out the same way for every post.
- [ ] Every "do more" or "do less" is backed by a number in the report.
- [ ] `learnings.json` is saved for the research skill.
