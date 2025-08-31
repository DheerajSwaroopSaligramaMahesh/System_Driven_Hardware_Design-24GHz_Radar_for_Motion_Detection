# 24GHz Motion Detection Radar

This project implements a **24 GHz radar sensor for movement detection** using **FreeSoC2 (Cypress PSoC)**, with signal processing performed through **FFT** and **CA-CFAR algorithms**.  
It integrates **hardware PCB design**, **embedded C firmware**, and **MATLAB scripts** for real-time analysis and visualization.

---

## Features
- **24 GHz Radar Frontend** – Captures reflected RF signals.
- **Analog Signal Conditioning** – Amplification + Bandpass filtering.
- **ADC Sampling** – FreeSoC2 samples the baseband signal.
- **FFT Processing** – Frequency-domain analysis on embedded side.
- **CA-CFAR Detection** – Adaptive thresholding for reliable movement detection.
- **UART Communication** – Transfers ADC/FFT/CFAR data to PC.
- **MATLAB Visualization** – Plots time-domain, FFT spectrum, and CFAR detections.
- **LED Indicators** – Show system states and detection results.

---

## Project Structure
- **C Code** → Firmware for FreeSoC2 (sampling, FFT, CFAR, UART, LEDs). [Fressoc C Code](https://github.com/DheerajSwaroopSaligramaMahesh/System_Driven_Hardware_Design-24GHz_Radar_for_Motion_Detection/tree/main/24GHz_Radar/Final_Design.cydsn/Final_Design.cydsn)
- **MATLAB Scripts** → Data acquisition & visualization of FFT + CFAR.

  [MATLAB Test Scripts](https://github.com/DheerajSwaroopSaligramaMahesh/System_Driven_Hardware_Design-24GHz_Radar_for_Motion_Detection/tree/main/24GHz_Radar/MATLAB_test_input)

  [MATLAB CFAR Script](https://github.com/DheerajSwaroopSaligramaMahesh/System_Driven_Hardware_Design-24GHz_Radar_for_Motion_Detection/blob/main/24GHz_Radar/MatlabPlots.mlx)
- **PCB Design (KiCad)** → 4-layer PCB (THT) with isolated analog/digital grounds. [KiCad PCB Design Project](https://github.com/DheerajSwaroopSaligramaMahesh/System_Driven_Hardware_Design-24GHz_Radar_for_Motion_Detection/tree/main/24GHz_Radar/PCB_Design_KiCad/Bandpass_Filter)
- **Presentation** → System explanation, testing, and results. [Presentation](https://github.com/DheerajSwaroopSaligramaMahesh/System_Driven_Hardware_Design-24GHz_Radar_for_Motion_Detection/blob/main/Final_Presentation.pdf)

---

## Workflow
1. **Signal Acquisition**  
   Radar captures reflected RF → Amplified & filtered → Converted to digital by ADC.  

2. **Embedded Processing**  
   FreeSoC2 performs FFT + CA-CFAR → Detects moving objects → LED indication.  

3. **Data Transfer & Visualization**  
   Processed data sent over UART → MATLAB plots spectrum, thresholds, and detections.  

---

## Outputs
- Hardware testing results of voltage divider, amplifiers, and ADC.  
- MATLAB plots for **sine + noise inputs, FFT magnitude, CFAR thresholds, and detected targets**.  
- Real radar detection experiments using 24 GHz module.  

---

## Files in Repo
- `C_Code/` → Embedded firmware (sampling, FFT, CFAR, UART).  
- `MATLAB/` → Scripts for simulation & visualization.  
- `Final_Presentation.pdf` → Slides showing design & testing.  

---

## Requirements
- **Hardware**: FreeSoC2 board, 24 GHz radar module, custom PCB.  
- **Software**:  
  - PSoC Creator 4.4  
  - MATLAB R2022b (or later)  

---

## How to Run
### On FreeSoC2
1. Open project in **PSoC Creator**.  
2. Build & program FreeSoC2.  
3. Press the **button** to start data acquisition.  
4. LEDs indicate **system state** (IDLE, SAMPLING, UART transfer, detection).  

### On PC (MATLAB)
1. Connect to FreeSoC2 via **UART (COM port)**.  
2. Run `MatlabPlots.mlx` in MATLAB.  
3. View **time signals, FFT spectrum, CFAR thresholds, and detections** in real-time.  

---

## References
- Project Presentation: [Final_Presentation.pdf](https://github.com/DheerajSwaroopSaligramaMahesh/System_Driven_Hardware_Design-24GHz_Radar_for_Motion_Detection/blob/main/Final_Presentation.pdf)  

---

## Project Demonstration Videos
1. [RADAR Testing Video](https://youtu.be/QEi5VdX2Rts)
2. [Final Working with CFAR](https://youtu.be/P_1PikC-du8?si=aujpoiVXmP4m2WWZ)

---

For more details, refer to the **presentation, and MATLAB/C code** in this repository.
