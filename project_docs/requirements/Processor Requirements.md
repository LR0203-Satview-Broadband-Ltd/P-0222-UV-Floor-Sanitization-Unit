# Processor Requirements

## Power Requirements

| Parameter | Value |
| --- | --- |
| Battery powered | NO  |
| Battery info |     |
| Battery life |     |
| Sleep / Wake-up |     |
| Operation Voltage | N/A |
| Other |     |

## Peripherals Requirements

Use this table to indicate peripheral requirements.

- **Qty required:** How many peripherals of this kind are required (e.g., 1 SPI, 2 UARTs)
- **Pins used:** How many pins will be required for the peripheral (e.g., 2 UARTs need 4 pins: 2×TX, 2×RX)
- **Notes:** Additional information specific to the given peripheral
- **Total number of pins:** How many pins for all peripherals including GPIOs are needed

| Peripheral | Qty Required | Pins Used | Notes (Any specific requirements?) |
| --- | --- | --- | --- |
| GPIO | 2   | 2   | Switch input |
|     | 1   | 1   | Debug button |
|     | 1   | 1   | Debug LED |
|     | 1   | 1   | Relay output |
|     | 1   | 4   | DIP Switch 1 |
|     | 1   | 2   | DIP Switch 2 |
|     | 1   | 2   | Spare |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
| **Total Number of IOs** |     | 13  |     |

## Wireless Requirements

Use this section in case we are selecting a SoC or Module with wireless capabilities.

| Protocol | Required? | Notes (Any specific requirements?) |
| --- | --- | --- |
| Bluetooth | No  | Bluetooth Classic Profile (SPP 1.1, A2DP, etc)   Bluetooth Low Energy (4.0, 4.2, 5, etc) |
| WiFi | No  | Speed requirements   Firmware requirements (specific protocol / library) |
| Zigbee | No  |     |
| Other? | No  |     |

## Memory and Processing Power

| Parameter | Value |
| --- | --- |
| Flash memory |     |
| EEPROM memory |     |
| RAM memory |     |
| Processor speed |     |
| Programming / Debug | Using TC2030 and inexpensive programmer |
| In-field firmware update |     |
| Other |     |

## Other Requirements

| Parameter | Value |
| --- | --- |
| Package size / type |     |
| Automotive | No  |
| Temperature rating | 0 to +40 °C |
| Budgetary / BOM |     |
| Stock / Production Qty | Minimum stock availability for production? |
| Other |     |

## Selected Options

Please spec here the options you selected (in case there are several).

### Option 1

| Parameter | Value |
| --- | --- |
| Manufacturer and Part No | STM32C011F6 |
| Manufacturer link | [STM32C011F6 \| Product - STMicroelectronics](https://www.st.com/en/microcontrollers-microprocessors/stm32c011f6.html#overview) |
| Digikey / Mouser / etc link | [STM32C011F6P6 STMicroelectronics \| Microcontrollers \| DigiKey](https://www.digikey.com/en/products/detail/stmicroelectronics/STM32C011F6P6/17071366) |
| Dev board information | [STM32C0116-DK \| Product - STMicroelectronics](https://www.st.com/en/evaluation-tools/stm32c0116-dk.html#sample-buy)  [STM32C0116-DK STMicroelectronics \| Embedded MCU, DSP Evaluation Boards \| DigiKey](https://www.digikey.com/en/products/detail/stmicroelectronics/STM32C0116-DK/17074591?s=N4IgjCBcoLQBxVAYygMwIYBsDOBTANCAPZQDaIALAJwDsIAugL6OEBMZIAygCoCyAzKwDCABjBgAbDAAiAaQaMgA) |
| Programmer | [ST-LINK/V2 STMicroelectronics](https://www.digikey.com/en/products/detail/stmicroelectronics/ST-LINK-V2/2214535)  [ARM20-CTX 20-Pin to TC2030-IDC](https://www.tag-connect.com/product/arm20-ctx-20-pin-to-tc2030-idc-adapter-for-cortex)  [6-pin small PCB footprint to IDC MCU debug cable](https://www.tag-connect.com/product/tc2030-idc-6-pin-tag-connect-plug-of-nails-spring-pin-cable-with-legs) |
| Pros for this option |     |
| Cons for this option |     |