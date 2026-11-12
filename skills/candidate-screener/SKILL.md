---
name: candidate-screener
description: Screen a candidate's profile against a target role and return a clear GO or NO GO decision, with evidence. Use once you have a full profile in hand and need to decide whether to reach out.
argument-hint: [target role and must-haves/exclusions]
---

Apply the screening policy below to the candidate profile text already in the conversation, using the target role context provided in the arguments.

Requirements:
- Return one final decision only: `GO` or `NO GO`
- Never invent missing facts
- Normalize titles, technologies, and domains using the reference tables below
- Keep the output concise and evidence-based

---

# Screening Policy

For a role in Israel, also load the **israeli-tech-market** skill and apply its army, education and employer rules first.

## Minimum Data Requirement — read this first

**You need the full profile to screen someone. A title, a company name, and a couple of keywords are not enough.**

A profile is screenable when it includes: full employment history with dates, what the person actually did in each role, and their full company history — not just the current one.

If the input doesn't include this, don't issue a GO or NO GO. Say plainly: "Insufficient data — full profile required before screening," and list what's missing.

The most common screening mistake is seeing a good current company plus two or three matching keywords and approving on the spot. A title like "Full Stack" doesn't confirm backend depth. Two matching technologies in a summary don't confirm the person isn't primarily doing something else entirely. That's guessing, not screening.

## Core Approach

Screen like a careful, skeptical, senior recruiter who has seen a lot of inflated profiles. Prefer depth, scope, ownership, and real impact over titles, brand names, or keyword density. Make the call independently, with evidence, as if nobody will check it before outreach goes out.

## Final Decision

One line, binary, no hedging: `GO` or `NO GO`. Never punt the decision back to the person reading it.

## Never Invent Facts

Use only what's explicitly in the profile, plus any clearly-labeled company research. If something is missing or ambiguous, say so, lower your confidence, and decide conservatively. Never fabricate tenure, seniority, team size, scope, or impact just because it would make the story cleaner.

## Calibrate on Real Profiles Before You Trust the Rules

A screening policy written from the job description alone is a guess. Before you screen a batch, run the rules on 10-20 real profiles from your searches and read the results with the hiring manager's eyes. A verdict the hiring manager has not confirmed is a hypothesis, not calibration.

**The "reject if X is not stated" trap.** Be suspicious of any rule shaped "NO GO if the profile doesn't mention X". First check what share of real profiles mention X at all. If only a few percent do (visa status, team size, a description under the current role), the rule is not a bar, it's an off switch: it rejects nearly everyone, including your best candidates. A rubric is finished when it has passed real people you would hire, not when it is written.

**Learn from the hiring manager's rejections.** When the client turns someone down, ask why. If the reason is a real requirement of the role (not a one-off), write it as a rule, test it on a few more profiles, and re-check earlier GOs against it. The same pattern often hides in several more profiles.

## Career Trajectory — check the whole arc, not just the current role

A strong current role doesn't make up for a career that's mostly unrelated. Return `NO GO` when the candidate's history is mostly non-technical roles, an unrelated domain with no credible transferable depth, or doesn't form a coherent path leading to where they are now.

Someone who spent most of their career outside tech and recently joined a tech company is a career changer early in that path, not a senior tech professional, regardless of how good their current title looks. Always read the full history before deciding — a good current company is not a shortcut past this.

## Hard Filters — automatic NO GO if any apply

- Current tenure under the minimum agreed for this role (agree it with the hiring manager before screening; promotions inside one company count as one continuous tenure)
- Three or more roles that each lasted under 2 years
- More than 8 years at one company with no visible progression or expanded scope
- Background is mostly telecom, banking, military, or outsourcing/services, unless the search specifically targets that background
- Must-have skills are missing with no credible adjacent match
- The overall career trajectory is mostly unrelated to the target role (see above)

## Tenure Must Be Verified, Never Assumed

The minimum current tenure has to be confirmed from the dates in the profile. If the start date isn't there, that's not a reason to skip the check — it's a reason to be more careful. If current tenure can't be confirmed, flag it clearly as unverifiable and confirm it before outreach. Don't reject on missing dates alone (see the "reject if X is not stated" trap above). Missing dates on past roles lower your confidence.

## Real Seniority vs. Title

Judge actual seniority from scope, ownership, complexity, influence, recency, and evidence of hands-on work, not the title alone. Real signals: ownership of major systems or domains, architecture or delivery ownership, measurable impact, and a credible pattern of growing responsibility.

## Skills Match

Normalize titles and technologies before judging fit (see reference tables below). Count clear synonyms as direct matches. Count adjacent technologies as partial matches only when the profile shows real evidence of transferability, not just proximity. Don't reject purely because the stack isn't a perfect match if the fundamentals and transferability are strong — but don't accept a skill gap that's too large for a realistic ramp-up either.

## Startup / Environment Fit

Positive: product companies, modern stack, real career progression, hands-on ownership, evidence of shipping. Negative: legacy tech, heavy services/outsourcing experience, stagnation, maintenance-only work with weak ownership. Don't use brand prestige as a shortcut — judge the actual environment. (Use the **Company Scout** skill when the company itself is the unclear part.)

## Patterns That Fooled Us

- **Long-term solo freelancer.** Years of "Freelance Developer" or a one-person consultancy, judged only on a skills list, is a NO GO unless the profile shows real clients, real products, and a team-scale environment.
- **Israeli army service: judge the work, not the unit.** Our default: relevant technical army work (8200, Mamram and similar) counts at half weight when checking years of experience. Unit membership alone proves nothing; read what the person actually did. Some roles count relevant army work fully, so agree it with the client.
- **Company tenure vs. years of experience.** "8 years at Company X" can be a whole career path across several roles, or 8 flat years in one job. Read the roles under the company before you judge either way.
- **8+ years at one employer with no visible change of scope.** Some clients read this as "settled, not likely to move" or "narrow experience". Check progression across roles, and ask the client whether it matters for this search.
- **A thin profile at a must-have company is not an automatic NO GO.** If the title is exactly right at exactly the right company, a short profile is a reason to get the full profile and look closer, not to reject.

## The Caliber Check — the last step before any GO

Box-ticking can pass a profile that no senior recruiter would call. Before you write GO, ask one question: **would I put my name on this introduction to the hiring manager?** If you hesitate, name the requirement and the evidence behind the concern. A concern you can tie to the role is a reason for NO GO; an unexplained feeling is not.

## A Second Check on GOs

In our experience, AI screening tends to be generous: it finds reasons to say yes. When the cost of a bad outreach is real (a client sees every candidate), check every GO again, independently, against the agreed requirements (a stronger model, or a fresh session). Report supporting evidence, contradictions and missing information. Also re-check a small sample of NO GOs, because a bad rule rejects good people too.

## Decision Standard

`GO` only when outreach is genuinely justified right now. `NO GO` when a hard filter triggers, the evidence is too thin, seniority looks inflated relative to scope, the skills gap is too wide, the environment fit is poor for this specific search, or the profile is too vague to justify a recruiter's time reaching out.

## Output Format

Return exactly these sections, in this order:

1. `Final Decision: GO` or `Final Decision: NO GO`
2. `Summary:`
3. `Relevant Experience Range:`
4. `Real Seniority Assessment:`
5. `Skills Match:`
6. `Environment Fit:`
7. `Green Flags:`
8. `Red Flags:`
9. `Company Context:` (only if you looked into the company)
10. `Decision Rationale:`
11. `Confidence:`

---

# Reference: Title Synonyms

Treat these as the same broad search family for initial matching, then verify actual scope from the profile:

- Software Engineer = Software Developer
- Backend Engineer = Backend Developer = Server-Side Developer
- Frontend Engineer = Frontend Developer = Front-End Developer
- Full Stack Engineer = Full Stack Developer = Fullstack Engineer/Developer
- DevOps Engineer can overlap with Platform Engineer, Infrastructure Engineer, SRE, Site Reliability Engineer
- Data Engineer can overlap with Data Pipeline Engineer, Big Data Engineer, ETL Developer
- QA Engineer = Quality Assurance Engineer = Test Engineer
- AI Engineer = ML Engineer = Machine Learning Engineer = Applied AI Engineer
- Architect = Software Architect = Technical Architect = Systems Architect = Solution Architect
- PM defaults to Product Manager (not Project Manager) unless the profile clearly indicates delivery/program management instead of product ownership

**Broad senior-level matching family:** Senior, Experienced, Tech Lead, Principal, Staff — different companies map these differently, so match broadly first, then calibrate real level from scope and evidence.

**Leadership-heavy titles** (usually a poor fit for IC searches unless the profile shows recent, relevant hands-on execution): CTO, Founder, VP, Director, Team Leader, Group Lead, Head of Engineering, Engineering Manager, R&D Manager. Don't exclude on title alone — exclude when both the title and the actual description point to leadership scope over hands-on work. For leadership searches, these are exactly what you want.

# Reference: Technology Synonyms

Normalize common aliases before judging a skills match:

- Node.js = Node = NodeJS
- React = ReactJS = React.js
- TypeScript = TS
- JavaScript = JS = ECMAScript
- Microservices = Micro-services = SOA
- Machine Learning = ML; Artificial Intelligence = AI; Natural Language Processing = NLP; Computer Vision = CV
- Kubernetes = K8s; Terraform is one IaC (Infrastructure as Code) tool: related to other IaC tools, not the same
- LLM(s) = Large Language Model(s) = Foundation Models
- Generative AI = GenAI = Gen AI
- RAG = Retrieval-Augmented Generation
- AWS = Amazon Web Services; GCP = Google Cloud Platform / Google Cloud
- Python = Py; Go = Golang; C# = C Sharp
- Cybersecurity = InfoSec = Information Security
- SaaS = Software as a Service = B2B/B2C SaaS = SaaS Platform

Count exact synonyms as direct matches. Count adjacent technologies as partial matches only when the profile actually shows the transferability, not just relatedness.

# Reference: Buzzwords vs. Real Signals

**Weak buzzwords that don't justify fit by themselves:** passionate engineer, results-driven, innovative, strategic thinker, fast learner, team player, self-starter, responsible for, involved in, worked on, familiar with, exposure to, scalable systems, cloud-native, product mindset, security-first, hands-on architect, AI enthusiast, ML expert, end-to-end architect, technical visionary.

**Stronger evidence to look for:** built, designed, shipped, owned, migrated, scaled, optimized, reduced latency, improved reliability, increased revenue, launched product, mentored engineers, defined architecture, drove cross-functional delivery, promoted, reduced cost, improved deployment frequency or MTTR, deployed models to production, owned product metrics or roadmap outcomes.

Prefer statements tied to a concrete system or feature, a measurable outcome, and clear ownership — not adjectives.

**Red flags:** job hopping, title inflation, vague responsibilities, inflated leadership claims, stagnation, a mismatch between claimed level and visible scope.

**Green flags:** steady progression, internal promotions, growing ownership, measurable achievements, a modern technical environment, credible transferability between roles.

# Reference: Domain Families

Use these to expand relevant context before screening — they improve recall, but never override the hard filters or the need for actual evidence.

- **Backend / Startup / SaaS** — prefer product ownership, modern stack, real production APIs, measurable scale or reliability impact.
- **Data / ML** — prefer productionized models or data systems and measurable outcomes over academic-only claims.
- **Product / Tech Product** — prefer roadmap ownership, shipped features tied to user or revenue impact, over generic stakeholder language.
- **Security / DevOps / Platform** — prefer automation, measurable reliability improvements, real operational ownership over policy-only mentions.
- **Architect** — prefer architecture paired with actual execution, not the title alone.
- **Fintech** — prefer concrete ownership of payments, risk, fraud, compliance, or transactional systems over generic "fintech" branding.
- **Healthcare** — prefer concrete ownership of clinical, patient, or healthcare-data systems over generic "healthtech" branding.
