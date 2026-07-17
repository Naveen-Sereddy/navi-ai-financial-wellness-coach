# NAVI

AI financial wellness benefit for the workplace, embedded in tools employees already use (Slack, Workday, BambooHR) instead of shipping as a separate app. 8-screen web prototype plus a separate mobile prototype at 390px.

**Live case study:** [naveensereddy.com/case-navi](https://naveensereddy.com/case-navi)

## Features

- Onboarding: connect payroll and accounts, set goals, trust-first AI introduction
- Dashboard: paycheck card, spending breakdown, proactive AI insights
- Weekly check-in with accept/override actions on each recommendation
- Goal tracking with a 13-month savings plan
- Full explainability panel: confidence score, data sources, and reasoning behind every recommendation
- Anomaly alerts with three resolution paths
- A simulated Slack Block Kit view of the embedded experience
- A privacy screen showing exactly what NAVI accessed, with redaction controls

Every recommendation ships with a confidence score, the data behind it, and an override button. NAVI never acts on its own.

## Tech stack

Both prototypes (`Navi - AI Financial Coach.html`, `Navi - Mobile.html`) run on a custom runtime, `support.js`, generated from a TypeScript source tree (`dc-runtime`) and built with Bun. The runtime wraps React under a custom-element system (`<x-app>`, `<x-import>`) rather than a standard bundler setup, confirmed by the generated-file header in `support.js` itself. There's no `package.json` in this repo; the runtime ships pre-built.

No backend, no database. It's a click-through prototype.

## Project structure

```
Navi - AI Financial Coach.html   # web prototype, entry point
Navi - Mobile.html                # mobile prototype (390px)
support.js                         # generated runtime (dc-runtime, do not edit directly)
deck-stage.js                       # slide-deck stage component, used by presentation-style sections
DESIGN.md                            # design token spec: claymorphism rationale, color, type, spacing
CASE-STUDY.md                         # research, usability results, outcomes
PORTFOLIO.md                           # shorter portfolio-facing summary
```

## Why I built it this way

The research came first: 7 HR managers and 12 employees across two mid-sized tech companies, and the same complaint kept coming up. Companies offer financial wellness benefits, but adoption sits around 3%, not because people don't care about money but because the apps feel like homework: clinical interfaces, banking-terminal aesthetics, a separate download to remember to open.

Claymorphism (soft 3D surfaces, warm sky-blue backgrounds, tactile card shadows) was a deliberate response to that, documented in full in `DESIGN.md`. Most fintech tools default to flat, dark, data-dense interfaces that read like audit software, the wrong register for a product built around financial anxiety.

The harder constraint was Slack's Block Kit: no charts, three buttons max, text only. Every standalone screen got better once I stress-tested it against that embedded format, since it forced the design to say only what actually mattered.

## Usability results

8-participant study, simulated onboarding plus two recommendation flows (full detail in `CASE-STUDY.md`):

- Average time to act on a recommendation: 38 seconds, against a 4.2-minute benchmark from comparable finance apps
- Trust rating: 4.4 / 5
- 7 of 8 participants said they'd use NAVI if their employer offered it

## Getting started

Open `Navi - AI Financial Coach.html` in any modern browser for the web prototype, or `Navi - Mobile.html` for the mobile flow. No install, no build.

## License

MIT

---

Naveen Sereddy · [naveensereddy.com](https://naveensereddy.com) · [github.com/Naveen-Sereddy](https://github.com/Naveen-Sereddy)
