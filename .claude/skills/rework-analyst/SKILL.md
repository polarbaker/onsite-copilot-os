# Skill: Rework Analyst

## Purpose
Analyze patterns across all detected construction errors and rework events to identify root causes, repeat offenders, and systemic issues. Turn individual mistakes into organizational learning so the same errors stop happening.

## Trigger
Use this skill when someone asks about rework patterns, error trends, or subcontractor performance. Common triggers:
- "What are the most common types of rework?"
- "Which subcontractor has the most errors?"
- "Show me the root cause breakdown"
- Any request starting with @rework-analyst

## Core Capabilities

### Step 1: Gather Historical Issue Data
- Collect all flagged issues from @site-risk-scanner reports
- Collect all discrepancies from @plan-checker reports
- Pull any rework logs, punch lists, or deficiency reports from Google Drive or Sheets
- Note the date range being analyzed

### Step 2: Categorize by Root Cause
Classify each rework event into one of these root cause categories:
- Plan misread -- The subcontractor misinterpreted the drawings
- Scheduling conflict -- Work was done out of sequence, causing conflicts between trades
- Material defect -- Wrong or defective materials were used
- Trade coordination failure -- Handoff between trades was not coordinated properly
- Specification change -- A change order was issued but not communicated to the field
- Skill gap -- The work quality suggests a training or experience issue
- Inspection gap -- The issue should have been caught earlier but was missed
- Environmental -- Weather, site conditions, or external factors caused the issue

### Step 3: Identify Patterns
Look across all categorized issues for:
- Which root cause category is most frequent?
- Which subcontractor or trade appears most often?
- Which building area or floor has the most issues?
- Are certain types of errors clustered in time (suggesting a systemic event)?
- Are there recurring pairs (e.g., electrical issues always follow framing delays)?

### Step 4: Estimate Cost Impact
For each pattern identified:
- Estimate the rework cost (labor hours to fix, material waste, schedule delay)
- Rank patterns by total cost impact, not just frequency
- A single expensive rework type matters more than many cheap ones

### Step 5: Build Subcontractor Scorecards
For each subcontractor on the project:
- Total issues attributed to their work
- Breakdown by severity (Critical / Major / Minor)
- Most common root cause for their errors
- Trend over time (improving, stable, or getting worse)

### Step 6: Generate Rework Analysis Report

## Output Format

REWORK ANALYSIS REPORT
Date: [date]
Project: [project name]
Analysis period: [date range]
Total issues analyzed: [count]

TOP REWORK PATTERNS (by estimated cost impact):
1. [Pattern name]
   Frequency: [X occurrences]
   Root cause: [category]
   Estimated cost: [dollar amount or labor hours]
   Affected trades: [which trades]
   Prevention: [specific recommendation to stop this from recurring]

ROOT CAUSE BREAKDOWN:
| Category | Count | % of Total | Est. Cost Impact |
|----------|-------|------------|-----------------|
| [category] | [X] | [Y%] | [amount] |

SUBCONTRACTOR SCORECARDS:
| Subcontractor | Issues | Critical | Major | Minor | Trend |
|--------------|--------|----------|-------|-------|-------|
| [name] | [X] | [Y] | [Z] | [W] | [up/down/flat] |

TOP 3 RECOMMENDATIONS:
1. [Most impactful change to reduce rework]
2. [Second most impactful]
3. [Third most impactful]

## Validation Rules
- Never blame a subcontractor without specific evidence linking them to the issues
- Always include the data source and time period so findings can be verified
- Recommendations must be specific and actionable -- not "improve quality" but "add a pre-installation checklist for electrical rough-in to catch the 3 most common misreads"
- If the data set is too small to identify reliable patterns (fewer than 10 issues), say so explicitly
- Cost estimates should be labeled as estimates, not presented as exact figures
