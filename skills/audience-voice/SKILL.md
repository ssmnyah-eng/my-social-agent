---
name: audience-voice
description: Finds the exact words the brand's customers use about their problems, wants and doubts, and saves them as a phrase bank that research and scripts write from. Runs after intake and again once a month.
---

# Audience Voice Skill

## 1. Job
Learn how the audience really talks, in their own words, so hooks and captions sound like something they'd say, not like marketing.

## 2. Inputs
- `brand/audience.md` — who the audience is
- `brand/words.md` — claims and names that are not allowed
- Competitors from the intake answers in **01 Research**
- The last phrase bank, if there is one (`brand/phrase-bank.md`)
- `templates/phrase-bank.md`

## 3. Tools
- Web search and web fetch
- Claude (reading and sorting)
- Google Drive (read and save)

## 4. Steps
1. Read `audience.md` and `words.md`.
2. Collect real words from real customers. Use only places where customers write in their own words:
   1. Google and Yelp reviews of the brand and its competitors (5-star and 1–3 star).
   2. Reddit threads and forums where the audience asks for help.
   3. Comments on competitors' most popular posts.
   4. "People also ask" questions on Google for the brand's main topics.
   5. Reviews the brand pasted into the intake form.
3. Copy each phrase exactly as written. Do not fix spelling or grammar.
4. Save every phrase with its source link.
5. Sort the phrases into the groups in `templates/phrase-bank.md`:
   1. Pains: how they describe the problem.
   2. Wants: how they describe the result they want.
   3. Doubts: why they hesitate to buy or trust.
   4. Questions: what they ask, word for word.
   5. Their words: slang, nicknames and terms they use for things.
   6. Words they don't use: industry terms the brand uses that customers never say.
6. Mark the phrases that show up again and again. These are the strongest.
7. Under each group, write 3 hook starters that use the audience's own words.
8. Remove any phrase that names a private person or includes personal details.
9. Save the result to `brand/phrase-bank.md` and a dated copy to **01 Research** as `phrase-bank_YYYY-MM-DD.md`.
10. On monthly runs, add new phrases, keep the repeated ones, and drop phrases that no longer show up.

## 5. Examples
Put a finished phrase bank in `examples/` with notes on which phrases turned into strong hooks.

## 6. Output
- `brand/phrase-bank.md`
- `phrase-bank_YYYY-MM-DD.md` in 01 Research

## 7. Checks
- [ ] Every phrase is copied exactly and has a source link.
- [ ] Every group has at least 5 phrases.
- [ ] Repeated phrases are marked.
- [ ] No private names or personal details.
- [ ] Nothing breaks `words.md`.
