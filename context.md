# Project Context

> This file keeps the AI assistant (and Tim & Sunil) aligned across conversations.
> Update this file whenever scope, direction, or key details change.

---

## Project Summary

**What:** Building simple automation & AI tools for small (mom-and-pop) businesses.
**Who:** Tim & Sunil (partners)
**Where:** Starting in Seattle, expanding based on traction.
**When:** Kicked off April 28, 2026.

---

## Current Status

| Item | Status |
|---|---|
| **Phase** | Idea exploration — narrowing down to one idea |
| **Top Pick** | #1 — "Never Miss a Lead" (home services) |
| **Alternative** | #2 — "Full House" Restaurant Customer Engine |
| **Decision Pending** | Tim & Sunil need to align on which idea to pursue |
| **MVP Built?** | No — waiting on idea selection |
| **Pilot Customers** | 0 — haven't started outreach yet |
| **Live Dashboard** | https://sunilmsft.github.io/smb-automation/ |
| **GitHub Repo** | https://github.com/sunilmsft/smb-automation |

---

## The 5 Core Ideas

| # | Idea | Target | Score |
|---|---|---|---|
| 1 | "Never Miss a Lead" — missed call text-back + follow-up + reviews | Home services (plumber, HVAC, electrician) | ★★★★★ |
| 2 | "Full House" Restaurant Engine — waitlist, reviews, promo blasts | Independent restaurants & cafes | ★★★★ |
| 3 | "Booked Solid" — booking + reminders + no-show follow-up | Salons, barbers, med spas | ★★★ |
| 4 | Bakery/Retail Order Manager — order intake + confirmations + reorder nudges | Bakeries, specialty food shops | ★★★ |
| 5 | "Neighborhood CRM" — unified inbox + customer profiles + campaigns | Any local SMB (broad) | ★★ |

---

## Out-of-Box Ideas (added April 28)

| # | Idea | Target | Trust Barrier | "Holy Shit" Factor |
|---|---|---|---|---|
| 6 | **AI Phone Receptionist** — AI answers calls 24/7, takes messages, books appointments | Any SMB (start with dental, auto, law, med spa) | Low | 🔥🔥🔥🔥🔥 |
| 7 | Social Media Autopilot — snap a photo, AI posts everywhere | Restaurants, bakeries, salons, retail | Low | 🔥🔥🔥 |
| 8 | Permit & Compliance Autopilot — OCR permits, auto-reminders | Restaurants, contractors | Low | 🔥🔥 |
| 9 | "Invisible Bookkeeper" — AI auto-categorizes bank transactions | Any SMB <$1M revenue | **High (bank access)** | 🔥🔥🔥 |
| 10 | "Cash Flow Crystal Ball" — predict cash crunches 2–4 weeks out | Restaurants, retail | **High (bank/POS access)** | 🔥🔥🔥🔥 |
| 11 | "Ghost Kitchen Lite" — virtual brand during dead kitchen hours | Restaurants | **High (operational control)** | 🔥🔥🔥 |

**Key learning:** Ideas #9–11 need trust-building first. Better as Phase 2/3 after establishing customer relationships. Ideas #6–8 are actionable now.

---

## Constraints & Principles

- Keep it simple — no over-engineering
- Low cost to build and operate
- Test with 2–5 real businesses quickly
- Not trying to build a big startup (yet)
- SMB owners buy solutions, not features — packaging matters
- Seattle-first with in-person sales
- Target neighborhoods: Ballard, Capitol Hill, Fremont, Columbia City, University District

---

## Tech Stack (Planned for MVP)

- **Twilio** — phone number + SMS
- **Webhook** — Node.js or Python (free tier hosting)
- **Google Sheets** — lead log for v1 (replace with DB later)
- **GitHub Pages** — project dashboard hosting
- **No frontend needed** for MVP

---

## Pricing Strategy

- **Idea #1:** $49–$99/mo (businesses losing $500+/mo in missed leads)
- **Idea #2:** $99–$199/mo (less than one DoorDash commission)
- **Free 2-week trial** to get pilot customers in the door

---

## Key Stakeholders

| Person | Role | Focus |
|---|---|---|
| Sunil | Co-founder | Product, technical, AI |
| Tim | Co-founder | TBD — sales? ops? both? |

---

## Files in This Repo

| File | Purpose |
|---|---|
| `index.html` | Multi-tab project dashboard (hosted on GitHub Pages) |
| `context.md` | This file — project context for AI and team alignment |
| `memory.md` | Running log of conversations, decisions, findings, and learnings |
