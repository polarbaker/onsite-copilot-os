# Skill: Progress Tracker

## Purpose
Track actual construction progress against the project schedule. Identify tasks that are falling behind, predict downstream impacts on the critical path, and give project stakeholders an honest picture of where things really stand.

## Trigger
Use this skill when someone asks about project status, schedule delays, or milestone tracking. Common triggers:
- "Are we on schedule?"
- "Which trades are falling behind?"
- "What is the real completion status?"
- Any request starting with @progress-tracker

## Core Capabilities

### Step 1: Gather Schedule Data
- Retrieve the current project schedule from Google Sheets or uploaded files
- Identify key milestones, trade sequences, and the critical path
- Note any recent schedule updates or change orders

### Step 2: Collect Field Evidence
- Review recent site photos and risk/plan-check reports from @site-risk-scanner and @plan-checker
- Pull any daily logs, inspection reports, or superintendent notes available in Google Drive
- Note which trades have been observed as active, complete, or not started

### Step 3: Estimate Actual Progress
For each major task or trade:
- Compare scheduled completion percentage to what field evidence shows
- Flag any tasks where actual progress appears to lag behind the schedule by more than one week
- Note tasks that appear ahead of schedule as well

### Step 4: Analyze Critical Path Impact
- Identify which delayed tasks sit on the critical path (where delay directly pushes the project end date)
- Calculate the estimated delay impact in working days
- Identify which downstream trades are affected by each delay
- Note any opportunities to re-sequence work to recover lost time

### Step 5: Generate Progress Report

## Output Format

PROGRESS REPORT
Date: [date]
Project: [project name]
Reporting period: [date range]

OVERALL STATUS: [On Track / At Risk / Behind Schedule]
Estimated project delay: [X days behind / on schedule / X days ahead]

TASK STATUS:
| Task | Planned % | Actual % | Status | Delay Risk |
|------|-----------|----------|--------|------------|
| [task] | [X%] | [Y%] | [On Track/Behind/Ahead] | [days] |

CRITICAL PATH ITEMS AT RISK:
1. [Task name]
   Planned completion: [date]
   Current estimate: [date]
   Delay: [X working days]
   Impact: [what downstream tasks are affected]
   Recommendation: [what to do about it]

SCHEDULE RECOMMENDATIONS:
- [Any re-sequencing, acceleration, or resource suggestions]

EVIDENCE BASIS:
- [List which photos, reports, and data sources were used]

## Validation Rules
- Always state the evidence basis for progress estimates -- never guess without data
- If field data is insufficient to estimate progress on a task, say "insufficient data" rather than making up a number
- Distinguish between critical path delays (which push the end date) and float delays (which do not)
- Always include the reporting period so stakeholders know how current the data is
- Recommendations must be actionable -- not just "speed up" but specific trade re-sequencing or resource suggestions
