# Breadboard Power Supply

This project is a simple breadboard power supply PCB made in KiCad. It is designed to take a DC input supply and provide useful output rails for breadboard experiments.

The board includes a barrel jack input, an on/off slide switch, voltage regulators, output headers, screw terminals, and a power indicator LED. The schematic uses a 12 V input label, a fixed 5 V regulator, and an LM317 regulator set up for a 3.3 V output.


## What This Board Does

- Accepts power through a DC barrel jack.
- Uses a slide switch to turn the board on and off.
- Provides a regulated 5 V output using an LM7805 regulator.
- Provides a regulated 3.3 V output using an LM317 regulator.
- Breaks out power through pin headers and screw terminals.
- Shows power status with an LED indicator.

This kind of board is useful when testing small circuits on a breadboard. It lets you power logic circuits, sensors, microcontrollers, and other low-voltage modules from one compact PCB.

## Project Files

| File | Purpose |
| --- | --- |
| `Breadboard Power Supply.kicad_pro` | Main KiCad project file. Open this file in KiCad. |
| `Breadboard Power Supply.kicad_sch` | Schematic file. This shows the electrical circuit. |
| `Breadboard Power Supply.kicad_pcb` | PCB layout file. This shows the board routing and component placement. |
| `Breadboard Power Supply.kicad_prl` | KiCad local project settings file. |
| `0398800302.stp` | 3D model used by the PCB. |
| `500SSP1S1M2REA--3DModel-STEP-418109.STEP` | 3D model used by the PCB. |
| `img/` | Photos shown in this README. |
| `Breadboard Power Supply-backups/` | KiCad backup files. |

## Main Components

The schematic includes these main parts:

- `J1`: DC barrel jack input.
- `S1`: EG1218 slide switch.
- `U2`: LM7805 regulator for the 5 V rail.
- `U1`: LM317 regulator for the 3.3 V rail.
- `D1`: Power indicator LED.
- `R1`, `R2`, `R3`: Resistors for LED current limiting and regulator setting.
- `C1`, `C2`, `C3`: Capacitors for regulator stability and filtering.
- `J2`, `J5`: Screw terminal outputs.
- `J3`, `J4`, `J6`, `J7`: Pin header outputs.

## Power Notes

The input net is labelled as `12V` in the schematic. Use a DC supply that is suitable for the regulators and the parts installed on the board.

The LM7805 regulator creates the 5 V output. The LM317 regulator creates the 3.3 V output using the resistor values shown in the schematic.

Linear regulators can become hot when the input voltage is much higher than the output voltage or when the load current is high. Check the regulator temperature during testing. Add heatsinks if needed.

## How to Open the Project

1. Install KiCad.
2. Open KiCad.
3. Choose **File > Open Project**.
4. Select `Breadboard Power Supply.kicad_pro`.
5. Open the schematic or PCB layout from the KiCad project window.

## Before Making the PCB

Before sending the board for manufacturing, check the design carefully:

1. Run the Electrical Rules Checker in the schematic editor.
2. Run the Design Rules Checker in the PCB editor.
3. Confirm the footprints match the real parts you will use.
4. Check the pinout of the barrel jack, regulators, switch, headers, and screw terminals.
5. Inspect the 3D view to make sure the parts fit correctly.
6. Generate Gerber files only after the checks pass.

## Suggested Assembly Order

1. Solder the resistors first.
2. Solder the capacitors.
3. Solder the LED.
4. Solder the pin headers and screw terminals.
5. Solder the barrel jack and slide switch.
6. Solder the voltage regulators last.
7. Inspect all solder joints before applying power.

## First Power Test

Use a current-limited power supply for the first test if possible.

1. Keep the board disconnected from any breadboard circuit.
2. Apply the input voltage.
3. Turn the slide switch on.
4. Check that the power LED turns on.
5. Measure the 5 V output with a multimeter.
6. Measure the 3.3 V output with a multimeter.
7. Turn the board off and check that the outputs turn off.

Do not connect sensitive parts until the output voltages are confirmed.

## Safety

This board is intended for low-voltage electronics experiments. Do not connect it directly to mains voltage. Always check polarity before applying power.

## Author

Designed by Jit Dey.

## Project Images

These photos show the breadboard power supply project.

![Breadboard power supply photo 1](img/1759331978309.jfif)

![Breadboard power supply photo 2](img/1759332013281.jfif)

![Breadboard power supply photo 3](img/1759332022775.jfif)

![Breadboard power supply photo 4](img/1759332033750.jfif)

![Breadboard power supply photo 5](img/1759332048909.jfif)
