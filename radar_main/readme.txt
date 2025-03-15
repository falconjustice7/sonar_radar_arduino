# Servo-Based Ultrasonic Scanner

This Arduino project uses a **servo motor** and an **HC-SR04 ultrasonic sensor** to scan an area and measure distances. The sensor rotates back and forth, capturing distance values and outputting them over Serial.

## Hardware Requirements
- **Arduino Uno/Nano/Mega**
- **HC-SR04 Ultrasonic Sensor**
- **SG90 Servo Motor**
- Jumper Wires

## Wiring Instructions
| Component   | Arduino Pin |
|-------------|------------|
| Servo (Signal) | 9 |
| HC-SR04 Trigger | 11 |
| HC-SR04 Echo | 12 |
| VCC (Both) | 5V |
| GND (Both) | GND |

## Installation and Usage
1. Connect the components as per the wiring table above.
2. Open **Arduino IDE** and upload the `servo_ultrasonic.ino` file.
3. Open **Serial Monitor** (9600 baud) to view the angle and distance readings.

## Expected Output
The serial monitor will display readings like:
90, 50 91, 48 92, 49 ...

where **90** is the servo angle and **50** is the measured distance (cm).

## Notes
- Modify `minimumAngle` and `maximumAngle` in the code to change the scanning range.
- If readings seem inaccurate, check wiring and power supply.

