---
name: engagement
description: Reads new comments and messages, replies to simple ones in the brand's voice, hides spam, and flags anything sensitive for a person to handle.
---

# Engagement Skill

## 1. Job
Keep up with comments and messages so people get answers in the brand's voice, while anything sensitive goes to a person.

## 2. Inputs
- Packages in **06 Posted** from the last 14 days
- `brand/voice.md` — tone and sample captions
- `brand/words.md` — words and claims not allowed
- `brand/audience.md` — common questions
- `config/settings.yaml` — which reply types are automatic
- `templates/replies.md` — approved answers to common questions

## 3. Tools
- Instagram Graph API (comments, replies, hiding comments, messages)
- Facebook Pages API (comments, replies, messages)
- Claude (sorting and writing replies)
- Google Drive (save the engagement log)

## 4. Steps
1. Pull new comments on every post from the last 14 days.
2. Pull new direct messages.
3. Sort each one into a type:
   1. **Question** — asks something the brand can answer
   2. **Compliment** — positive comment
   3. **Spam** — links, bots, scams, unrelated selling
   4. **Complaint** — unhappy customer or problem
   5. **Sensitive** — health, legal, money, personal crisis, anger, threats
4. Handle each type.
   - **Question**
     1. Look for the answer in `templates/replies.md`.
     2. If it is there and question replies are automatic in `settings.yaml`, reply in the brand's voice.
     3. If it is not there, add it to the review list.
   - **Compliment**
     1. If compliment replies are automatic, reply with a short thank-you in the brand's voice.
     2. Don't use the same reply twice in a row.
   - **Spam** — hide the comment.
   - **Complaint** — don't reply, add it to the review list.
   - **Sensitive** — don't reply, add it to the review list marked urgent.
5. Check every reply against `words.md` before sending.
6. Reply to messages only within the platform's reply window.
7. Save the engagement log to **07 Reports** as `engagement_YYYY-MM-DD.md` with:
   1. Replies sent
   2. Comments hidden
   3. Review list, urgent items first
8. Add any new common question to the "needs an approved answer" section of `templates/replies.md`.

## 5. Examples
Put example comments with good replies in `examples/`.

## 6. Output
- Replies posted
- Spam hidden
- `engagement_YYYY-MM-DD.md` with the review list

## 7. Checks
- [ ] No reply to complaints or sensitive comments.
- [ ] Every reply sounds like `voice.md`.
- [ ] No reply breaks `words.md`.
- [ ] No promises about refunds, results or health.
- [ ] Every urgent item is at the top of the review list.
