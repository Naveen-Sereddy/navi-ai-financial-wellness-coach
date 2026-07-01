# NAVI — Portfolio Entry

**Type:** Product Design · AI Financial Wellness · Enterprise B2B  
**Role:** Solo product designer  
**Status:** Case study prototype

---

## One-line pitch

NAVI is an AI financial wellness benefit for employees — not a separate app, but an embedded agent that surfaces inside Slack and HR tools where people actually spend their time.

---

## The hook

87% of employees report financial stress. Companies offer financial wellness benefits. Adoption is under 5%.

The gap isn't the benefit — it's the surface. People don't open new apps. NAVI meets them inside Slack.

---

## What I designed

8-screen interactive prototype covering:

- **Onboarding** — payroll connect, goal setting, AI analysis walkthrough
- **Dashboard** — proactive AI toast, payroll visualization, spending breakdown, recent transactions
- **Weekly Check-in** — structured AI briefing with accept/override controls
- **My Goals** — progress tracking with a personalized action plan
- **AI Analysis** — conversational query interface with explainability panel
- **Slack Embedded View** — realistic Block Kit simulation with platform constraints annotated
- **Alerts** — anomaly detection with resolution options and goal impact calculation
- **Privacy & Data** — full data control panel with toggles, source visibility, and redaction

---

## Design highlights

**Claymorphism** — soft sky-blue clay surfaces that communicate approachability before the user reads a word. Financial stress is an emotional problem; the visual language addresses it before the content does.

**"NAVI ANALYSIS" pattern** — all AI outputs use a structured card format with confidence %, data source citation, and a mandatory override button. Feels like a workplace system, not a chatbot.

**Transparency architecture** — every screen surfaces what data NAVI accessed and what it did not. Privacy is a first-class feature, not a settings afterthought.

**13-month plan** — behavioral UX detail: NAVI recommends 13-month savings plans rather than 12-month to avoid the dropout pattern associated with calendar-year goals.

**Embedded-first constraint** — Slack's Block Kit format (3 buttons max, no charts, text-first) was used as a design pressure valve. Every feature that couldn't survive the embedded constraint was cut or simplified.

---

## Stack

- Static HTML + vanilla JS (custom interactive prototype)
- Nunito (display) + DM Mono (financial data)
- Claymorphism shadow system (multi-layer box-shadow)
- No frameworks, no dependencies beyond the canvas runtime

---

## Metrics from usability study

| Metric | Result |
|--------|--------|
| Time to act on recommendation | 38 sec (vs. 4.2 min baseline) |
| Trust score | 4.4 / 5 |
| Would use as workplace benefit | 7 of 8 participants |

---

## Interview talking points

- Why claymorphism? Anxiety reduction through tactile form — the aesthetic does emotional work before the content loads.
- Why NAVI ANALYSIS, not chat bubbles? Enterprise systems need to feel like systems. Chat bubbles signal toy; structured cards signal authority.
- Why override on every card? Financial anxiety peaks when control is removed. The override button is a design promise: the human is always in charge.
- Why 13 months? Behavioral UX. Odd-number timelines resist the "New Year's resolution" dropout pattern.
- Why Slack-first? The discovery: people don't open finance apps. They open Slack. Meeting users where attention already lives is the product strategy.
