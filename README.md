# NAVI — AI Financial Wellness Coach

A product design case study. 6 weeks, solo, end-to-end.

---

## What this is

NAVI is an AI-powered financial wellness benefit built for the workplace — not as a standalone app, but as something that lives inside the tools employees already use every day (Slack, Workday, BambooHR).

The core idea came out of research. I interviewed 7 HR managers and 12 employees across two mid-sized tech companies, and kept hearing the same thing: companies offer financial wellness programs, but nobody uses them. Adoption was around 3%. Not because employees don't care about money — they do — but because the apps feel like homework. Clinical interfaces, banking-terminal aesthetics, a separate download you have to remember to open. The stress the product is supposed to fix gets amplified by the product itself.

So instead of building another finance app, I redesigned the concept entirely. NAVI doesn't ask employees to change their behavior and open something new. It shows up where they already are.

---

## The design problem

Most fintech tools default to flat, dark, data-dense interfaces that feel like audit software. That's the wrong register for a product built around financial anxiety.

I used claymorphism — soft 3D surfaces, warm sky-blue backgrounds, tactile card shadows — specifically because it communicates safety before the user reads a single word. The visual language says: this is not threatening. That matters a lot when someone opens a financial alert on a Tuesday morning.

Beyond aesthetics, the biggest challenge was designing for Slack's Block Kit constraints: no charts, max 3 buttons per message, text-first. Every standalone screen improved once I stress-tested it against that embedded format. It forced NAVI to say only what actually mattered.

---

## What's built

**8 screens in the standalone web prototype:**

- Onboarding — payroll connect, goal setting, trust-first AI introduction
- Dashboard — paycheck card, spending breakdown, proactive AI insights
- Weekly Check-in — NAVI briefing with accept/override actions
- My Goals — progress tracking, 13-month savings plan
- AI Analysis — full explainability panel, confidence scores, data sources
- Alerts — anomaly detection with three resolution paths
- Slack Embedded View — Block Kit simulation showing the embedded experience
- Privacy & Data — what NAVI accessed, what it didn't, full redaction controls

**Plus a separate mobile prototype** covering the core flows at 390px.

Every AI recommendation shows a confidence percentage, the data it used, and an Override button. NAVI never acts on its own. The human is always in charge — that was non-negotiable from day one.

---

## Outcomes

Usability study with 8 participants (simulated onboarding + 2 recommendation flows):

- Average time to act on a recommendation: **38 seconds** vs. 4.2 min benchmark
- Trust rating: **4.4 / 5** — participants said they trusted the reasoning, not just the output
- Adoption intent: **7 of 8** said they'd use NAVI if their employer offered it

---

## Tools

Figma · HTML/CSS (interactive prototype) · User interviews

---

## View the prototype

Open `Navi - AI Financial Coach.html` in any browser for the full web experience.  
Open `Navi - Mobile.html` for the mobile flow.

No dependencies, no install — just open and click through.

---

## Case study

Full write-up with research findings, design decisions, and process: [naveen-sereddy.vercel.app](https://naveen-sereddy.vercel.app)
