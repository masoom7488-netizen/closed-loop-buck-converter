# Closed-Loop Buck Converter with Analog PI Controller

## Project Overview

This project implements a **closed-loop DC-DC buck converter** controlled using an **analog PI (Proportional-Integral) controller**.

The objective was to design and experimentally test a buck converter for regulating the output voltage using feedback control. The power stage and control circuit were assembled and tested on a breadboard-based hardware prototype.

## Design Specifications

| Parameter                      | Design Value |
| ------------------------------ | -----------: |
| Input Voltage                  |         24 V |
| Target Output Voltage          |         12 V |
| Rated Output Power             |         24 W |
| Switching Frequency            |       20 kHz |
| Inductor Current Ripple        |          20% |
| Output Voltage Ripple          |          10% |
| Calculated Duty Ratio          |          50% |
| Calculated Load Resistance     |          6 Ω |
| Calculated Inductance          |       750 µH |
| Calculated Minimum Capacitance |      2.08 µF |

## Control Strategy

The converter uses a **closed-loop voltage control scheme**.

The scaled output voltage is compared with the reference voltage. The resulting error is processed by an **analog PI controller**. The controller output is compared with a triangular carrier waveform to generate the PWM signal, which is then applied to the switching device through a gate-driver stage.

### Control Flow

**Reference Voltage → Error Amplifier → PI Controller → PWM Generation → Gate Driver → Buck Converter → Output Feedback**

## Circuit

The circuit diagram provided for the project is available in the [`circuit`](./circuit/) folder.

## Hardware Implementation

The power stage and control circuitry were assembled and tested on a breadboard using discrete power and control components.

The hardware prototype includes the switching device, freewheeling diode, inductor, output capacitor, feedback network and analog control circuitry.

Hardware photographs are available in the [`hardware`](./hardware/) folder.

## Design Calculations

The main design calculations, including duty ratio, load resistance, inductor current ripple, inductance and output capacitance, are documented here:

[Design Calculations](./calculations/design-calculations.md)

## Experimental Testing

The prototype was experimentally tested using a digital multimeter and laboratory hardware setup.

The measurement photographs are available in the [`results`](./results/) folder.

The recorded readings in the photographs are presented as **observed test measurements** and are not assumed to represent the final regulated 12 V output without confirming the exact measurement node.

## Key Components / Concepts

* Buck converter topology
* Analog PI controller
* PWM generation
* Voltage feedback
* Gate-driver circuit
* Inductor and capacitor selection
* Closed-loop voltage regulation
* Power electronics hardware implementation

## Skills Demonstrated

* Power Electronics
* DC-DC Converter Design
* Analog Control
* Feedback Control
* PWM Generation
* Circuit Prototyping
* Experimental Testing
* Electrical Measurements

## Project Status

**Hardware prototype implemented and experimentally tested.**

Further work can include PCB implementation, improved feedback scaling, controller tuning and detailed waveform analysis using an oscilloscope.

