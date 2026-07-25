# Bluetooth Controlled DC Motor

Controls DC motors wirelessly via Bluetooth using a PIC16F877A microcontroller, 
UART communication, and an L293D motor driver IC.

## Features
- Wireless motor control via Bluetooth (Android app/serial terminal)
- Bidirectional motor control (clockwise/counterclockwise)
- UART-based serial communication

## Hardware Used
- PIC16F877A microcontroller
- HC-05 Bluetooth module
- L293D Motor Driver IC
- DC Motors (x2)
- Crystal oscillator (with 22pF capacitors)
- 5V power supply

## Software/Tools
- MPLAB IDE / XC8 Compiler
- Embedded C
- Bluetooth terminal app (for testing)

## Circuit Diagram
![Circuit Diagram](images/bluetooth_circuit.png)

## How It Works
1. Commands are sent from a smartphone/PC via Bluetooth (HC-05).
2. PIC16F877A receives data through UART (RC6/TX, RC7/RX).
3. Based on the received command, the L293D driver controls motor direction and speed.

## Pin Connections
| Component      | PIC16F877A Pin |
|-----------------|----------------|
| HC-05 TX        | RC7/RX         |
| HC-05 RX        | RC6/TX         |
| L293D IN1-IN4   | RD0-RD3        |

(adjust to match your exact wiring)

## How to Run
1. Wire the circuit as per the diagram.
2. Pair HC-05 with your phone/PC via Bluetooth.
3. Send commands (e.g. F/B/L/R) via a Bluetooth serial terminal app.
4. Motors respond according to the command received.

## Demo
![Demo](images/demo.jpg)
