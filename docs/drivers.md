# RePlay Custom Drivers & DIY

RePlay provides out of the box support for the following custom drivers and devices:

* TAITO Paddle & Trackball
* NAMCO GunCon 2 Lightgun (for CRT TVs)
* GPIO Joystick (for arcade JAMMA boards)
* Retroflag 64Pi CASE
* Retroflag Dreamcase
* DIY Tilt Addon for RPi5

## DIY Tilt Add-on for RPi 5

**IMPORTANT**: Works only with Raspberry Pi 5.

To build the Tilt add-on, you need:

* 1× 2K resistor
* 1× tilt switch
* 3 wires for 3.3V, GND, and GPIO17
* A protoboard or PCB for assembly

### Circuit description

The connection is:

```
GND → Resistor → GPIO17 → Tilt Switch → 3.3V
```

### Raspberry Pi 5 physical pins

* Pin 1: 3.3V Power
* Pin 9: Ground
* Pin 11: GPIO17

### ASCII schematic

```
   Pin 1 (3.3V)
        │
   [ Tilt Switch ]
        │
      GPIO17 (Pin 11)
        │
     [ 2K Ω ]
        │
   Pin 9 (GND)
```

### How it works

* The 2K resistor acts as a pull-down, keeping GPIO17 at a stable LOW state when the tilt switch is open.
* When the tilt switch closes (due to movement), it connects GPIO17 directly to 3.3V.
* GPIO17 then reads as HIGH, providing a clear digital signal transition (LOW → HIGH) that software can detect.
* This avoids floating inputs and false triggers, ensuring stable readings.
* RePlay OS includes a new option to enable this feature: ADDONS > TILT INPUT PI5.
* When enabled, the system automatically rotates the UI and filters the game list to vertical titles.