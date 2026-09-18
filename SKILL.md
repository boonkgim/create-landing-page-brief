---
name: create-landing-page-brief
description: Interview the user one question at a time, then write a high-conversion landing page copy brief (copy only, no layout). Use when the user wants a landing page brief, sales page copy, or website copy plan.
---

# Create Landing Page Brief

Produce a **copy brief** for a high-converting landing page. Copy only — headlines, subheads, body, CTA labels, section order and intent. **Never specify layout, visual design, components, grids, colors, or typography.** A separate design skill owns that. You may note *what a visual must communicate* (e.g. "product screenshot showing the inbox at zero"), never how it should look.

## Core principle

A high-converting page is one continuous argument from top to bottom. Each section answers the next question in the visitor's head, in the order the question blocks them. Every line must earn the scroll to the next one.

Every landing page asks a stranger to give up something scarce. The currency changes (money, an email, an hour, switching cost, the reputational risk of associating with you); the argument does not. Know what you are asking for before you write a word.

## Process

### 1. Interview — one question at a time

Ask **exactly one question per message.** Never batch. Never present a form. Wait for the answer, let it shape the next question, and keep going until you can fill every section without inventing anything.

Rules:
- Keep each question short and concrete. Give a worked example or 2–3 options when it helps the user answer fast.
- Dig when an answer is vague or generic ("saves time" → "how much time, for whom, measured how?").
- Push for the visitor's *own words* — quotes from sales calls, support tickets, reviews, DMs. Verbatim language beats your paraphrase.
- Push for specifics over adjectives: numbers, names, timeframes, before/after.
- If the user doesn't have something (no testimonials yet, no pricing), say so plainly, mark it as a gap, and move on. Do not stall.
- Track what you already know. Never re-ask.

Open with these three, in order, because they select the archetype and the vocabulary for everything after:
1. What is this page for, and what's the product/person/project name?
2. What's the single action you want a visitor to take?
3. What does taking that action cost them — money, an email, time, setup effort, switching from what they use now, or putting their name next to yours?

Then work through, adapting to the archetype reference (step 2):
4. Who exactly is this for, and who is it *not* for?
5. What is that person struggling with right now, in their words?
6. What do they do instead today, and why does it fall short?
7. What changes for them afterwards — the outcome, not the feature?
8. How does it work, in three steps from where they are to the result?
9. Why should they believe you — proof, credentials, numbers, mechanism?
10. What proof exists — logos, users, ratings, results, named testimonials?
11. What's the #1 reason people say no, and what do you say back?
12. What exactly do they get, what does it cost, and what happens in the first minute after they act?
13. What risk can you take off their plate — guarantee, trial, no card, cancel anytime, unsubscribe anytime?
14. What are the 5–6 real questions people ask before they act?
15. Is there a genuine reason to act now — deadline, cohort, limited seats, price change?
16. What tone should this sound like, and is there a page whose voice you'd want to match?

Before you stop asking, run this check and ask about anything missing: target reader, primary action, what it costs them, pain in their words, mechanism, outcome, proof, top objection, the ask, de-risking, urgency, tone.

### 2. Pick the archetype

Decide early, from the answer to question 1, and **read the matching reference before continuing the interview** — it changes which questions matter and what the sections are called.

| The page is for | Read |
| --- | --- |
| A person: consultant, coach, creator, founder, freelancer, speaker | `references/personal-brand.md` |
| A business: a product or service sold as the solution to a problem | `references/business.md` |
| Anything else | Derive it (below), borrowing from whichever reference is closer |

Ask the user to confirm if it is genuinely ambiguous (a solo consultant selling a productized service can go either way, and the difference is whether the person or the offer is the thing being trusted). Otherwise just pick and say which you picked.

**Deriving an archetype on the fly.** For anything the two references don't cover (a newsletter, a donation page, an open-source project, an event, a job posting, a research lab), do not force the default stack. Derive it:

1. Write down the single ask and what it costs the visitor.
2. List the questions that visitor must have answered before they will act, in the order each one blocks them. Use their language.
3. One section per question. Order the sections by when the question blocks.
4. Check the result against the default stack below, and against the closer reference. Add anything genuinely missing; **cut any section you have no real answer for** rather than filling it. A section of filler costs more than a missing section.
5. Name the sections in the user's domain language, not generic labels.
6. State the derivation in the brief: the archetype, the ask, the currency, and one line per section explaining what question it answers.

### 3. Default section stack

The baseline both references adapt. For each section write: **job** (one line), then the **actual copy** — headline, subhead, body, CTA label, microcopy. Write finished copy, not descriptions of copy.

1. **Hero** — headline, subhead, one CTA, note on what the visual must show. Job: say what this is, who it's for, and the outcome or problem solved.
2. **Proof bar** — logos, counts, ratings, one hard stat. Job: buy credibility cheaply before attention is invested.
3. **Problem** — name the pain in the visitor's own words. Job: prove you understand, so the solution lands as relevant rather than generic.
4. **Solution / How it works** — usually three steps. Job: kill the fear of complexity; show the path from where they are to the result.
5. **Benefits** — outcomes, not specs. Job: show what their life or work looks like afterwards.
6. **Features / proof of mechanism** — the specifics behind the claims. Job: give the skeptical reader something concrete to verify.
7. **Testimonials / case studies** — named people, specific results. Job: let someone like them say it instead of you. Strongest right before an ask.
8. **Objection handling / Why us** — comparison, "is this for you / not for you", or a why-us section. Job: surface the doubts they'd otherwise leave to go research.
9. **The ask** — what they get, what it costs, what happens next. Job: remove ambiguity, the most common silent killer of conversions.
10. **De-risking** — guarantee, trial, no card, easy cancellation. Job: move the perceived risk from them to you.
11. **FAQ** — the five or six real questions people ask before acting. Job: catch the last hesitations without cluttering the flow.
12. **Final CTA** — a clean repeat of the hero ask plus the single strongest reason to act now. Job: convert the person who read the whole page.

### 4. Write the brief

Output a markdown file at `landing-page-brief.md` in the working directory (or wherever the user asks):

- **Page summary** — what this is, audience, primary action, what it costs the visitor, secondary action, tone.
- **Archetype** — which one, and any adaptation you made to its stack, one line of reasoning each.
- **Positioning line** — one sentence: for [who] who [pain], [name] is the [category] that [outcome], unlike [alternative].
- **Sections** — in order, each with job + finished copy.
  - **3 headline options** for the Hero, recommendation marked, one line on why.
  - The **exact CTA label** everywhere a CTA appears, worded consistently across the page.
- **Visual notes** — per section, what a visual must *communicate*. No styling.
- **Gaps** — anything the user couldn't supply, flagged as `NEEDS: ...` so nothing is silently invented.

## Copy rules

- Specific beats clever. Concrete nouns and numbers beat adjectives.
- Write for a busy skimmer. Short sentences. No throat-clearing.
- Second person. Active voice. Lead every section with the payoff.
- No claim the user didn't give you. No invented stats, logos, names, or quotes — flag as `NEEDS:` instead.
- Testimonials must be verbatim. Never write a quote for a real named person.
- One primary CTA for the whole page. Don't dilute it with competing asks.
- Headlines: say the outcome, not the category. Cut any word that could be deleted without loss.
