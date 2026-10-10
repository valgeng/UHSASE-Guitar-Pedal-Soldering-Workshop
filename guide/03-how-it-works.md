# 03 — How the digital delay pedal works

[← Workshop home](../README.md) · [← Controls](02-pedal-controls.md) · [Next: Soldering →](04-soldering-guide.md)

## Signal flow

`Guitar → Input jack → Audio/input circuitry → Teensy digital processing → Audio/output circuitry → Output jack → Amplifier`

1. **Guitar / input jack:** Guitar strings create an electrical audio signal that enters the pedal.
2. **PCB (printed circuit board):** Holds the components and connects them through copper traces, pads, and plated holes. It is the physical wiring platform, **not the device that calculates the echo**.
3. **Audio circuitry / adaptor:** Interfaces with the guitar signal and digital processing; appropriate audio conversion is needed for digital delay processing.
4. **Microcontroller:** Runs a program that temporarily stores audio samples and plays them back after a set delay. Feedback can feed a portion of the delayed audio back into the effect.
5. **Knobs:** Potentiometers allow the player to adjust time, feedback, and volume settings.
6. **Output jack / amplifier:** Sends the processed audio to the amplifier, where it becomes audible.

## Kicad Schematic vs. PCB layout

- [**Schematic**](../hardware/kicad/delay_pedal_teensy.kicad_sch): Which parts connect electrically.
- [**PCB layout**](../hardware/kicad/delay_pedal_teensy.kicad_pcb): Where those parts and copper connections are placed physically.
- [**Gerbers**](../hardware/manufacturing/gerbers_delay_pedal_teensy.zip): Files a manufacturer uses to fabricate the board.
