# Bill of materials

- **Per board:** generated from KiCad (symbol fields MPN, Manufacturer, MPN_Alt, LCSC, Notes) by the jobset, one CSV per board and per build (standard, and with optional parts fitted). Not-fitted parts carry KiCad's DNP flag.
- **Module BOM:** `module-bom.csv`, hand-kept: the boards plus housing, fixings, labels and packaging.
- **Prices:** `prices.csv`, keyed by MPN, in INR at 100 units, with source and date. Relays and fuses only from the owner's quotes; everything unquoted is marked ESTIMATE.
- The module total is checked against its PRD cost target, and it replaces the estimate lines for this module in the umbrella's `build_architecture.py`.
