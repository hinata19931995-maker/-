# Competitive Intelligence

## Objective

Treat competitor and substitute analysis as a continuous evidence stream across the full hardware product lifecycle, not as a one-time market-research task.

Competitive intelligence should answer two questions:

1. What user problems are competitors already solving well?
2. Where is there still a meaningful gap that our product can win?

User pain alone does not prove a market opportunity. A stronger opportunity requires both meaningful user dissatisfaction and a competitive gap.

## Core Principle

Use two evidence lines in parallel:

User Evidence: Scene → JTBD → VOC → Problems → Unmet Needs

Competitive Evidence: Competitors → Substitutes → Positioning → Specs → Price → Reviews → Technology → Cost Signals → Benchmark Performance → Market Changes

Combine them before major product decisions.

A practical conceptual model is:

Product Opportunity = User Importance × User Dissatisfaction × Competitive Gap × Solvability × Economics

Use this as a reasoning framework, not fake mathematical precision.

## Competitor Universe

Do not only study products that look identical.

Classify:

1. Direct competitors
2. Indirect competitors
3. Substitute products
4. Substitute behaviors
5. Emerging technologies
6. Adjacent-category products that may enter the job space

## Benchmark Product Set

For each active project, maintain approximately 5–10 relevant benchmark products when possible.

Include representative roles such as:

- Market Leader
- Price Leader
- Feature Leader
- Design Leader
- Best Rated / Strong User Satisfaction
- Emerging / Fast-moving Challenger
- Direct Substitute

A single product may represent more than one role.

Do not force every role when evidence is unavailable.

## Competitive Intelligence by Product Stage

### 1. Scene / Opportunity Discovery

Study:

- What products are already present in the scene?
- What substitutes do users use?
- Which jobs are already well served?
- Which jobs require multiple products or workarounds?
- Where are users paying a premium for partial solutions?

Output:

- Competitor landscape
- Substitute map
- Initial competitive gaps

### 2. VOC / Problem Discovery

Use competitor reviews, Q&A, returns, forums, and public discussions to determine:

- Repeated complaints
- Repeated praise
- Workarounds
- Expectations that competitors consistently meet
- Problems competitors consistently fail to solve

Do not assume a complaint remains an opportunity if another competitor already solves it well.

### 3. Product Validation

Before GO / CONDITIONAL GO / NO-GO, evaluate:

- Is the problem still poorly solved?
- How crowded is the market?
- Is the proposed differentiation meaningful to users?
- Can competitors copy it quickly?
- Does the target price leave room for a viable business?

### 4. Product Definition

Classify competitive requirements as:

- Category Entry Requirement — users expect it; missing it creates rejection
- Must Match — product should be competitive but does not need to lead
- Must Win — deliberate product advantage
- Acceptable Lag — allowed to be weaker because it is not central to positioning
- Irrelevant — do not spend cost or complexity here

This prevents feature-by-feature copying and specification arms races.

### 5. PRD / Specification

Use benchmark products to define measurable targets.

Examples:

- Charging time
- Thermal behavior
- Noise
- Battery life
- RF range
- Latency
- Force
- Weight
- Dimensions
- Compatibility
- Reliability
- Setup time
- One-handed operation

Whenever possible, define the test method, not only the target number.

### 6. Cost / BOM

Use market pricing and product architecture to challenge assumptions about:

- Target retail price
- Target landed cost
- Target BOM
- Feature cost
- Packaging cost
- Included accessories

Do not claim competitor BOM or factory cost as fact unless supported by reliable evidence.

### 7. Supplier / RFQ

Ask suppliers:

- Whether similar platforms already exist
- Which competitor-like architectures they manufacture
- Which functions are standard vs custom
- Key component differences
- Tooling implications
- Certification status
- Cost delta for benchmark features

Do not request or misuse confidential competitor information.

### 8. EVT / DVT

Use physical competitive benchmarking where appropriate.

Compare our product against the benchmark set under controlled, repeatable conditions.

DVT should answer:

- Do we meet category-entry requirements?
- Do we match where we promised parity?
- Do we win where our positioning says we must win?
- Are any competitive weaknesses severe enough to block launch?

Read `references/competitive-benchmarking.md` for detailed rules.

### 9. PVT / MP

Competitor analysis is not the main gate, but verify that manufacturing changes have not destroyed the intended competitive advantage.

Example:

- Cost-down material increases noise
- Process variation reduces charging alignment
- Alternate component worsens thermal behavior

### 10. Launch

Recheck:

- Current price
- Promotions
- New models
- Listing claims
- Bundles
- User rating trends
- Review themes
- Key specification changes

Do not launch against a competitive landscape that is months out of date when the category changes quickly.

### 11. Post-launch / Next Generation

Monitor:

- Competitor launches
- Price changes
- New protocols / technology
- New user complaints
- Competitors copying our differentiation
- Changes in marketplace expectations

Feed meaningful changes into `/feedback`, `/VOC`, `/validate`, or the next-generation product definition.

## Competitive Gap Types

Classify gaps as:

- Performance Gap
- Reliability Gap
- UX Gap
- Scenario Gap
- Price / Value Gap
- Design Gap
- Compatibility Gap
- Ecosystem Gap
- Service / Warranty Gap
- Manufacturing / Quality Gap

A gap is only attractive if users care about it and the business can realistically exploit it.

## Evidence Discipline

For competitor data, record whenever possible:

- Product
- Brand
- Market / country
- Source
- Date observed
- Price and whether promotional
- Specification source
- Review source
- Test method if measured
- Confidence

Never fabricate:

- Price
- Sales volume
- Review count
- Rating
- Market share
- Specification
- BOM
- Supplier identity

Mark estimates clearly.

## Refresh Triggers

Refresh competitive intelligence when:

- A major competitor launches a new model
- A protocol / platform changes
- Target retail price changes materially
- Product definition changes materially
- Before design freeze
- Before launch
- Meaningful post-launch market changes appear

## Required Output for /competitors

Adapt depth to project stage, but normally include:

1. Research Scope
2. Competitor Universe
3. Benchmark Product Set
4. Positioning Map
5. Price / Value Map
6. Feature and Specification Comparison
7. User Praise / Complaint Comparison
8. Category Entry Requirements
9. Must-Match / Must-Win / Acceptable-Lag Areas
10. Competitive Gaps
11. Substitute Threats
12. Evidence Quality and Unknowns
13. Implications for Product Definition
14. Next Competitive Validation

## Guardrails

Never:

- Copy every competitor feature
- Treat the market leader as automatically correct
- Confuse high specification with high user value
- Claim a gap without checking current alternatives
- Ignore substitute behaviors
- Use outdated competitive information without labeling the date
- Treat competitor weakness as an opportunity unless users care

The purpose of competitive intelligence is better product decisions, not a larger comparison table.
