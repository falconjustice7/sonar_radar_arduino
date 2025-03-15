# Ultrasonic Radar Visualization using Processing  

## Overview  
This project visualizes distance measurements from an **Arduino-based ultrasonic sensor** using **Processing**. The radar sweep detects objects and displays them on-screen in real time.  

## Requirements  
- **Arduino Uno** (or compatible board)  
- **HC-SR04 Ultrasonic Sensor**  
- **SG90 Servo Motor**  
- **Processing IDE** (Download from [processing.org](https://processing.org/download))  
- **Processing Serial Library** (Install via **Sketch → Import Library → Add Library → "serial"**)  

## Installation & Setup  
1. **Download the `radar_display` folder** and extract it.  
2. **Connect the Arduino to your PC** and upload the ultrasonic radar scanning code.  
3. **Ensure Arduino is on the correct COM port** (Update `myPort = new Serial(this, "COM5", 9600);` if needed).  
4. **Open `radar_display.pde` in Processing IDE**.  
5. **Make sure the three "OCRAExtended.vlw" font files are inside the `radar_display` folder**.  
6. **Run the Processing sketch** while the Arduino is connected.  

## Wiring Instructions  
| Component   | Arduino Pin |  
|------------|------------|  
| Servo (Signal) | 9 |  
| HC-SR04 Trigger | 11 |  
| HC-SR04 Echo | 12 |  
| VCC (Both) | 5V |  
| GND (Both) | GND |  

## Expected Output  
- **A radar sweep appears on the screen.**  
- **Detected objects appear as red lines.**  
- **Live angle & distance values are displayed.**  

## Notes  
- The Processing code reads **angle and distance** from the **Arduino serial output**.  
- The **detection range is limited to 40cm** in the visualization.  
- **Ensure the Arduino Serial Monitor is CLOSED** before running Processing.  

## Troubleshooting  
- **No output?**  
  - Check the **COM port** in `myPort = new Serial(this, "COM5", 9600);`.  
  - Ensure Arduino is **sending data in `<angle>,<distance>\n` format**.  
  - **Close Arduino Serial Monitor** (it can block Processing from accessing the port).  
- **Fonts missing?**  
  - Ensure **OCRAExtended.vlw** files are inside the `radar_display` folder.  


