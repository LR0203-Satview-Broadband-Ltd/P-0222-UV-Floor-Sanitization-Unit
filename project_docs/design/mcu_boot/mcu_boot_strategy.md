# STM32C011F6P6 Boot and Programming Implementation Report

## Scope
This report summarizes the boot architecture and firmware programming interfaces currently implemented for the STM32C011F6P6 in project P-0222, and identifies provisional alternatives retained for recovery scenarios.

## Implemented Boot Configuration
- The selected option-byte configuration is nBOOT_SEL = 0.
- Under this configuration, BOOT0 is sampled during reset.
- The intended default behavior is direct startup from user Flash in normal operation.

## Implemented Hardware Behavior (No External Tool Connected)
- No external pull-down resistor was implemented on PA14/BOOT0.
- This implementation is aligned with STM32C0 reset behavior documented by ST: after reset, PA14 is configured for SWD alternate function and an internal pull-down on PA14 is enabled, while an internal pull-up on PA13 is enabled.
- Based on this behavior, the default reset condition keeps BOOT0 at a defined low level and the device boots from user Flash.
- The NRST network includes a local 100 nF capacitor from PF2/NRST to GND, placed close to the MCU.
- Manual reset pushbutton provision on NRST remains optional.

## Implemented Primary Programming Interface (SWD)
SWD was defined as the primary programming and debug interface using ST-LINK/V2, ARM20-CTX, and TC2030-IDC.

TC2030 6-pin assignment:

| TC2030 pad | SWD signal | STM32C011F6P6 pin |
| --- | --- | --- |
| 1 | VREF | VDD |
| 2 | SWDIO | PA13 |
| 3 | NRST | PF2/NRST |
| 4 | SWCLK | PA14/BOOT0 |
| 5 | GND | VSS |
| 6 | SWO/TDO | Not connected |

Associated electrical criteria:
- VREF is used by ST-LINK for target I/O level detection; the target board is externally powered during programming.
- SWDIO, SWCLK, NRST, and GND are routed as short and low-noise connections to improve debug robustness.

## Provisional Recovery Alternatives (System Memory Bootloader)
The following interfaces remain available as provisional recovery/update options when SWD access is not available.

### Bootloader Entry Condition
- BOOT0 forced high during reset.
- NRST toggled with nBOOT_SEL = 0 active.
- Resulting mode: System Memory bootloader.

### Provisional Alternative A: USART
- Reserved access points: PA11, PA12, GND.
- Intended usage: temporary firmware recovery/programming path.

### Provisional Alternative B: I2C
- Reserved access points: PB6 (I2C1_SCL), PB7 (I2C1_SDA), GND.
- Electrical condition: external pull-ups on SCL and SDA, nominal 4.7 kOhm to VDD.

## Consolidated Status
- Implemented as baseline: SWD programming/debug and Flash boot in normal operation.
- Retained as provisional: USART and I2C bootloader-based recovery paths.

## Pending Technical Validation
Before design release, final verification remains required against the latest STM32C011F6P6 documentation set (datasheet and AN2606), specifically for System Memory interface mapping and boot-mode behavior by package and silicon revision.
