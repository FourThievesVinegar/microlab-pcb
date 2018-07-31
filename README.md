# FTVC Microlab PCB

![Four Thieves Vinegar Micro Lab](https://github.com/FourThievesVinegar/microlab/blob/master/images/4tvc.jpg)


This is the printed circuit board hardware component for controlling the Four Thieves Vinegar Collective's Apothecary Microlab. It was built with Altium Designer v15 and sits mezzanine to the Raspberry Pi Zero.

## Building

To build your own Microlab PCB follow these guides:

[Ordering the PCB](docs/order-pcb.md)

[Ordering the PCB Components](docs/order-pcb-components.md)

## Interfaces

The PCB provides the following interfaces:

* 2 x 12 V Stepper motors
* 4 x Buttons for stepper motor control
* 4 x Limit switches
* 1 x DC motor controller (PWM)
* 3 x Relays
* N x DS18B20 temperature probes
* 2 x Raspberry Pi GPIO

## Electrical

### Power

The PCB is powered by a 12 VDC power brick. It will supply power to the Raspberry Pi Zero, stepper motors, stirrer motor, and temperature probes.

The power connector is a standard 2.10mm ID, 5.50mm OD centre-positive barrel jack connector (PJ-037AH).

Power consumption has yet to be measured.

### Stepper Motors

Drives two bipolar (four-wire) stepper motors with 12 V at 1.2 A max.

Stepper motor driver IC: TB6612FNG.

### Buttons and Limit Switches

Active-high. Includes pull-down resistors and debounce RC filters.

### DC Motor Controller

Supplies 12 VDC at 2 A max. Connected to a PWM pin on the Pi.

### Relays

Rated for 250VAC, 125VDC at 10 A max.

**WARNING:** If you are switching main's powered devices, be careful not to touch the exposed leads on the bottom of the PCB.

### Temperature Probes

Supports any number of DS18B20 temperature probes. Connected to the 1-wire pin on the Pi and includes the data-line pull-up resistor.

### Pi GPIO Pins

Two Pi GPIO pins, BCM0 (pin 27) and BCM1 (pin 28) are exposed along with 5, 12, 3.3 V and GND on a six pin header.

## Mechanical

The PCB is 100 mm x 50 mm with rounded corners.

The three M2.5 mounting holes are concentric with the Pi's. They are drilled to 2.75 mm diameter and provide 6 mm diameter clearance. The centre-to-centre horizontal and vertical distance is 58 mm and 23 mm. The holes' centres are 3.5 mm from their board edge.
