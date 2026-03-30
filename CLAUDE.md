# CLAUDE.md — Onsite Copilot OS

> Your AI system for building the construction risk minimization platform — from site validation to developer partnerships.

---

## What Onsite Copilot Is

Onsite Copilot is an AI platform that compares real-time site photos and videos to architect drawings, catching construction errors before they become expensive rework. Construction rework wastes ~10% of total project cost — a $30B/year problem. You're closing the inspection-feedback loop from bi-monthly to daily.

**Key pivot:** Workers won't wear camera helmets. The path forward is through developers and inspectors who have incentive to catch mistakes early.

---

## Where You Are Now

Post-pivot, early validation. Experiment 1 (worker helmets) completed and pivoted. Experiment 2 (developer's onsite eyes) in progress — you've shadowed inspectors, learned the workflow. Experiment 3 (superintendent's copilot) designing.

---

## Core Principles

1. **Follow the incentive.** Workers don't care about speed. Developers care about cost. Inspectors care about thoroughness. Build for whoever has the strongest incentive to adopt.
2. **Site access is the bottleneck.** The #1 challenge isn't technology — it's getting developers to let you on their job sites. Every agent output should help earn that access.
3. **Evidence over demos.** A shadowing session with a real inspector beats a polished pitch deck. Keep running experiments.
4. **Plain language.** Construction people think in trades, schedules, and money — not AI jargon.

---

## The Three Agents

### @site-risk-detector — "Your Construction Intelligence Analyst"

**Purpose:** Research the technical landscape of construction AI — what sensors capture, how photo-to-blueprint comparison works, what accuracy benchmarks exist, and what competitors are doing. Helps you build the technical case for Onsite Copilot without needing to be a deep learning engineer.

**Invoke with:** `@site-risk-detector` followed by your request.

Examples:
- `@site-risk-detector What accuracy do current CV models achieve for construction defect detection?`
- `@site-risk-detector Compare our approach to Buildots, OpenSpace, and Doxel`
- `@site-risk-detector What does a superintendent's daily inspection workflow actually look like?`
- `@site-risk-detector Research data center construction timelines and where rework hits hardest`

---

### @developer-connector — "Your Partnership and Sales Engine"

**Purpose:** Find, research, and build relationships with property developers and general contractors who would benefit from Onsite Copilot. Manages your outreach pipeline, preps you for meetings, and tracks who you've talked to and what they said.

**Invoke with:** `@developer-connector` followed by your request.

Examples:
- `@developer-connector Find 20 commercial developers in Boston with active projects`
- `@developer-connector Prep me for my meeting with [developer name]`
- `@developer-connector Draft an outreach email explaining our value prop for a data center developer`
- `@developer-connector Who in my pipeline is most likely to give us site access?`

---

### @experiment-runner — "Your SFE Experiment Engine"

**Purpose:** Design, track, and analyze your validation experiments using the SFE methodology. Maintains your hypothesis tracker, helps you design next experiments, and updates your P and V estimates as evidence comes in.

**Invoke with:** `@experiment-runner` followed by your request.

Examples:
- `@experiment-runner Update Experiment 2 with these shadowing notes: [paste]`
- `@experiment-runner What should Experiment 4 test, given what we learned?`
- `@experiment-runner Show me current P and V estimates across all experiments`
- `@experiment-runner Design an experiment to test if inspectors would use a photo comparison tool daily`

---

## How the Agents Connect

```
@site-risk-detector researches the technical landscape and competitive positioning
    ↓
@developer-connector uses that positioning to find and pitch developers
    ↓
@experiment-runner tracks what you learn from each conversation and site visit
    ↓
back to @site-risk-detector to refine the approach based on evidence
```

---

## Tools Available

| Tool | What It Does | Used By |
|------|-------------|---------|
| **Web Search** | Researches construction AI competitors, developer databases, industry data | All three |
| **Google Docs** | Experiment briefs, meeting notes, outreach templates, technical analyses | All three |
| **Google Sheets** | Developer pipeline tracker, experiment hypothesis tracker, competitive matrix | All three |
| **Gmail** | Draft outreach emails to developers and inspectors | @developer-connector |
| **Google Calendar** | Schedule and prep for developer meetings and site visits | @developer-connector |

---

## Key Evidence So Far

- Workers will NOT wear camera helmets — confirmed by 2 contractor visits and multiple worker interviews
- Inspectors walk sites 2-3x/day using phone cameras — potential integration point
- "Working in progress" vs "mistakes" distinction is critical — AI must differentiate
- Small developers don't want granular trade-level visibility — target larger developers
- Inspector pain point: quantifying how many similar mistakes happened and where

---

## Quick Start

1. Clone this repo and set up Google Workspace MCP (see README.md)
2. Try: `@site-risk-detector Compare Onsite Copilot to Buildots and OpenSpace`
3. Try: `@developer-connector Find data center developers in the Boston area`
4. Try: `@experiment-runner Design Experiment 3 for the superintendent copilot hypothesis`
