# 🔧 Logic Probe PCB v1.0

A custom logic probe circuit board designed using EasyEDA to diagnose digital signals and logic states.

## 💡 Project Overview
This project implements:
- **Three-state logic indication**: LOW, HIGH, and PWM (logic toggling)
- **Comparators (U1, U4)** with reference voltages
- **RC Low-pass filter** to detect PWM signals
- **LED indicators** with pull-up resistors
- **USB power input**

## 🧩 Circuit Details
| Component | Description |
|-----------|-------------|
| R1–R4     | Voltage dividers for `REF_LOW` and `REF_HIGH` |
| R5 + C1   | RC filter for smoothing PWM signal |
| R6–R7     | Midpoint voltage reference |
| U1, U4    | Comparators to evaluate logic level |
| U2        | USB power input |
| LED1-3    | LOW, HIGH, PWM state indicators |

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

