---
name: talent-sourcer
description: Turn a job description into a tiered set of boolean search strings and sourcing filters (LinkedIn Recruiter, Sales Navigator, or any ATS/sourcing tool). Use once you have a market research brief and need to actually build searches.
argument-hint: [job-description-or-market-research-brief]
---

# Talent Sourcer

A single search string never covers a role properly. This skill builds a tiered set of searches, from tight to loose, so you find both the obvious candidates and the ones a single narrow search would miss entirely.

## Step 1: Analyze the Role

Pull out, explicitly:
1. **Core title** — what the role is actually called
2. **Adjacent titles** — what similar roles are called at other companies (titles are not standardized; a "DevOps Team Lead" somewhere else might be an "SRE Lead" or "Platform Engineering Manager")
3. **Seniority level** — IC, senior, team lead, manager, director
4. **Must-have skills or stack** — the non-negotiables
5. **Location** — and how flexible it actually is
6. **Industry or domain preference**, if any

## Step 2: Build Tiers, Tight to Loose

Don't run one search. Build several, ordered from narrow to broad, and only move down a tier if the tighter ones aren't yielding enough qualified people.

**Tier 1 — Exact match (tightest).** Exact title + required seniority + location. This is your highest-precision, lowest-volume search.

**Tier 2 — Title expansion.** Same seniority and location, broader title variations and known synonyms (see the expansion table below).

**Tier 3 — Adjacent roles.** Related roles that could realistically transition into this one, even without an exact title match.

**Tier 4 — Loosened seniority** (only if 1-3 aren't enough). Drop the seniority filter, or widen it — a strong senior IC might be ready to step up.

**Tier 5 — Skill-based** (only if still short). Search by required skills instead of title. Useful when the title landscape for a domain is genuinely inconsistent.

## Title Expansion Reference

Titles for the same function vary a lot between companies. Use this as a starting map, not a fixed rule — always sanity-check against the actual role.

| Role Family | Search Terms to Include |
|---|---|
| DevOps / Platform | DevOps, SRE, Site Reliability, Platform Engineer, Infrastructure |
| Backend | Backend, Server, API, Microservices |
| Frontend | Frontend, Front-end, UI Engineer, React, Web |
| Full Stack | Full Stack, Fullstack, Full-Stack |
| Data | Data Engineer, Data Platform, Analytics Engineer, ETL |
| ML / AI | Machine Learning, ML Engineer, AI Engineer, Deep Learning |
| Security | Security Engineer, AppSec, InfoSec, Cyber |
| Mobile | iOS, Android, Mobile, React Native, Flutter |
| QA | QA, SDET, Test Engineer, Quality, Automation Engineer |
| Management | Engineering Manager, R&D Manager, VP Engineering, CTO |

## Seniority Mapping

| Target Role Level | Include These Seniority Signals |
|---|---|
| Junior/Mid IC | Entry, Senior |
| Senior IC | Senior |
| Team Lead | Senior, Manager |
| Manager | Manager, Director |
| Director+ | Director, VP, C-level |

## Step 3: Write the Boolean Strings

Aim for around 12 distinct search strings per role, each targeting a different candidate persona, not 10 variations of the same search:

- 2 strings for exact title matches (narrow)
- 2 strings for broader title variations (medium)
- 2 strings for senior ICs who look ready to step up (medium)
- 2 strings for domain- or industry-specific candidates (medium)
- 1 string for passive candidates showing leadership signals without the title yet (broad)
- 1 string for people currently at your target companies from the market research brief (narrow but high-signal)
- 1 string for a strong title in a *past* role, whatever the current title is
- 1 string for people who *used to* work at your target companies

Use real boolean syntax — AND, OR, NOT, parentheses, "exact phrases" — and keep each string reasonably short (LinkedIn Sales Navigator and most tools have practical length limits, generally well under 500 characters).

Each string should come with the filters that go with it: title, location, industry, seniority band, company size band, and any keyword filters. Which filters exist and how they're named will depend on the specific tool you're using (Sales Navigator, an ATS's built-in search, a sourcing platform) — map the categories above onto whatever your tool actually offers.

## Write Title Phrases That Catch Everyone and Nothing Else

First check how your tool matches titles. Many tools (and LinkedIn, when you put the phrase in quotation marks) match a phrase anywhere inside the title. Test a few phrases and look at the results before you trust them.

- **Never use a bare generic word** like "Engineer", "Developer", "Manager", "Lead" or "Analyst" as a title filter. "Engineer" catches Sales Engineer, Solutions Engineer and Field Engineer too.
- **Use the tightest phrase that can only mean this role.** "Backend Engineer", "Full Stack", "Product Manager". With contains-matching, "Full Stack" also catches Senior Full Stack Developer, Full Stack Tech Lead and Full Stack Web Developer. You don't need to list seniority prefixes; they come free.
- **List every spelling.** To the tool these are different words: Full Stack / Full-Stack / Fullstack, Back End / Back-End / Backend, Tech Lead / Technical Lead, Pre-Sales / Presales.
- **Add house styles and abbreviations** when the role uses them: SWE, SDE, SRE, MLE, Member of Technical Staff.
- **Run the noise test before you commit a phrase.** Ask: would a Sales Engineer, Account Manager, Graphic Designer, Data Scientist or Recruiter pass this? If yes, the phrase is too bare. A tighter phrase is the fix; a NOT list is only a patch.

## Keywords Go Across Every Text Field, Not the Title

A keyword search on the title alone returns noise and misses the best people. If your tool lets you choose fields, spread each keyword across the headline, the summary, the skills list, and the current AND past role descriptions. Many strong people have a plain title ("Software Engineer", "Architect") and the real signal sits in what they wrote about their work.

## Every Search Round Runs Six Angles

The tiers above say how tight a search is. The angles below say *where* you look. A round that only runs one angle sees one slice of the market. Run all six, or write down why you skipped one:

1. **Current title.** A strong title in the current role, at the target companies (the companies the client named first, then your tiered list).
2. **Past title.** A strong title in a *past* role, whatever the current title is. This finds people who moved to a plain title.
3. **Past employer.** Worked at a target company before, now anywhere. This finds alumni who moved on.
4. **Best companies, any title.** Only the strongest companies, any relevant title, no keyword. This finds people whose profile has neither the exact title nor the keywords. Keep it small and let screening decide.
5. **Keywords without the title.** Strong keywords across all text fields, with a broad title.
6. **Whole market.** Strong titles, no company list. Run it last and keep it small.

**Never call a market "dry" or "used up" until all six angles have run.** One empty angle says that angle is empty, nothing more. An angle that gives zero new people two rounds in a row may be skipped next round, with that as the written reason.

**Exclude the people you already saw.** Most tools return the same top results every time unless you exclude profiles you already reviewed. Use your tool's own filter for this ("hide profiles already viewed", "exclude people already in a project"), or keep a list and exclude it on every search.

## Role-Specific Rules Stay With the Role

A precision rule that suits one role (for example "must have a hands-on engineering background") must be switched on for that role only, never made the default for every search. A forgotten switch should cost you some precision, never silently return zero candidates for every other role.

## What Makes This Work

- Don't rely on titles alone. The best candidate for a role sometimes has a title that would never surface in a naive search.
- Think about who's not actively looking. Passive candidates with the right trajectory are often better hires than active ones — build at least one search angle around leadership or ownership signals rather than job titles.
- Move down tiers deliberately. If Tier 1 gives you 200 qualified people, you don't need Tier 4. If it gives you 5, you need Tier 3 immediately.

## Output

A tiered list of search strings, each with: the persona it targets, the string itself, the filters to apply, and a rough expectation of result volume (narrow/medium/broad).

Hand qualified results to the **Candidate Screener** skill before reaching out to anyone.
