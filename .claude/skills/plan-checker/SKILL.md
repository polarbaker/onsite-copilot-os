# Skill: Plan Checker

## Purpose
Compare photographs of completed or in-progress construction work against the original architectural drawings and specifications. Identify discrepancies between what was designed and what was actually built.

## Trigger
Use this skill when someone wants to verify that built work matches the plans. Common triggers:
- "Compare this photo to the plans"
- "Does this framing match drawing A-201?"
- "Check if the HVAC installation matches specs"
- Any request starting with @plan-checker

## Core Capabilities

### Step 1: Gather Reference Documents
- Identify which architectural drawing, specification section, or detail applies to the work being checked
- Retrieve the relevant plan sheets from Google Drive
- If the correct drawing is not clear, ask which plan sheet or specification section to compare against

### Step 2: Identify What Was Built
From the site photo(s), document what is visible:
- What trade or system is shown (framing, electrical, plumbing, HVAC, finish, etc.)
- What stage the work appears to be in
- Key measurements or proportions that can be estimated from the photo
- Materials visible in the photo

### Step 3: Compare Against Plans
Check the photo against the reference drawing for discrepancies:
- Dimensional: Does the spacing, sizing, or positioning match what the plans call for?
- Material: Are the visible materials consistent with what was specified?
- Location: Is the element installed where the plans say it should be?
- Configuration: Is the arrangement (routing, orientation, connections) correct?
- Completeness: Are all elements shown on the plans present in the photo?

### Step 4: Assess Work Status
Before calling something a discrepancy, check:
- Is this trade marked as complete, or is it still in progress?
- Could the apparent discrepancy be explained by a later construction step?
- Is there an RFI or change order that might have modified the original plan?
If the work is clearly unfinished, note it as "in progress -- verify when complete" rather than a discrepancy.

### Step 5: Rate Each Discrepancy
- Critical -- Structural or safety implication. Must be resolved before work continues.
- Major -- Will require rework if not corrected. Does not match plans in a meaningful way.
- Minor -- Small deviation that may be within acceptable tolerance. Document and monitor.
- Pass -- Work matches plans within normal construction tolerances.

### Step 6: Generate Comparison Report
Compile into a structured comparison.

## Output Format

PLAN CHECK REPORT
Date: [date]
Location: [building/floor/area]
Trade: [what type of work]
Reference drawing: [sheet number and detail]
Status: [PASS / DISCREPANCIES FOUND]

COMPARISON:
Plan says: [what the drawing specifies]
Site shows: [what the photo reveals]
Match: [Yes / No / Partial]

DISCREPANCIES:
1. [CRITICAL/MAJOR/MINOR] -- [Short description]
   Plan reference: [drawing sheet, detail number, or spec section]
   Expected: [what should be there per plans]
   Actual: [what the photo shows]
   Impact: [why this matters]
   Action: [what to do about it]

CONFIDENCE: [High / Medium / Low]
Reason: [why confidence is at this level -- photo quality, angle, etc.]

## Validation Rules
- Always reference the specific drawing sheet and detail number being compared against
- Never claim a match or mismatch without explaining what you compared
- If photo angle or quality makes comparison impossible, say so and request better imagery
- Confidence level must be included -- if the comparison is uncertain, do not present it as definitive
- Distinguish between "does not match plans" and "cannot determine from this photo"
