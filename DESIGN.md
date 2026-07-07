# Navi Design System
## AI Financial Wellness for Work — Token Specification v2.0

> **Author:** Naveen Sereddy · UX Designer  
> **Status:** Active · Last updated June 29, 2026  
> **Scope:** Employee-facing prototype · Enterprise B2B · Embedded + standalone surfaces  
> **Product:** Navi — embedded AI financial wellness agent (TechCorp Benefits)

---

## 0. Visual Language: Claymorphism

### Why claymorphism for a financial wellness product?

Most enterprise financial tools default to flat, clinical interfaces — dark backgrounds, cold blues, data-dense grids. They feel like audit software. That's the wrong signal for a product built around financial anxiety.

**The product position:** Navi lives inside Slack, Workday, and HR portals. It shows up uninvited in moments of financial stress — a paycheck alert, a bill overlap, a missed savings month. The design must communicate one thing before the user reads a single word: *this is not threatening.*

Claymorphism — soft 3D surfaces, warm off-white backgrounds, dome shadows that make UI feel tactile and approachable — solves this directly.

**The "best friend who happens to know finance" argument:**  
When you imagine getting financial advice from a trusted friend, you don't imagine a Bloomberg terminal. You imagine a warm conversation, maybe over coffee. The claymorphism treatment creates that subconscious register. The surfaces feel soft, rounded, held. The gold accent reads warm, not alarming. The typography (Nunito) is friendly without being juvenile.

**Why this matters for employee adoption:**  
Financial stress products fail at activation. Employees enroll in benefits they never use because the interface makes the anxiety worse, not better. Every pixel of a financial wellness tool is a trust signal. Claymorphism externalizes trust through tactile, warm, approachable form — before the AI says a word.

**Behavioral design rationale:**  
- Rounded corners (20px+) signal safety, not urgency
- Multi-layer soft shadows create dimensionality without aggression
- Off-white warm background (#EAE6DF) reads like paper, not a screen
- Gold accent (#B8870A) is amber-toned, not flashy — signals attention without alarm
- Inset (recessed) elements signal "settled" state — the plan is set, the data is stable

### Shadow Formula

**Primary clay card** (elevated, interactive):
```
box-shadow:
  8px 8px 20px rgba(0,0,0,0.15),
  -4px -4px 12px rgba(255,255,255,0.82),
  inset -3px -3px 8px rgba(0,0,0,0.07),
  inset 3px 3px 8px rgba(255,255,255,0.62);
```

**Inner recessed surface** (data display, settled state):
```
box-shadow:
  inset 3px 3px 7px rgba(0,0,0,0.12),
  inset -2px -2px 6px rgba(255,255,255,0.55);
```

**Nav item active** (pressed in, selected):
```
box-shadow:
  inset 3px 3px 8px rgba(0,0,0,0.18),
  inset -3px -3px 8px rgba(255,255,255,0.5);
```

---

## 1. Color Tokens

### 1.1 Clay Palette

| Token | Value | Usage |
|-------|-------|-------|
| `color.bg` | `#DFF0FF` | Page background (soft sky blue) |
| `color.surface` | `#FFFFFF` | Cards, sidebar, elevated surfaces (white clay) |
| `color.surface.inner` | `#E8F3FF` | Recessed elements, stat backgrounds |
| `color.border` | `#BDD8F5` | All borders, dividers |
| `color.text.1` | `#0D2137` | Primary text, headings (deep navy) |
| `color.text.2` | `#3D5E7A` | Secondary text, descriptions |
| `color.text.3` | `#7A9BB5` | Muted text, timestamps |

### 1.2 Semantic Colors

| Token | Value | Usage rule |
|-------|-------|------------|
| `color.blue` | `#3D96F0` | CTAs, AI active states, primary accent. Signal use only. |
| `color.blue.bg` | `rgba(61,150,240,0.08)` | Blue-tinted card backgrounds |
| `color.emerald` | `#22A55A` | Success, money up, goal milestones, high confidence |
| `color.amber` | `#D97706` | Medium confidence, caution |
| `color.red` | `#DC4545` | Errors, anomalies, spending overages |

### 1.3 Anti-patterns

- Purple of any shade
- Warm brown or gold as primary — previous palette, retired
- Heavy dark backgrounds on main screens — NAVI is light and airy
- Saturated neon blue — use muted sky blue (#3D96F0) only
- Heavy dark backgrounds on main screens — Navi is warm, not moody

---

## 2. Typography

### 2.1 Font Families

| Token | Family | Usage |
|-------|--------|-------|
| `font.display` | Nunito | All body copy, headings, UI labels, navigation |
| `font.mono` | DM Mono | All financial figures, account numbers, amounts |

**Why Nunito:** Rounded letterforms that reinforce the claymorphism aesthetic. Warm and readable. Professional enough for enterprise, approachable enough for anxious employees.

**Why DM Mono:** Clean and tabular for financial data. Distinguishable from the display font at small sizes. Paired gold accent numbers read as precise and trustworthy.

### 2.2 Scale

| Token | Size | Weight | Usage |
|-------|------|--------|-------|
| `type.hero` | 32px | 800 | Dashboard greeting, onboarding headline |
| `type.title` | 26px | 800 | Screen titles |
| `type.subheading` | 15px | 700 | Card section headers |
| `type.body` | 13px | 500 | Body copy, AI messages |
| `type.label` | 11–12px | 600 | Meta labels, timestamps |
| `type.micro` | 10px | 700 | ALL-CAPS section labels (letter-spacing: 0.08em) |
| `type.mono.lg` | 26–28px | 700 | Primary financial figures |
| `type.mono.sm` | 12–13px | 500 | Inline financial values |

---

## 3. Spacing Grid

**Base unit: 4px**

| Token | Value | Usage |
|-------|-------|-------|
| `space.2` | 8px | Icon gaps, micro spacing |
| `space.3` | 12px | Component gaps |
| `space.4` | 16px | Card internal padding (small) |
| `space.5` | 20px | Card internal padding (standard) |
| `space.6` | 24px | Section spacing |
| `space.8` | 32px | Screen padding |
| `space.9` | 36px | Content area padding |

---

## 4. Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `radius.sm` | 10px | Tags, badges, small buttons |
| `radius.card` | 20px | All primary cards |
| `radius.card.inner` | 14px | Inner cards, stats tiles |
| `radius.button` | 14–16px | Primary buttons |
| `radius.full` | 9999px | Toggles, pills, avatars |

**Rule:** Generous radius reinforces the clay form. 20px is the primary card radius. Inner cards use 14px. Embedded surfaces (Slack interior) use 5–8px to match platform conventions.

---

## 5. Component States

### 5.1 State Definitions

| State | Visual treatment |
|-------|-----------------|
| **Default** | `color.surface` bg · primary clay shadow |
| **Active / Selected** | `color.gold.bg` bg · gold border · gold text · nav inset shadow |
| **Recessed / Settled** | `color.surface.inner` bg · inset shadow |
| **Alert / Warning** | `color.red.bg` · red border |
| **Success** | `color.emerald.bg` · emerald border |
| **Disabled** | 50% opacity · not-allowed cursor |

### 5.2 Transition Standard
```css
transition: background 200ms ease-out, border-color 200ms ease-out, box-shadow 200ms ease-out;
```

---

## 6. AI-Specific Component Patterns

### 6.1 Navi Analysis Card

```
┌─────────────────────────────────────────┐  ← 20px radius, clay shadow
│ NAVI ANALYSIS               [timestamp] │
├─────────────────────────────────────────┤
│ [body text — structured, not            │
│  conversational. Presents data,         │
│  not opinions]                          │
│                                         │
│ Confidence: ▓▓▓▓▓▓▓▓▓░ 87%             │  ← emerald bar
│ Source: TechCorp Payroll · Chase        │
├─────────────────────────────────────────┤
│ [Accept]  [⊘ Override]  [Ask why ↗]    │  ← gold CTA, muted override
└─────────────────────────────────────────┘
```

**Rules:**
- Label says "NAVI ANALYSIS" — never "Navi says"
- Every card shows confidence % and data source
- Every card has Override — human always in control
- "Ask why ↗" opens Explainability Panel

### 6.2 Confidence Indicator

- High (80–100%): `color.emerald` fill
- Medium (50–79%): `color.amber` fill
- Low (< 50%): `color.red` fill + uncertainty note

### 6.3 Explainability Panel

Slides from right (400px wide). Five required sections:

1. **Data Used** — what Navi accessed + what it did NOT access
2. **Alternatives Considered** — all options evaluated, with rejection reasons
3. **Confidence Breakdown** — per-factor bars
4. **What Would Change This** — conditions that trigger recalculation
5. **Dispute / Redact** — data redaction CTA

### 6.4 Human Override Flow

1. Click "⊘ Override"
2. Reason selection (3–5 options)
3. Confirmation: "Navi will note your override and update future recommendations"

**Critical:** Navi never acts on its own. Every recommendation requires explicit user confirmation.

### 6.5 Proactive vs Reactive

| Pattern | Trigger | Surface |
|---------|---------|---------|
| **Proactive** | Payroll event, anomaly, calendar-aware | Toast, Slack DM, Check-in |
| **Reactive** | User question | AI Analysis screen |

Proactive messages carry `PROACTIVE` badge in gold. Never framed as alerts — framed as briefings.

---

## 7. Embedded Surface Constraints

### 7.1 Slack / Microsoft Teams (platform-native light interior)

When Navi renders inside Slack:
- Sidebar: `#3F0E40` (Aubergine — Slack's default workspace theme, stays dark purple even in light mode)
- Sidebar inactive text: `#CFC3CF` · active item bg: `rgba(255,255,255,0.2)` · active text: `#FFFFFF`
- Main DM area: `#FFFFFF` · text: `#1D1C1D` · secondary: `#616061` · dividers: `#E8E8E8`
- Block Kit card bg: `#F8F8F8` · border-left accent: `#3D96F0`
- Action buttons: primary `#3D96F0` fill; secondary white bg + `rgba(29,28,29,0.24)` border
- Input: white bg, `rgba(29,28,29,0.28)` border, `#868686` placeholder
- Outer context banner and constraint footer use clay treatment on `#FFFFFF` / `#BDD8F5`
- Block Kit format: max 3 buttons per message
- No custom data visualization — text + inline figures only

### 7.2 Workday / BambooHR Embed

- 320–400px iframe width
- Single-screen only
- Simplified visualization: text bars, no SVG charts
- SSO passthrough

### 7.3 Standalone Portal

Full claymorphism treatment. All 8 screens available.

---

## 8. Privacy-First Design Rules

1. Every AI card cites data sources
2. Every AI screen shows what was NOT accessed (negative disclosure)
3. Privacy & Data screen always reachable within 2 taps
4. HR aggregate visibility: opt-in, off by default
5. Data redaction always visible — never behind support
6. "Navi never acts without your confirmation" — required copy whenever Navi proposes action

---

## 9. Screen Inventory

| Screen | Status | Key flows |
|--------|--------|-----------|
| Onboarding (4 steps) | ✅ Built | Payroll connect · Goal set · Analysis |
| Dashboard | ✅ Built | Proactive toast · Payroll bar · Insights · Spending · Transactions |
| Weekly Check-in | ✅ Built | Navi briefing · Accept/Override · Mark reviewed |
| My Goals | ✅ Built | Progress ring · Bar chart · Action plan |
| AI Analysis | ✅ Built | System UI chat · Explainability panel · Override |
| Alerts | ✅ Built | Anomaly detection · Resolution options · Goal impact |
| Embedded View | ✅ Built | Slack DM simulation · Platform constraints annotation |
| Privacy & Data | ✅ Built | Data sources · AI behavior toggles · Redaction actions |

---

## 10. Case Study Framing

**Product position:** Not a consumer finance app. A financial wellness benefit embedded where work already happens.

**Research foundation:** 7 HR manager interviews + 12 employee interviews. Finding: employees don't open finance apps — they open Slack, payroll portals, HR dashboards. The opportunity was embedding the advisor where attention already lives.

**Key design decisions to defend:**

1. Claymorphism (not flat or dark) — anxiety reduction through tactile warmth
2. Amber-gold primary (not blue) — warm intelligence vs. cold corporate
3. "NAVI ANALYSIS" labels (not chat bubbles) — enterprise system feel, not a toy
4. Confidence scores on every recommendation — transparent AI
5. Human override on every card — control, not dependency
6. Privacy controls prominent, not buried — trust architecture
7. 13-month plan over 12 — behavioral UX over aspirational UX

**The pivot:** Consumer concept → 7 HR + 12 employee interviews → enterprise embedded opportunity → redesigned for Slack-first surfaces and payroll-aware AI.

---

## 11. Accessibility Standards

| Requirement | Implementation |
|------------|----------------|
| Color contrast | WCAG AA minimum (4.5:1 body, 3:1 large text) |
| Focus indicators | Gold 2px outline |
| Touch targets | Minimum 44×44px |
| Keyboard navigation | All flows completable keyboard-only |
| Screen reader | All AI suggestions have text alternatives |
| Motion | Respects `prefers-reduced-motion` |

---

*This spec is the source of truth for all Navi design decisions. Any deviation requires justification in the component documentation.*
