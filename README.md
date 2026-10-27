# STM32G071 touch display board (ILI9341)

<p>
  <img alt="MCU: STM32G071CBT6" src="https://img.shields.io/badge/MCU-STM32G071CBT6-blue">
  <img alt="Display: ILI9341" src="https://img.shields.io/badge/display-ILI9341-informational">
  <img alt="PCB: KiCad" src="https://img.shields.io/badge/PCB-KiCad-informational">
  <img alt="Status: v1.0, known footprint issue" src="https://img.shields.io/badge/status-v1.0%20(footprint%20issue)-orange">
  <a href="LICENSE"><img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-green"></a>
</p>

A custom STM32G071CBT6 board that carries an ILI9341 SPI TFT display on its back, with
demo firmware.

![STM32G071 board for the ILI9341 display, rendered in KiCad](docs/board-3d.png)

## What is on it

| Part | Purpose |
|---|---|
| STM32G071CBT6 | Cortex-M0+ MCU, 128 KB flash, 36 KB RAM |
| 16 MHz and 32.768 kHz crystals | Main clock and RTC |
| AMS1117-3.3 | 5 V → 3.3 V regulator |
| ILI9341 header (14-pin) | The display module, SPI |
| Tag-Connect TC2030 footprint (DEBUG) | SWD programming and debugging — see the [STDC14-to-TC2030 adapter](https://github.com/TechnikWeber/STDC14-to-TC2030-IDC) |
| 3-pin headers | UART (RX, TX, GND) and power (5 V, 3.3 V, GND) |
| RESET, BOOT0 and USER buttons, red LED | |

## Files

- `STM32G071.kicad_sch` / `.kicad_pcb` — schematic and PCB (KiCad)
- [`production/`](production) — Gerber/drill zip, BOM, positions and netlist
- [`Firmware/Display.7z`](Firmware) — STM32CubeIDE demo project for the display

## Known issue

> [!WARNING]
> **The ILI9341 footprint does not match** the display module that was bought
> ([AliExpress listing](https://de.aliexpress.com/item/32847628219.html)) — check the
> module's pin spacing and mounting holes before ordering boards.

<img src="https://github.com/user-attachments/assets/eac0f761-1974-4db9-a4fc-650ef7e3adc8" width="300" alt="Footprint mismatch">

## Pictures

<img width="635" alt="Board" src="https://github.com/user-attachments/assets/1e37552e-0095-4c62-91bf-244bf4a354f2" />

<img src="https://github.com/user-attachments/assets/f812a35f-fbf1-4fb1-ac30-f2a02b13746b" width="300" alt="Board"> <img src="https://github.com/user-attachments/assets/3334bf73-3c45-476b-af18-25e910a7d26a" width="300" alt="Board">

## License

[MIT](LICENSE).
