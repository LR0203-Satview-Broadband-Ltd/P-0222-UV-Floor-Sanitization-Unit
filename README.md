# P-0222 UV Floor PCB Design Repository

## Overview
This repository contains hardware design deliverables for project P-0222 (UV Floor Sanitization Unit) developed for Satview Broadband Ltd. under Logic Reliance engineering processes.

## Project Identification
- Project code: P-0222
- Project name: UV Floor Sanitization Unit
- Primary discipline: PCB hardware design
- Design scope: requirements traceability, calculations, schematic capture, layout development, and supporting technical documentation

## Technical Scope
- Electrical design calculations and sizing validation
- Schematic definition and iterative review
- PCB implementation and packaging decisions
- Supporting simulation outputs and reference material
- Design documentation aligned with project requirements and acceptance criteria

## Repository Structure (Current Baseline)
This section is a controlled inventory and must be updated when directories are added, removed, or renamed.

Top-level directories:
- `.github/`: repository-local automation and assistant instruction assets
- `docs_logic_reliance/`: company process references and templates
- `pcb_0222/`: KiCad project files (schematic, PCB, project configuration, and local library artifacts)
- `project_docs/`: project evidence package (requirements, design notes, references, and datasheets)

Main directories under `project_docs/`:
- `design/`: implementation reports, pinout definitions, and design outputs
- `datasheets/`: component manufacturer documentation and package assets
- `references/`: external technical references used for engineering decisions
- `requirements/`: PRD and processor requirement documents

Directories currently present under `project_docs/design/`:
- `mcu_boot/`
- `mcu_pinout/`
- `power_supply/`

Directories currently present under `project_docs/datasheets/`:
- `buttons/`
- `conectors/`
- `debugger/`
- `dipswitch/`
- `inductor/`
- `leds/`
- `mcu/`
- `nails/`
- `npn/`
- `pmos/`
- `pptc/`
- `psu/`
- `relay/`
- `rotary/`
- `tvs/`
- `xtal/`
- `zenner/`

## Current Technical Status
- Schematic and footprint assets are under active review.
- MCU boot/programming policy documentation is available in `project_docs/design/mcu_boot/`.
- Replacement datasheet packages have been incorporated for component review cycles.

## Responsible Engineer
- Ing. Vega Maximiliano

## General Project Updates
- 2026-07-27: KiCad project files were uploaded; schematic baseline was published with pending MCU section completion.
- 2026-07-28: MCU boot/programming note was added with SWD as primary path and provisional USART/I2C recovery alternatives.
- 2026-07-28: MCU boot policy note was revised to align BOOT0 handling with STM32C0 internal reset pull behavior.
- 2026-07-28: Documentation inventory was aligned to the `project_docs/design/` structure.
- 2026-07-29: Footprint and related datasheet assets entered active review, including replacement files for validation.
