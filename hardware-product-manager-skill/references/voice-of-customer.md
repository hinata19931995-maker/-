# Voice of Customer (VOC) Research

## Objective

Discover real user problems before defining solutions or features.

VOC research should convert raw user language into evidence-backed problem statements and product opportunities.

Do not use VOC merely to confirm an existing product idea.

## Core Principle

Follow this sequence:

Raw Voice → Context → Problem Code → Problem Cluster → Frequency → Severity → Existing Solution → Workaround → Root-Cause Hypothesis → Opportunity → Validation

Preserve traceability to original evidence whenever possible.

## Evidence Sources

Use multiple sources when available:

1. E-commerce reviews, especially 1–3 star reviews
2. Product Q&A and pre-purchase questions
3. Reddit, forums, communities, and public discussions
4. Customer service tickets and warranty cases
5. Return reasons and refund reasons
6. User interviews
7. Direct observation / contextual inquiry
8. Existing product usage data where available

Do not treat any single source as complete representation of the market.

## Research Order for New Consumer Electronics

Default sequence:

1. Select 10–20 relevant competitors or substitutes
2. Collect a sufficiently broad sample of user voices
3. Preserve original text and source/context
4. Code individual problems
5. Merge semantically equivalent codes
6. Separate symptoms from likely root causes
7. Quantify recurring patterns where the dataset supports it
8. Identify user workarounds
9. Rank problems
10. Convert the strongest problems into opportunity hypotheses
11. Validate high-impact hypotheses before product definition

Do not invent sample sizes or frequency percentages when complete source data is unavailable.

## VOC Coding

For each meaningful user statement capture:

- Source
- Product / competitor
- Rating if applicable
- Date if available
- Original voice
- Usage scenario
- User task
- Problem code
- Problem cluster
- Symptom
- Likely root cause
- Severity
- Existing solution
- Workaround
- Desired outcome
- Evidence level

One review may contain multiple independent problems. Split them when necessary.

## Problem vs Feature

Translate feature requests into underlying jobs or problems.

Example:

Raw voice: "I wish there were a button to turn off the LED."

Do not immediately define:

> Add an LED-off button.

Instead infer the problem:

> Persistent status lighting may disturb nighttime use.

Then evaluate alternative solutions such as automatic dimming, timeout, ambient-light sensing, or no persistent LED.

## Symptom vs Root Cause

Do not merge all similar symptoms prematurely.

Example:

"It doesn't charge" may originate from:

- Alignment failure
- Case interference
- Unsupported protocol
- Insufficient power adapter
- Thermal protection
- Defective hardware

Keep root-cause conclusions as [HYPOTHESIS] until supported by evidence.

## Workaround Signal

User-created workarounds are strong signals.

Examples:

- Covering a bright LED with tape
- Repositioning a device repeatedly
- Removing a phone case before charging
- Buying a separate adapter
- Adding padding or spacers

A workaround indicates that the user is paying a behavioral cost to solve the problem.

## Interview Rule

Prefer questions about real past behavior over hypothetical feature requests.

Ask:

- Tell me about the last time this happened.
- What were you trying to do?
- What happened?
- How did you notice the problem?
- What did you do next?
- How often does this happen?
- What do you use instead?
- Have you spent money or time trying to solve it?

Avoid leading questions such as:

> Would you like a product with feature X?

## Problem Scoring

Evaluate each problem using:

- Frequency
- Severity
- Dissatisfaction with existing solutions
- Solvability
- Willingness to pay / behavioral evidence
- Evidence strength

A practical conceptual model is:

Problem Opportunity = Frequency × Severity × Dissatisfaction × Solvability × Willingness-to-Pay Signal

Do not manufacture a precise numeric score when inputs are qualitative or incomplete. In that case use High / Medium / Low and explain the evidence.

## Evidence Strength

Classify conclusions as:

- [DATA] Directly observed in collected user voices
- [PATTERN] Repeated across multiple independent voices or sources
- [HYPOTHESIS] Inferred underlying need or root cause
- [VALIDATED] Confirmed through additional evidence, interview, test, or experiment

Never label an AI inference as validated user demand.

## Opportunity Ranking

For each top problem report:

| Rank | User Problem | Scenario | Frequency | Severity | Existing Solution | Workaround | Evidence Strength | Opportunity |
|---|---|---|---|---|---|---|---|---|

Prioritize problems that are frequent, severe, poorly solved, realistically solvable, and commercially meaningful.

## Required VOC Output

When `/VOC` is requested, default to:

1. Research Scope
2. Sources and Sample Limitations
3. Raw VOC Themes
4. Problem Coding / Clusters
5. Top User Problems
6. Usage Scenarios
7. Workarounds
8. Symptom vs Root-Cause Analysis
9. Problem Ranking
10. Opportunity Hypotheses
11. Contradictory Evidence
12. Unknowns / Research Gaps
13. Recommended Validation
14. Implications for Product Definition

## Guardrails

Never:

- Invent reviews or quotes
- Invent review counts or percentages
- Treat marketplace star ratings as proof of a specific need
- Treat one loud complaint as a market-wide problem
- Convert every complaint into a feature
- Remove contradictory evidence
- Present root-cause inference as fact
- Claim willingness to pay without evidence

Always distinguish raw evidence from interpretation.

## Handoff to Product Validation

VOC should feed `/validate`.

The handoff should contain:

- Top 3–10 evidence-backed user problems
- Core usage scenarios
- Important workarounds
- Unresolved root-cause hypotheses
- Evidence strength
- Opportunity hypotheses
- Key unknowns

Then `/validate` determines whether those problems support a desirable, differentiated, feasible, manufacturable, compliant, and profitable product.