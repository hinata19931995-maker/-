# Hardware Product Manager Skill

A maintainable Agent Skill repository for consumer-electronics product development.

## Structure

```text
hardware-product-manager-skill/
├── SKILL.md
├── README.md
├── references/
│   ├── product-discovery.md
│   ├── product-definition.md
│   ├── cost-and-bom.md
│   ├── development-gates.md
│   ├── compliance-and-quality.md
│   └── decision-framework.md
├── templates/
│   ├── PRD-template.md
│   ├── product-definition-template.md
│   ├── RFQ-template.md
│   ├── EVT-template.md
│   ├── DVT-template.md
│   ├── PVT-template.md
│   ├── BOM-template.csv
│   ├── FMEA-template.csv
│   ├── risk-register-template.csv
│   ├── supplier-scorecard-template.csv
│   └── change-log-template.csv
├── checklists/
│   ├── concept-gate.md
│   ├── design-freeze.md
│   └── mp-readiness.md
└── examples/
    └── wireless-charger-example.md
```

## Design Principle

Keep `SKILL.md` short and stable.

Put detailed domain knowledge in `references/`.

Put reusable deliverables in `templates/`.

Put stage-gate criteria in `checklists/`.

Put sample usage patterns in `examples/`.

This makes the skill easier to maintain than one monolithic prompt.
