# Raspberry Pi Pico W Keypad-to-LED Controller

## Overview
This project runs on a Raspberry Pi Pico W (RP2040) and maps a 4x4 membrane keypad to 12 LEDs.
Each key press toggles specific LED outputs exactly as implemented in the original source logic.

- Numeric keys `1..8`: turn on one of the first 8 blue LEDs
- `9`: turn on all first 8 blue LEDs
- `0`: turn off all first 8 blue LEDs
- `A..D`: turn on one of the 4 red LEDs
- `*`: turn on all red LEDs (`A..D` group)
- `#`: turn off all red LEDs (`A..D` group)

## Repository Structure
- `src/main.cpp` - Main firmware logic (preserved behavior)
- `include/` - Reserved for headers if project expands
- `docs/wiring.md` - Hardware components and GPIO wiring details
- `docs/architecture.md` - Firmware architecture and behavior mapping
- `CMakeLists.txt` - Minimal top-level build metadata for C/C++ layout

## Features
- 4x4 keypad scanning via `Keypad` library
- 12 independent LED outputs
- Group control keys for blue and red LED banks
- 10ms loop delay for stable polling

## Hardware Requirements
- Raspberry Pi Pico W
- 4x4 membrane keypad
- 12 LEDs (8 blue + 4 red in the Wokwi model)
- 12x 220Ω LED series resistors
- 4x 1kΩ pull-up resistors for keypad rows (as in provided diagram)
- Jumper wires / breadboard

## Build and Flash

### Option A: Wokwi Simulation (Recommended for this source)
1. Create a new **Raspberry Pi Pico** project in Wokwi.
2. Paste `src/main.cpp` into the sketch source.
3. Add the provided `diagram.json` as the project diagram.
4. Ensure the `Keypad` library is available in the Wokwi environment.
5. Start simulation and press keypad buttons.

### Option B: Real Hardware using Arduino-Pico Core
This code is written with Arduino APIs (`setup()`, `loop()`, `digitalWrite()`, `Keypad.h`).

1. Install Arduino IDE 2.x.
2. Install **Raspberry Pi Pico/RP2040** board package (Earle Philhower core).
3. Install `Keypad` library from Library Manager.
4. Select board: **Raspberry Pi Pico W**.
5. Open `src/main.cpp` (or copy into an `.ino` sketch preserving content).
6. Put Pico W in BOOTSEL mode and upload.

## Pico W Notes
- This firmware does not currently use Wi-Fi.
- Keep Wi-Fi credentials out of source control if you add network features later.

## Behavior Preservation
The core application logic from the provided source is preserved verbatim in `src/main.cpp`.
Only repository organization and documentation were added.
