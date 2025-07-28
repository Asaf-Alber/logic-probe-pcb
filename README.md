#  Logic Probe PCB v1.0

This logic probe tool was designed to identify signal states (LOW, HIGH, or PWM activity) on a digital line. It leverages voltage reference dividers, comparators, and an RC filter to reliably distinguish between static and pulsed inputs.

---

##  Functional Overview

- **Signal Input** is compared to three voltage levels:
  - **REF_LOW (≈1.5V)**: If the signal is below this, it's considered LOW.
  - **REF_HIGH (≈3.5V)**: If the signal is above this, it's considered HIGH.
  - **Between REF_LOW and REF_HIGH**: Signal is indeterminate — possibly PWM or noise.

###  Comparators Used

| Comparator | Function                          | Output LED     |
|------------|-----------------------------------|----------------|
| `U1`       | Signal < REF_LOW                  | `LED1` (🔴 Red for LOW) |
| `U2`       | Signal > REF_HIGH                 | `LED2` (🟢 Green for HIGH) |

---

##  Reference Voltage Dividers

| Voltage     | Divider Components   |
|-------------|----------------------|
| `REF_LOW`   | `R1` and `R2`        |
| `REF_HIGH`  | `R3` and `R4`        |

Each divider scales `VCC` into usable thresholds for the comparators.

---

##  Annotated Schematic

The following schematic maps the logic described above to the physical design.

![Annotated Schematic](schematiclogicprobe.png)

---

##  Waveform Simulation

Below is a simulated signal passing through LOW, PWM, and HIGH regions. The dashed lines represent the logic thresholds.

![Waveform](waveform.png)

---

##  3D Preview

View of the final PCB board with all labeled components.

![3D View](3D%20view.png)

---

##  How to Use

1. Connect 5V and GND to the probe input header.
2. Attach the input signal to the `SIGNAL_IN` pin.
3. Observe the LED indicators:
   - 🔴 Red = LOW
   - 🟢 Green = HIGH
---
##  Summary


This project demonstrates my ability to:
- Design with analog comparators
- Use voltage dividers for reference generation
- Design and route PCBs in EasyEDA
- Document functional logic clearly

---

## 📦 Contents

- `Gerber_Logic-Probe-Tool...` – Fabrication files
- `PCB_PCB_Logic-Probe-Tool...` – PCB layout project
- `Schematic_Logic-Probe-Tool...` – Source schematic
- `3D view.png` – Rendered 3D model
- `README.md` – Project documentation (you’re reading it!)

---

## 🧠 Author

**Asaf Alber**  
Logic Probe PCB Designer – May 2025  
GitHub: [Asaf-Alber](https://github.com/Asaf-Alber)
