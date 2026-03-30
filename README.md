# Onsite Copilot OS

AI Operating System for construction risk minimization — 3 agents that handle technical research, developer partnerships, and experiment validation so you can focus on building the product and getting site access.

## What's Inside

| Agent | What It Does |
|-------|-------------|
| **@site-risk-detector** | Researches construction AI landscape, competitor analysis, technical benchmarks, inspector workflows |
| **@developer-connector** | Finds developers and GCs, manages outreach pipeline, preps meetings, tracks relationships |
| **@experiment-runner** | Designs and tracks SFE experiments, maintains hypothesis tracker, updates P/V estimates |

## Setup (~10 min)

```bash
git clone https://github.com/polarbaker/onsite-copilot-os.git
cd onsite-copilot-os
npx -y google-workspace-mcp serve  # authorize Google account once
claude                              # open Claude Code
```

Then try: `@site-risk-detector Compare our approach to Buildots and OpenSpace`

## File Structure
```
onsite-copilot-os/
├── CLAUDE.md                                  # System instructions
├── .mcp.json                                  # Google Workspace connection
├── README.md                                  # This file
└── .claude/skills/
    ├── site-risk-detector/SKILL.md
    ├── developer-connector/SKILL.md
    └── experiment-runner/SKILL.md
```

## Privacy
Everything runs locally. Google Workspace data stays in your account.

---
Built by Gold Star AI — SFE HBS 1257
