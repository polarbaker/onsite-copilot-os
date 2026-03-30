# Onsite Copilot OS

An AI operating system for construction risk minimization and rework reduction. Built for Teresa He's Onsite Copilot startup.

---

## What's Inside

| Agent | What It Does |
|-------|-------------|
| **@site-risk-scanner** | Analyzes site photos for safety hazards, quality risks, and deviations from standard practices |
| **@plan-checker** | Compares photos of completed work against architectural drawings to catch discrepancies |
| **@progress-tracker** | Tracks real construction progress vs. schedule and predicts downstream delay impacts |
| **@rework-analyst** | Finds patterns in construction errors to identify root causes and repeat issues |

---

## Setup

1. **Install Claude Code** — Follow the instructions at [claude.ai/code](https://claude.ai/code)
2. **Clone this repo** — `git clone https://github.com/polarbaker/onsite-copilot-os.git`
3. **Open in Claude Code** — `cd onsite-copilot-os && claude`
4. **Connect your tools** — Set up Google Drive and Google Sheets access when prompted
5. **Upload project plans** — Put your architectural drawings and specifications into a Google Drive folder

---

## File Structure

```
onsite-copilot-os/
├── CLAUDE.md                            # System identity, principles, and agent guide
├── README.md                            # This file
├── .mcp.json                            # Tool connections (Google Drive, Sheets)
└── .claude/
    └── skills/
        ├── site-risk-scanner/
        │   └── SKILL.md                 # How @site-risk-scanner analyzes site photos
        ├── plan-checker/
        │   └── SKILL.md                 # How @plan-checker compares work to plans
        ├── progress-tracker/
        │   └── SKILL.md                 # How @progress-tracker monitors schedules
        └── rework-analyst/
            └── SKILL.md                 # How @rework-analyst finds error patterns
```

---

## How It Works

**The problem:** Construction rework wastes ~10% of project costs. Mistakes go undetected for weeks because inspection cycles are too slow.

**The solution:** Four AI agents that work together to catch errors early, compare work against plans, track real progress, and surface patterns that cause repeated rework.

**The flow:**
1. Field teams take photos during site walkthroughs (using phones they already carry)
2. @site-risk-scanner flags immediate safety and quality concerns
3. @plan-checker verifies completed trades match the architectural design
4. @progress-tracker aggregates findings into an honest project status picture
5. @rework-analyst identifies systemic issues so they can be fixed at the source

---

## Privacy

This system processes construction site data. All project plans, photos, and reports stay in your connected Google Drive. No construction data is stored by the AI system between sessions unless you explicitly save it to your own tools.

---

*Built by Gold Star AI — SFE HBS 1257*
