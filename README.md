create /tmp/msme-finscore-card/README.md

# MSME FinScore Card

**Team Titans | IDBI Innovate 2026 | Track 03 — Financial Health Score**

## Problem

Bank's MSME credit evaluation relies on traditional financial documents, which many
New-to-Credit (NTC) and New-to-Bank (NTB) enterprises lack or maintain inadequately.
Despite rich alternate data (GST, UPI, Account Aggregator, EPFO), the absence of a
unified assessment framework leads to high rejection rates, missed viable borrowers,
and slower financial inclusion.

## Our Solution

**MSME FinScore Card** is an AI/ML-driven Financial Health Card that aggregates
consent-based alternate data — GST, UPI, Account Aggregator (AA), and EPFO — and
computes a transparent, multidimensional financial health score. It visualizes
strengths and risks, generates an explainable lend recommendation with reason codes,
and is designed to integrate with ULI/OCEN/AA rails for near real-time credit
assessment, unlocking credit for credit-invisible MSMEs while improving portfolio
quality for the bank.

## Live Demo

Open `index.html` in any browser, or view the deployed version:
**[GitHub Pages link — add after deployment]**

## How the Score Works

The engine computes a weighted score (0–100) across 5 pillars:

| Pillar                    | Weight | Signal Source                                |
| ------------------------- | ------ | -------------------------------------------- |
| Revenue Stability         | 25%    | GST filing consistency & revenue growth      |
| Cash Flow Health          | 25%    | UPI transaction volume & volatility          |
| Compliance & Credibility  | 20%    | Compliance index (GST/tax filing regularity) |
| Operational Footprint     | 15%    | EPFO employee count & business vintage       |
| Debt & Repayment Behavior | 15%    | Debt-to-revenue ratio & payment bounce rate  |

Each pillar contributes explicit **reason codes** (strengths in green, risk flags in
red) so every score is fully auditable — critical for credit decisioning.

## Prototype Scope (PoC)

This is a client-side prototype using **two hardcoded synthetic MSME profiles**
(one established business, one thin-file NTC business) to demonstrate the scoring
methodology, UI/UX, and explainability. It is **not connected to live GST/UPI/AA/EPFO
systems** — that integration is planned for the pilot phase via IDBI's sandbox APIs.

## Tech Stack

- Vanilla HTML/CSS/JS (zero build step, zero dependencies) for the PoC UI
- Scoring logic: transparent rules-based weighted engine (see `computeFinScore()` in `index.html`)
- Planned for pilot: Python (FastAPI) scoring API, PostgreSQL, AWS hosting,
  ULI/OCEN/AA integration

## Roadmap

1. **PoC (current):** Scoring engine + Health Card UI on synthetic profiles
2. **Post-shortlist:** Integrate IDBI sandbox APIs, test on synthetic bank datasets
3. **Pilot:** Connect live ULI/OCEN/AA rails, run with loan officers
4. **Production:** Full rollout inside IDBI's MSME lending workflow

## Team

- **Mritunjay** — Team Leader (Team: Titans)

## Files

- `index.html` — full interactive prototype (open directly in browser)
- `finscore_card_sample.png` — static Health Card snapshot (for deck/screenshots)
