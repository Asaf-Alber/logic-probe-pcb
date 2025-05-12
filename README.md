# 🔧 Logic Probe PCB v1.0

A custom-designed logic probe circuit built using EasyEDA, capable of detecting LOW, HIGH, and PWM (pulsed) digital signals. This project showcases analog signal processing techniques, comparator configurations, and PCB design proficiency.

## 💡 Project Overview
This logic probe utilizes three comparators to evaluate input signals against defined voltage references:
U1: Compares the input signal to a low reference voltage (e.g., 1.0V) to detect a LOW logic level.
U2: Compares the input signal to a mid-level reference voltage (e.g., 2.5V) to detect a PWM or pulsing signal.
U3: Compares the input signal to a high reference voltage (e.g., 4.0V) to detect a HIGH logic level.
Each comparator controls an LED indicator, providing a visual representation of the signal state.


🧩 Circuit Details
Component	Function
R1–R4	Voltage dividers to establish REF_LOW and REF_HIGH reference voltages
R5 + C1	RC low-pass filter to smooth out PWM signals
R6–R7	Voltage divider to create the mid-level reference voltage (REF_MID)
U1, U2, U3	Comparators for detecting LOW, PWM, and HIGH logic levels respectively
LED1–LED3	Visual indicators for LOW (red), PWM (yellow), and HIGH (green) signals

🌀 RC Low-Pass Filter Functionality
The RC filter, composed of resistor R5 and capacitor C1, serves to smooth out high-frequency components of the input signal. This is particularly useful for detecting PWM signals, where the filter averages the rapid on-off transitions into a steady voltage level. This averaged voltage can then be compared against the mid-level reference (REF_MID) by comparator U2 to determine the presence of a PWM signal.
## 🖼️ 3D Preview

![3D View](3D%20view.png)

## 📂 Included Files
- ✅ Gerber files (for fabrication)
- ✅ Schematic PDF
- ✅ PCB layout PDF
- ✅ EasyEDA JSON file
- ✅ 3D rendered image

## 👨‍💻 Author
Designed by **Asaf Alber** — aspiring Hardware Engineer.

