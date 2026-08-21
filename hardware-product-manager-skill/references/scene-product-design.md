# Scene-Driven Product Design

## Objective

Translate validated scenes into product requirements without confusing a scene with a feature list.

The product should solve the important job in the core scene with the minimum necessary complexity.

## Translation Chain

Scene → Job → Friction / Failure → Desired Outcome → Product Principle → Requirement → Test Method

Example:

Bedroom charging → reliably charge before sleep → user may misalign the phone → charging should begin without careful positioning → easy alignment → magnetic alignment / placement tolerance requirement → alignment success-rate test.

## Scene Requirement Matrix

For every important scene capture:

- Scene role
- User
- Trigger
- Job
- Friction / failure
- Desired outcome
- Competitor performance
- Product response
- Requirement priority
- Requirement metric
- Validation method

## Product + Content + Service Rule

A user problem may require more than hardware, but only add non-hardware elements when they materially improve the product experience.

Possible solution layers:

- Hardware
- Firmware
- Accessories
- Setup / instructions
- Service / support

Do not add marketing content as a substitute for weak product performance.

## Scene-to-Spec Rule

A scene should influence specifications only when the connection is explicit.

Examples:

- Quiet bedroom → acoustic-noise requirement
- Dark bedroom → indicator-light requirement
- Travel → size / weight / cable-storage requirements
- One-hand use → stability / removal-force requirements
- Outdoor use → ingress / temperature / drop requirements

Do not use vague requirements such as “bedroom friendly.” Convert them into measurable product behavior.

## Core vs Supporting Scene Tradeoff

When requirements conflict:

1. Protect the Core Scene
2. Protect Category Entry Requirements
3. Protect Must-Win attributes
4. Support secondary scenes only if cost and complexity remain acceptable

Document the tradeoff instead of silently compromising every scene.

## Competitive Scene Benchmark

Compare competitors inside the same scene, not only on feature sheets.

Example dimensions:

- task success
- number of user steps
- time to completion
- reliability
- noise
- heat
- visibility / light
- placement tolerance
- compatibility
- one-hand interaction
- occupied space

A specification is valuable only if it improves a meaningful user outcome or is necessary for category parity.

## Validation During EVT / DVT

EVT should test whether the engineering architecture can support the scene-critical requirements.

DVT should test the final product in representative scene conditions and compare Must-Win claims against benchmark products under comparable conditions.

If the product fails the core scene, do not compensate by adding unrelated features.

## Required Output

For `/define`, `/prd`, or `/spec`, provide a Scene Requirement Matrix when scene-driven requirements are important.

For each requirement show:

Scene → User Problem → Desired Outcome → Requirement → Metric → Priority → Benchmark → Validation
