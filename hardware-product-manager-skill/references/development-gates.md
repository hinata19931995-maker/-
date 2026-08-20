# Hardware Development Gates

## Development Architecture

Concept → Feasibility → Prototype → EVT → DVT → PVT → MP

Prototype approval is not mass-production readiness.

## EVT

Purpose:

Verify that the engineering architecture works.

Validate:

- Electronics
- PCB
- Firmware
- Mechanical architecture
- Thermal
- RF
- Power
- Charging
- Core functionality

Exit criterion example:

No unresolved P0 engineering defects.

## DVT

Purpose:

Verify that final design meets the PRD.

Validate:

- Functional performance
- Reliability
- Drop
- Temperature
- Humidity
- Battery
- Charging
- RF
- Compatibility
- Materials
- Mechanical life
- UX
- Packaging
- Certification

## PVT

Purpose:

Verify the factory can manufacture consistently.

Validate:

- Production line
- Fixtures
- SOP
- Work instructions
- Cycle time
- Yield
- Calibration
- Firmware flashing
- Serial number
- Traceability
- Packaging
- QC

Track:

- FPY
- Production yield

## Design Freeze

Do not freeze until:

- Core requirements validated
- Major DVT issues resolved
- Cost acceptable
- Tooling risk acceptable
- Certification path confirmed
- Supplier ready
- Critical components secured

## MP Readiness

Approve MP only when:

- PRD passed
- DVT passed
- Critical defects closed
- PVT passed
- Yield acceptable
- QC plan approved
- Critical parts available
- Certifications obtained
- Cost target met

Return:

- MP READY
- MP NOT READY
