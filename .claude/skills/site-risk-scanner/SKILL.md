# Skill: Site Risk Scanner

## Purpose
Analyze construction site photos and video to identify safety hazards, quality risks, and deviations from standard building practices. This is the first-pass safety and quality check on incoming field imagery.

## Trigger
Use this skill when someone uploads site photos or asks you to check field imagery for risks. Common triggers:
- "Scan these photos for risks"
- "Check today's site photos"
- "Are there safety issues in these images?"
- Any request starting with @site-risk-scanner

## Core Capabilities

### Step 1: Receive and Organize Photos
- Accept photos from Google Drive (folder link or individual files)
- Note the date, location on site, and which trade or area is shown
- If this information is not provided, ask for it before proceeding

### Step 2: Visual Safety Scan
Look at each photo for common construction safety and quality issues:
- Structural: Misaligned beams, cracked concrete, improper bracing, sagging forms
- Electrical: Exposed wiring, missing junction box covers, improper conduit routing
- Safety: Missing guardrails, fall hazards, blocked exits, missing signage, improper scaffolding
- Material: Visible water damage, wrong material type, corroded fasteners, damaged supplies
- Housekeeping: Excessive debris, blocked pathways, improper material storage

### Step 3: Classify Each Finding
For every issue spotted, assign a severity:
- Critical -- Immediate safety risk or code violation that could cause injury. Requires stop-work consideration.
- Major -- Significant quality issue that will likely require rework if not addressed soon. Needs attention this week.
- Minor -- Small issue that should be noted and monitored. Can be addressed in normal workflow.

### Step 4: Check for Work-in-Progress
Before flagging something as an issue, consider whether the work might simply be unfinished:
- Is the trade still active in this area?
- Are there signs of ongoing work (tools present, partial installations)?
- Would this look normal at an intermediate stage of the process?
If the answer is yes, note it as "work in progress -- monitor" rather than flagging it as a defect.

### Step 5: Generate Risk Report
Compile findings into a structured report.

## Output Format

For each photo analyzed, produce:

SITE RISK REPORT
Date: [date]
Location: [building/floor/area]
Photos reviewed: [count]

FINDINGS:
1. [CRITICAL/MAJOR/MINOR] -- [Short description]
   Photo: [which photo]
   Location in photo: [where to look]
   Issue: [what is wrong and why it matters]
   Action: [what should be done]

SUMMARY:
- Critical: [count]
- Major: [count]
- Minor: [count]
- Work in progress (monitored): [count]

## Validation Rules
- Never flag work-in-progress as a defect without explicitly noting uncertainty
- Every finding must reference a specific photo and location
- Every finding must include a recommended action
- If no issues are found, say so clearly -- do not invent problems
- If photo quality is too low to make a determination, say that instead of guessing
