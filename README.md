# LED Heart (555 + 4017 Chaser)

A custom heart-shaped PCB featuring 10 LEDs running in a continuous loop, built entirely with classic discrete logic ICs (NE555 and CD4017) — no microcontroller or code required!

## Why does it exist?
- Christmas Gift: Created as a handmade electronic gift for Christmas.
- Back to Basics: Instead of reaching for an Arduino, ESP32, or any microcontroller for every small project, I wanted to build something purely in hardware using classic timer and counter ICs.

## Features
- No Code Needed: Pure hardware logic.
- Custom Heart-Shaped PCB: Designed in KiCad.
- Adjustable Speed: Smoothly control the LED loop speed via an onboard potentiometer.
- 5V Powered

## How It Works
1. Clock Generation (U2 - NE555P): Configured in astable mode to generate a continuous clock signal. Turning the 50k potentiometer adjusts the charge rate of C1, changing the blink frequency.
2. Decade Counter: Advances its active output (Q0–Q9) on every rising clock edge from the 555 timer, lighting up D1 through D10 sequentially in an endless loop (as long if it had eletrical energy).
3. Current Limiting: Since only one LED is active at any given time, a single 470Ω shared cathode resistor safely limits the current for all 10 LEDs.

## Bill of Materials (BOM)

| Reference | Component | Value / Notes |
| :--- | :--- | :--- |
| U1 | Decade Counter IC | CD4017 (DIP-16) |
| U2 | Timer IC | NE555P (DIP-8) |
| D1 – D10 | LEDs | 3mm or 5mm (any color) |
| R1 | Resistor | 470 (Current limiting) |
| R2 | Resistor | 1 k |
| RV1 | Potentiometer | 50 k (Loop speed control) |
| C1 | Capacitor | 1 µF |
| C2 | Capacitor | 0.01 uF (10 nF) |
| J1, J2 | Power Pads | 5V & GND |
| PCB | Custom Board | Heartshaped PCB (KiCad) |

## Tools

- KiCad – Schematic capture and PCB layout.

## Schematic

<img width="627" height="469" alt="image" src="https://github.com/user-attachments/assets/233dbf60-0fe7-4602-9b86-d2acd63831ae" />

## PCB

<img width="735" height="605" alt="image" src="https://github.com/user-attachments/assets/06d10fa1-c1a7-4954-83e6-2b7be099226d" />

<img width="750" height="627" alt="image" src="https://github.com/user-attachments/assets/72510d76-e294-4474-a7b8-668180a8bf2d" />

## Extras & Credits

- Artwork Credit: Pixel art on the personal build inspired by OMOCAT (not included in the repo files).

## Bonus

There was a time I had no idea what I was doing.

<img width="668" height="606" alt="Screenshot 2026-10-11 161922" src="https://github.com/user-attachments/assets/a1ec8ca0-2564-4813-9743-c6d37ee7b127" />

Something I added to the PCB as an example of what you can put on.

<img width="729" height="591" alt="image" src="https://github.com/user-attachments/assets/7aef20c5-43fb-49fb-9bec-35059ac181d2" />
