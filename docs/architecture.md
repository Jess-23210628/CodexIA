# Firmware Architecture

## Source Layout
- `src/main.cpp`: single-module firmware using Arduino runtime.

## Runtime Flow
1. `setup()`
   - Iterates all 12 LED pins.
   - Configures each as OUTPUT.
   - Initializes all LEDs OFF (`LOW`).
2. `loop()`
   - Reads one key from keypad scanner (`keypad.getKey()`).
   - If a valid key is received, executes a `switch` dispatch:
     - Direct mappings for `1..8`, `A..D`
     - Group operations for `9`, `0`, `*`, `#`
   - Delays 10ms before next scan.

## Module Responsibilities
- `Keypad` object:
  - Maintains key matrix mapping and row/column scanning.
- `ledPins[]`:
  - Hardware abstraction array for deterministic GPIO writes.
- `switch(key)`:
  - Behavior table that defines exact feature semantics.

## Behavioral Guarantees (Preserved)
- No key release events are handled.
- LEDs are latched (state persists until another key changes it).
- Blue group and red group are independently controlled by dedicated keys.
- Timing behavior remains polling-based with fixed 10ms delay.

## Portability Note
This source is Arduino-style C++ and not raw Pico SDK C API. For pure Pico SDK, logic can be ported without changing behavior by replacing GPIO and keypad abstractions.
