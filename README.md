# P-0222 UV Floor PCB - Complete Design

This repository contains complete PCB design work for Satview Broadband Ltd. under Logic Reliance project execution criteria.

## What Is Being Done
- Electrical calculations for sizing, protection, and design validation.
- Schematic definition and refinement of the UV Floor Sanitization Unit.
- PCB layout development and implementation.
- Power and behavior simulations to support engineering decisions.
- Technical documentation aligned with project requirements and acceptance criteria.

## Project Context
- Project code: P-0222
- Project name: UV Floor Sanitization Unit
- Design scope: Calculations, schematics, layout, simulations, and full board definition.

## Repository Contents

This section describes the current repository organization and must be updated whenever the folder structure changes.

Top-level folders:
- `.github/`: local repository automation and assistant instructions.
- `docs_logic_reliance/`: company process references and templates.
- `pcb_0222/`: KiCad project files (schematic, PCB, project settings, and local libraries), including temporary library-copy artifacts used during review cycles.
- `project_docs/`: project technical documentation and engineering evidence.

Main content under `project_docs/`:
- `design/`: implementation notes, design outputs, and engineering artifacts.
- `datasheets/`: component manufacturer datasheets used by the design.
- `references/`: external technical references and review support documents.
- `requirements/`: PRD and processor requirements for the project.

Current notable areas under `project_docs/datasheets/`:
- `mcu/`: MCU package files, symbols, and footprint source assets.
- `pmos/`: PMOS documentation assets under replacement/review.
- `rotary/`: rotary switch documentation assets under replacement/review.
- `debugger/`: debug and programming interface datasheets.

Current content under `project_docs/design/`:
- `mcu_boot/`: MCU boot implementation report and programming path status.
- `mcu_pinout/`: processor pinout definition and revision-controlled spreadsheet.
- `power_supply/`: power supply design output documents.

## Responsible Engineer
- Ing. Vega Maximiliano

## General Project Updates
- 2026-07-27: KiCad project files are uploaded. Current schematic status: SCH without MCU (MCU section pending).
- 2026-07-28: Added an MCU boot and programming strategy note with selected nBOOT_SEL behavior, SWD as primary path, and provisional USART/I2C recovery alternatives.
- 2026-07-28: Revised MCU boot policy note to remove external BOOT0 pull-down requirement and align default reset behavior with STM32C0 internal pull configuration.
- 2026-07-28: Project documentation inventory was updated to reflect the current `project_docs/design/` structure and newly added MCU-related assets.
- 2026-07-29: Footprint-related assets and supporting datasheet packages are in active review; replacement files and library-copy artifacts were added for validation before final consolidation.
