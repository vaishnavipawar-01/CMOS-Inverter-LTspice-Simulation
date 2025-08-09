# CMOS Inverter Design & Simulation in LTspice

## 📌 Overview
This project demonstrates the design and simulation of a **CMOS inverter** using LTspice.  
Both **DC analysis** and **transient analysis** are performed to study:
- Voltage Transfer Characteristics (VTC)
- Propagation delay
- Rise & fall times

---

## 🛠 Tools Used
- **LTspice XVII** (Analog Devices)
- Default NMOS & PMOS models provided by LTspice

---

## ⚡ Circuit Schematic
![Circuit Schematic](Schematic/ckt.png)

---

## 📊 Simulation Results

### 1️⃣ DC Analysis
**Purpose:** To determine the switching threshold and noise margins.

- **Switching Threshold (Vth):** ~ 2.5 V  
- **Noise Margin High (NMH):** ~ 2.4 V  
- **Noise Margin Low (NML):** ~ 2.4 V  

![DC Analysis](Simulation/DC_analysis.png)

---

### 2️⃣ Transient Analysis
**Purpose:** To observe the inverter output for a pulse input and measure delay.

- **Rise Time (tr):** ~ 10 ns  
- **Fall Time (tf):** ~ 8 ns  
- **Propagation Delay (tp):** ~ 9 ns  

![Transient Analysis](Simulation/transient_analysis.png)

---

## 📈 Key Observations
- Ideal switching near Vdd/2.
- Symmetrical rise and fall times indicate well-sized PMOS/NMOS pair.
- CMOS inverters consume negligible static power except during switching.

---

## 📚 How to Run the Simulation
1. Open `ckt.asc` in LTspice.
2. For DC Analysis:  
   - Add `.dc V1 0 5 0.01`
   - Run simulation and plot `V(out)` vs `V(in)`.
3. For Transient Analysis:  
   - Add `.tran 0 200n`
   - Input source: `PULSE(0 5 0 1n 1n 50n 100n)`
   - Plot `V(in)` and `V(out)`.

---

## 🏷 Applications
- Understanding CMOS logic basics.
- Introductory VLSI design experiments.
- Low-power digital design study.

---

## 📜 License
MIT License — Free to use and modify.

---
