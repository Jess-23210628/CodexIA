# Wiring and GPIO Mapping (Raspberry Pi Pico W)

## Components Derived from `diagram.json`
- 1x Raspberry Pi Pico (target runtime: Pico W compatible pinout)
- 1x 4x4 membrane keypad
- 12x LEDs
  - 8 blue LEDs labeled `1..8`
  - 4 red LEDs labeled `A..D`
- 12x 220Ω resistors (LED current limiting)
- 4x 1kΩ resistors (keypad row pull-ups to 3.3V)

## GPIO Mapping from Firmware
### Keypad Lines
| Keypad Signal | Pico GPIO |
|---|---|
| C1 | GP19 |
| C2 | GP18 |
| C3 | GP17 |
| C4 | GP16 |
| R1 | GP26 |
| R2 | GP22 |
| R3 | GP21 |
| R4 | GP20 |

### LED Outputs
| LED Label | Firmware Index | Pico GPIO |
|---|---:|---|
| 1 | ledPins[0] | GP11 |
| 2 | ledPins[1] | GP10 |
| 3 | ledPins[2] | GP9 |
| 4 | ledPins[3] | GP8 |
| 5 | ledPins[4] | GP7 |
| 6 | ledPins[5] | GP6 |
| 7 | ledPins[6] | GP5 |
| 8 | ledPins[7] | GP4 |
| A | ledPins[8] | GP3 |
| B | ledPins[9] | GP2 |
| C | ledPins[10] | GP28 |
| D | ledPins[11] | GP27 |

## Electrical Notes
- LED cathodes are tied to GND in the provided diagram.
- LED anodes are driven from GPIO through 220Ω resistors.
- Keypad rows are additionally pulled up to 3.3V via 1kΩ resistors (`R1..R4` net in diagram names `rp1..rp4`).

## Assumptions
- The provided Wokwi diagram uses `wokwi-pi-pico`; pin mapping is valid for Pico W as both share RP2040 GPIO numbering.
- No level shifting is required since all devices are 3.3V domain.
