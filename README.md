# NAVI — AI Financial Wellness Coach

**Live case study:** [naveensereddy.com/case-navi](https://naveensereddy.com/case-navi)

A product design case study, 6 weeks, solo, end to end.

NAVI is an AI-powered financial wellness benefit built for the workplace — not a standalone app, but something that lives inside the tools employees already use every day: Slack, Workday, BambooHR.

## Why I built it this way

The idea came out of research. I interviewed 7 HR managers and 12 employees across two mid-sized tech companies, and kept hearing the same thing: companies offer financial wellness programs, but almost nobody uses them. Adoption sat around 3%. Not because employees don't care about money. Because the apps feel like homework — clinical interfaces, banking-terminal aesthetics, a separate download you have to remember to open. The stress the product is supposed to fix gets amplified by the product itself.

So instead of building another finance app, I redesigned the concept. NAVI doesn't ask employees to change their behavior and open something new. It shows up where they already are, and it explains itself instead of just issuing verdicts — every recommendation carries a confidence score, the data behind it, and an override button. NAVI never acts on its own; the human decides. That was non-negotiable from day one.

The visual language matters here too. Most fintech tools default to flat, dark, data-dense interfaces that read like audit software — the wrong register for a product built around financial anxiety. I used claymorphism instead: soft 3D surfaces, warm sky-blue backgrounds, tactile card shadows. It communicates safety before the user reads a word, which matters when someone's opening a financial alert on a Tuesday morning. The harder design constraint was Slack's Block Kit: no charts, three buttons max, text only. Every standalone screen got better once I stress-tested it against that embedded format — it forced NAVI to say only what actually mattered.

In an 8-participant usability study (simulated onboarding plus two recommendation flows), average time to act on a recommendation was 38 seconds against a 4.2-minute benchmark. Trust rating came in at 4.4 out of 5, and participants specifically called out trusting the reasoning, not just the output. 7 of 8 said they'd use NAVI if their employer offered it.

## What's built

8 screens in the standalone web prototype, plus a separate mobile prototype covering the core flows at 390px:

- Onboarding — payroll connect, goal setting, trust-first AI introduction
- Dashboard — paycheck card, spending breakdown, proactive AI insights
- Weekly check-in — NAVI briefing with accept/override actions
- My goals — progress tracking, 13-month savings plan
- AI analysis — full explainability panel, confidence scores, data sources
- Alerts — anomaly detection with three resolution paths
- Slack embedded view — Block Kit simulation of the in-Slack experience
- Privacy & data — what NAVI accessed, what it didn't, full redaction controls

## Run the prototype

Open `Navi - AI Financial Coach.html` in any browser for the full web experience, or `Navi - Mobile.html` for the mobile flow. No dependencies, no install — just open and click through.

## Tools

Figma, HTML/CSS for the interactive prototype, user interviews.

---

Naveen Sereddy — [naveensereddy.com](https://naveensereddy.com) · [github.com/Naveen-Sereddy](https://github.com/Naveen-Sereddy)
