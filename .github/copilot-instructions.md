# Copilot Instructions — SMB Automation Project

> Copilot reads this file automatically on any machine. It carries project context forward across sessions.

---

## Project Overview

**What:** Multi-tab HTML dashboard for a side project building simple automation & AI tools for small (mom-and-pop) businesses.
**Who:** Tim & Sunil (partners).
**Where:** Seattle-first, expanding based on traction.
**Repo:** https://github.com/sunilmsft/smb-automation
**Live:** https://sunilmsft.github.io/smb-automation/

---

## Tech Stack

- **Single-file app:** Everything is in `index.html` (~2,000+ lines). Pure HTML/CSS/JS — no frameworks, no build tools, no dependencies.
- **Hosting:** GitHub Pages (auto-deploys from `master` branch).
- **No package.json, no npm, no bundler.** Just a single HTML file.

---

## Dashboard Architecture

### Tabs (9 total)
| Tab | ID | Content |
|-----|-----|---------|
| Overview | `overview` | Mission, constraints, Seattle strategy, current recommendation |
| Core Ideas (5) | `ideas` | Ideas #1–#5 with detail cards |
| Out-of-Box Ideas (6) | `out-of-box` | Ideas #6–#11 with detail cards |
| Comparison Matrix | `comparison` | 3 sections: Core, Out-of-Box, Strategy & Bundles |
| Deep Dives | `deep-dives` | 11 research cards |
| Go-to-Market | `go-to-market` | GTM strategy |
| 2-Week Plan | `two-week-plan` | Timeline |
| Decision Log | `decision-log` | Chronological decisions |
| Open Questions | `open-questions` | Unresolved items |

### Navigation
- Tab nav: `position: sticky; top: 0; z-index: 100;` with IntersectionObserver
- CSS: `html { scroll-behavior: smooth; scroll-padding-top: 70px; }`
- Quick-nav link strips at top of: Core Ideas, Out-of-Box, Comparison, Deep Dives tabs

### ID Conventions
- Idea cards: `idea-1` through `idea-11`
- Deep dive cards: `dd-1`, `dd-2`, `dd-calendar`, `dd-voice`, `dd-costs`, `dd-sms`, `dd-hallucination`, `dd-onboarding`, `dd-churn`, `dd-language`, `dd-privacy`
- Comparison sections: `cmp-core` (blue), `cmp-oob` (purple), `cmp-strategy` (green)

---

## CSS Conventions

### Color System
```
--primary: #2563eb (blue)
--green-bg: #f0fdf4 / border: #bbf7d0
--blue-bg: #eff6ff / border: #bfdbfe
--yellow-bg: #fefce8 / border: #fef08a
Purple: #f3e8ff / border: #d8b4fe
```

### Tier Pill Styling
Multi-tier fields (Price, Build Complexity, Time to MVP) on Ideas #1 and #6 use colored pill spans:
- **v1/Voice** = green (`--green-bg/#bbf7d0`)
- **v2/+Text** = blue (`--blue-bg/#bfdbfe`)
- **v3/+Scheduling** = purple (`#f3e8ff/#d8b4fe`)
- Container: `display:flex;flex-direction:column;align-items:flex-start;gap:0.4rem;margin-top:0.25rem;`
- Pill: `padding:0.2rem 0.5rem;background:COLOR;border:1px solid BORDER;border-radius:5px;font-size:0.82rem;`

### Quick-Nav Link Styling
```
padding:0.3rem 0.7rem;border-radius:6px;font-size:0.82rem;text-decoration:none;
```

---

## Comparison Tab Structure

Three sections with colored h3 dividers:
1. **Core Ideas (#1–#5)** — blue border (`var(--primary)`) — Comparison Table + Investment Breakdown
2. **Out-of-Box (#6–#11)** — purple border (`#8b5cf6`) — Comparison Table + Investment Breakdown
3. **Strategy & Bundles** — green border (`#059669`) — Packaging Approach + Bundle Ideas + Bottom Line

Both comparison tables use **11 unified criteria:** Target Customer, Monthly Price, Build Time, Ease of Build, Ease of Sale, Trust Barrier, Market Opportunity, Competitive Moat, Expansion Potential, Key Risk, Overall Rating (★ stars).

### Bundle Card (6 bundles)
- Home Services Pro (#1+#6)
- Restaurant Growth Pack (#2+#7)
- Beauty & Bookings (#3+#7)
- Lead Machine (#1+#7)
- Full Front Office (#1+#6+#7)
- Restaurant Empire (#2+#7+#10)

---

## Idea #1 Tiers
| Tier | Price | What It Adds |
|------|-------|-------------|
| v1 | $79–$149/mo | Missed call text-back + follow-up + reviews |
| v2 AI Texting | $129–$199/mo | Two-way AI text conversations |
| v3 Lifecycle | $179–$249/mo | Warranty expiry nudges, service-due reminders, one-click scheduling |

## Idea #6 Tiers
| Tier | Price | What It Adds |
|------|-------|-------------|
| Voice | $199/mo | AI answers calls 24/7 |
| Voice + Text | $299/mo | + Two-way AI SMS |
| Full Suite | $399/mo | + Calendar/scheduling integration |

---

## Preferences & Workflow

- **Always push to GitHub after editing** — the prototype lives on GitHub Pages and Sunil references it there
- **Git push stderr is normal** — git push shows exit code 1 due to stderr output but pushes succeed
- **Verify nesting after edits** — run the PowerShell depth-checker to confirm all `<div>` tags are balanced
- **When replacing div opening tags** that share a line with h3 tags, be careful not to strip the h3

---

## Key Decisions Made

| Date | Decision | Rationale |
|------|----------|-----------|
| Apr 28, 2026 | Seattle-first strategy | In-person sales, dense business districts, word-of-mouth |
| Apr 28, 2026 | Bundle features under one theme | SMBs buy solutions not features |
| Apr 28, 2026 | Top pick: "Never Miss a Lead" (#1) | Easiest build, easiest sell, clearest ROI |
| Apr 28, 2026 | AI Comms Hub (#6) is biggest opportunity | Subsumes #1, biggest gap, low trust barrier |
| Apr 28, 2026 | Bank-access ideas (#9–#11) are Phase 2/3 | SMBs won't share bank login to strangers |
| Apr 28, 2026 | Added v3 Customer Lifecycle to #1 | Proactive service reminders turn past customers into repeat revenue |
| Apr 28, 2026 | Unified comparison criteria to 11 | Both tables now comparable; includes trust barrier + expansion potential |

---

## Other Files in This Repo

| File | Purpose |
|------|---------|
| `index.html` | The dashboard — single-file HTML/CSS/JS app |
| `context.md` | Project context for AI and team alignment |
| `memory.md` | Running log of conversations, decisions, findings |
| `.github/copilot-instructions.md` | This file — Copilot auto-reads it on any machine |
