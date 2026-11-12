---
name: outreach-writer
description: Write a subject line and personal note for candidate outreach, based only on verifiable facts from their profile. Use for the first message and the follow-up in an outreach sequence, once a candidate has passed screening.
argument-hint: [candidate-profile-info]
---

# Outreach Writer

Generic recruiter openers get ignored. This skill writes a subject line and a personal note from specific, verifiable details in a candidate's profile — never from a guess dressed up as a compliment.

## What This Produces

Two things, for two different messages:
1. **Subject line** — under 10 words, for the first outreach email
2. **Personal note** — one or two sentences, for the follow-up email body

They must reference **different details**. If the subject line uses a career move, the note should use something else — education, a skill, a career pattern.

## Only Use Reliable Data Points

1. Previous employer (their prior company, if it's genuinely different from the current one)
2. Education (school name)
3. Current title (Team Lead, Staff, Founding Engineer, etc.)
4. A specific, interesting skill (Rust, Go, Kubernetes, Kafka, Scala, and similar)

## Never Use Interpreted or Guessed Data

- Years at a company, unless the dates are explicitly stated and current
- Specific achievements or projects that were summarized or inferred rather than quoted
- Tenure claims like "5+ years" unless it's directly stated
- Anything that reads like an assumption dressed as a fact

## Validation Rules — check every draft against these

1. **No em dashes.** Never use "—". Use a period or a comma instead.
2. **No duplicate companies.** If the "previous" and "current" company are the same entity under different names (a rebrand, an acquisition, a product name vs. the parent company), don't use a "company transition" framing — pick education, title, or skills instead.
3. **Clean company names.** Strip corporate suffixes — Ltd, Inc, Corp, Technologies, Labs, Group, Solutions, .io — and use the name people actually say out loud.
4. **Same parent company counts as one company.** If someone moved between a product and its parent company (an acquired startup and its acquirer, for example), that's not a transition — treat it as staying put.

## Priority Order for the Subject Line

1. A notable previous company — only if genuinely different from the current one
2. A notable school
3. An interesting title (Team Lead, Staff, Founding Engineer, Architect)
4. Any previous company, as a fallback — only if different from current
5. An interesting or unusual skill
6. Generic, based on the current company, as a last resort

## Never Use (instant rewrite)

- Em dashes
- "I hope this message finds you well"
- "I came across your profile"
- "I was impressed by"
- "I noticed"
- "Reaching out because"
- Any opener that could apply to literally anyone

## React or Ask. Never Recite the CV.

The most common failure: an opener that reads the person's resume back to them. "5 years at [Company] building payments infrastructure is impressive" tells them nothing they don't know. A good opener does one of two things:
- **Reacts** to something specific, the way a person who knows the field would ("Moving payments to a new provider without downtime is rare to see done well.")
- **Asks** a real question about it ("How did the move from [big company] to a 30-person team feel?")

**Banned shape:** "[X years] at [Company] doing [thing] ... is [judgment]". Rewrite any draft that fits it.

**One question at most, and not in every opener.** The email doesn't wait for the answer. In a batch, use a question in at most a third of the openers. Test each question: would it fit someone with a completely different history? If yes, it's generic. Rewrite.

**Never negative about the candidate.** No "despite", no "even though your current role is narrow", no hint that their move was a step down or their career is unusual in a bad way. One word of judgment loses the reply.

**The opener is the hook, not the introduction.** Who you are and what the role is go in the rest of the email. The opener is only about them.

## Show Three Before You Write Fifty

Before writing a whole batch, write 3 examples and show them to the person who will send them. Tone problems are cheap to fix at 3 and expensive at 50. Once a batch is written, read it as one list: if five openers share the same shape or the same first word, rewrite until they don't.

## Subject Line Examples

Based on a company move: "Snyk to Wilco?" · "Vimeo to Ultima Genomics?" · "Google to Foretellix?"

Based on education: "Technion grad at [company]?" · "TAU CS at [company]?" · "Hebrew U grad at [company]?"

Based on title: "Still hands-on as lead?" · "Founding engineer at [company]?" · "From manager back to IC?"

Based on skills: "Rust in production?" · "Go and K8s at scale?" · "Kafka at [company]?"

## Personal Note — Rules

- Pick a **different** angle than the subject line used.
- Reference something concrete, not a vague compliment.
- Vary the format between messages — don't reuse the same template every time.
- Ask a genuine question, or give a specific compliment. Not both, not neither.

## Personal Note Examples, by Angle

**Company transitions:** "From [prev]'s scale to a 20-person team is a real change. How is the pace?" · "Curious what drew you from [prev] to the startup world."

**Education:** "Technion is no joke. How do you apply that rigor at work?" · "TAU CS is competitive. What area grabbed your interest?"

**Title / leadership:** "Leading and coding is a balancing act. How do you split your time?" · "Tech lead who still builds, that's rare. How do you make time?"

**Skills:** "Rust in production is still rare. How's adoption going with the team?" · "K8s at scale gets complex. What's your approach?"

**Career path:** "First employee at a startup is intense. What was the wildest part?" · "Back to hands-on after managing. What do you enjoy most about building again?"

**Unique backgrounds:** "[Non-tech field] to engineering is unique. How does that background help?"

## Output Format

```
Subject: [subject line]
Note: [personal note]
```

Run this only on candidates who already passed the **Candidate Screener** skill. Writing a great opener for the wrong person is wasted effort.
