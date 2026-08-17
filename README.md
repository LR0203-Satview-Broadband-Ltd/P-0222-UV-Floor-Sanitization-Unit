# P-0222 | UV Floor Sanitization Unit

> Low-voltage custom PCB replacing an Arduino-based prototype for a hospital UV floor sanitization platform.

| Project | Status | Current package | Owner |
| --- | --- | --- | --- |
| P-0222 | Layout review pending | Preliminary manufacturing package generated | Ing. Vega Maximiliano |

## Project Overview

Satview Broadband Ltd. is developing a UV foot-sanitizing floor unit for hospital environments. This project replaces the prototype controller with a professional PCB that manages the UV cycle, relay actuation, protected 24 VDC input, power regulation, timer selection, and external component connections.

The design is developed under Logic Reliance engineering processes and follows the project requirements, acceptance criteria, and KiCad library governance defined for the work.

## Current Status

The PCB layout has not yet passed formal review. A preliminary manufacturing package has been generated to support the upcoming layout review and early manufacturing feedback; it is not an approved production release.

### Preliminary Package Contents

- BOM: 40 grouped entries and 70 component references.
- Assembly positions: DNP components excluded from the pick-and-place output.
- Component sourcing: manufacturer, MPN, and DigiKey fields populated in the current EBOM.
- Fabrication outputs: Gerbers, ODB++, PTH/NPTH drills, assembly files, drawings, and 3D model present.
- Surface finish: `ENEPIG`.
- Board UID and board specifications added to the `F.Fab` layer and assembly drawing.
- Manufacturing drill outputs: duplicate PTH/NPTH files removed.
- Logic Reliance BOM workbook: editable Excel version generated from the KiCad CSV.

### Release Conditions

- Complete and approve the formal layout review.
- Assign the formal board revision in the Gerber job file, which currently reports `Revision: rev?`.
- Regenerate and review the manufacturing outputs after approval before releasing them to a supplier.

## Technical Scope

- Requirements traceability and acceptance criteria.
- Electrical sizing and power regulation validation.
- STM32C011F6 MCU control.
- Relay-driven UV load switching.
- Reverse-polarity, surge, fuse, and transient protection.
- Configurable cycle timer through DIP switches.
- KiCad schematic capture, PCB layout, manufacturing outputs, and supporting evidence.

## Design Boundaries

This iteration includes the low-voltage PCB only.

Out of scope:

- 120 VAC design, which remains within the external certified power supply.
- Mechanical enclosure design.
- Regulatory certification.
- UV strip sourcing and final optical characterization.

## Manufacturing Package

The current package is delivered as:

`pcb_0222/outputs/Manufacture/20260816-P_0222_manufacture.zip`

| Directory or file | Purpose |
| --- | --- |
| `3D/` | STEP model and board snapshot |
| `ASM/` | Pick-and-place positions and assembly layers |
| `BOM/` | KiCad EBOM CSV and Logic Reliance Excel BOM |
| `DRILLS/` | Plated and non-plated drill files |
| `DWG/` | Schematic and assembly drawings |
| `GBR/` | Gerber layers and fabrication job file |
| `pcb_0222-odb.zip` | ODB++ fabrication exchange package inside the manufacturing package |

The archive contains the editable company-format BOM, fabrication outputs, assembly files, drawings, and 3D model.

## Repository Contents

This is the controlled inventory of publishable project content. Local process notes, AI working files, and internal assistant configuration are intentionally excluded from publication.

| Directory | Contents |
| --- | --- |
| `pcb_0222/` | KiCad project, schematic, PCB, local library assets, and manufacturing outputs |
| `project_docs/design/` | MCU boot, pinout, power supply, and implementation records |
| `project_docs/datasheets/` | Manufacturer datasheets and component package evidence |
| `project_docs/references/` | External technical references used for engineering decisions |
| `project_docs/requirements/` | Released PRD and processor requirements |

### Design Records

- `mcu_boot/`
- `mcu_pinout/`
- `power_supply/`

### Datasheet Categories

`buttons/` · `conectors/` · `debugger/` · `dipswitch/` · `inductor/` · `leds/` · `mcu/` · `nails/` · `npn/` · `pmos/` · `pptc/` · `psu/` · `relay/` · `rotary/` · `tvs/` · `xtal/` · `zenner/`

Some directory names preserve legacy spelling for traceability, including `conectors/` and `zenner/`.

## Key Documents

- [Project context baseline](p-0222.md)
- [Released PRD](project_docs/requirements/PRD%20v1.0.md)
- [Processor requirements](project_docs/requirements/Processor%20Requirements.md)
- [MCU boot and programming records](project_docs/design/mcu_boot/)
- [MCU pinout records](project_docs/design/mcu_pinout/)
- [Power supply records](project_docs/design/power_supply/)

## General Project Updates

- 2026-07-27: KiCad project files were uploaded and the schematic baseline was published.
- 2026-07-28: SWD programming guidance and STM32C0 BOOT0 handling were documented.
- 2026-07-29: Footprint and datasheet review entered the active validation cycle.
- 2026-07-30: Placement outputs, drawings, STEP model, and exchange artifacts were refreshed.
- 2026-08-02: Schematic review comments were incorporated into the PCB and manufacturing outputs.
- 2026-08-09: Layout placement and routing review continued with synchronized schematic and PCB updates.
- 2026-08-11: The active layout iteration was prepared for formal review.
- 2026-08-16: A preliminary manufacturing package was generated to support the pending layout review; it is not approved for supplier release.
- 2026-08-16: Board UID and board specifications were added to the `F.Fab` layer and assembly drawing to improve manufacturing traceability.
