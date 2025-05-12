# 🔧 Logic Probe PCB v1.0

A custom-designed logic probe circuit built using EasyEDA, capable of detecting **LOW**, **HIGH**, and **PWM** (pulsed) digital signals. This project demonstrates analog signal processing techniques, comparator configurations, and practical PCB design skills.

---

## 💡 Project Overview

The circuit uses three comparators to detect signal states:

- **U1** – Compares the input to a low voltage reference (`REF_LOW`) to detect **LOW** logic levels.
- **U2** – Compares the input to a mid-level reference (`REF_MID`) to detect **PWM** signals using a filtered voltage.
- **U3** – Compares the input to a high voltage reference (`REF_HIGH`) to detect **HIGH** logic levels.

Each comparator drives an LED (red, blue, green) to indicate the signal type visually.

---

## 🧩 Circuit Description

| Component | Purpose |
|-----------|---------|
| **R1–R4** | Voltage dividers to set `REF_LOW` and `REF_HIGH` |
| **R6–R7** | Voltage divider to create `REF_MID` |
| **R5 + C1** | RC low-pass filter for smoothing PWM signals |
| **U1, U2, U3** | Comparators for LOW, PWM, and HIGH logic levels |
| **LED1–LED3** | Status LEDs for LOW (red), PWM (blue), and HIGH (green) |

---

## 🌀 RC Filter: Why It Matters

The RC filter (R5 and C1) is used to average the PWM input signal into a steady analog voltage. This allows comparator **U2** to detect a PWM waveform based on its duty cycle. Without this filter, the comparator would toggle rapidly and not accurately identify PWM behavior.

---

## 📦 Project Files

- `Gerber_Logic-Probe-Tool_PCB_Logic-Probe-Tool_2025-05-12/` – Gerber files for fabrication
- `Schematic_Logic-Probe-Tool_2025-05-12.pdf` – Circuit schematic
- `PCB_PCB_Logic-Probe-Tool_2025-05-12.pdf` – Board layout
- `PCB_PCB_Logic-Probe-Tool_2025-05-12.json` – EasyEDA source file
- `3D View.png` – Rendered 3D image of the assembled PCB

---

## 🖼️ 3D Preview

![3D View](3D%20view.png)


---

## 👨‍💻 Author

Designed by **Asaf Alber**, a Control & Hardware Engineering student with a focus on analog and embedded system design.

This logic probe project is part of my hardware design portfolio.
