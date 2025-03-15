# Ultrasonic Radar System  

## Overview  
This project consists of two main folders:  
- **radar_main** → Contains the Arduino code for scanning using an ultrasonic sensor and servo motor.  
- **radar_display** → Contains the Processing code for visualizing the radar data on a computer screen.  

The system scans the environment using an **HC-SR04 ultrasonic sensor** mounted on a **servo motor** and sends real-time distance data to Processing for display.  

## Requirements  
- **Arduino Uno (or compatible board)**  
- **HC-SR04 Ultrasonic Sensor**  
- **SG90 Servo Motor**  
- **Processing IDE** ([Download](https://processing.org/download))  
- **Processing Serial Library** (Install via **Sketch → Import Library → Add Library → "serial"**)  

## Download & Setup  
### **1. Clone or Download the Repository**  
Download the repository from GitHub:  
git clone https://github.com/falconjustice7/sonar_radar_arduino.git

Or manually download the ZIP and extract it.  

### **2. Upload Arduino Code**  
1. Open the **Arduino IDE**.  
2. Open the `radar_main` folder.  
3. Upload the `.ino` file to your **Arduino Uno**.  
4. Close the **Serial Monitor** before running Processing.  

### **3. Run Processing Code**  
1. Open the **Processing IDE**.  
2. Open the `radar_display` folder.  
3. **Ensure the three "OCRAExtended.vlw" font files are inside the `radar_display` folder.**  
4. Run the `radar_display.pde` file.  
5. The radar visualization should appear.  

## Wiring Instructions  
| Component | Arduino Pin |  
|------------|------------|  
| Servo (Signal) | 9 |  
| HC-SR04 Trigger | 11 |  
| HC-SR04 Echo | 12 |  
| VCC (Both) | 5V |  
| GND (Both) | GND |  

## Expected Output  
- **Green radar sweep** shows scanning progress.  
- **Red lines** indicate detected objects.  
- **Live angle & distance** displayed on-screen.  

## Notes  
- The **Arduino sends data in `<angle>,<distance>\n` format**.  
- **Close Arduino Serial Monitor** before running Processing.  
- The radar display is **limited to 40cm detection range** (can be modified).  

## Troubleshooting  
- **No output?**  
  - Ensure the correct **COM port** is set in `radar_display.pde`.  
  - Verify the **Arduino is sending data properly**.  
  - **Close Arduino Serial Monitor** (it can block Processing).  
- **Fonts not loading?**  
  - Make sure **OCRAExtended.vlw** files are inside `radar_display`.  

---

### **Developed by:**  
- **Manish Googa (falconjustice7)**  
- **Chiranjeevi Bogaraju**  
