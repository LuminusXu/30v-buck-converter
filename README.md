# 30v-buck-converter
Buck Converter Design &amp; Simulation Designed and simulated a non-synchronous 30V-to-5V DC-DC buck converter in LTspice. Features active thermal protection via NTC-comparator network, transient overvoltage "crowbar" protection, and RC snubbers for EMI/ringing suppression.

# LTspice Buck Converter Design & Analysis

This repository documents the design, theoretical analysis, and LTspice simulation of a non-synchronous step-down DC-DC buck converter. The project was engineered to convert a 24V DC input into a regulated 5V DC output with a 2A load capacity.

## 🛠️ Key Technical Features
* **Regulation:** Designed for 100kHz switching frequency in Continuous Conduction Mode (CCM) to ensure stable output regulation.
* **Active Thermal Protection:** Implemented an NTC thermistor-based sensing network with an LT6700 comparator to trigger a definitive system shutdown at critical thermal limits.
* **Crowbar Overvoltage Protection:** Designed a latching crowbar circuit using a 6.8V Zener diode (1N4736A) and BJT transistors (2N3904/2N3906) to divert energy and protect sensitive loads from transient overvoltage.
* **EMI & Transient Suppression:** Engineered an RC snubber network across the switching node to dampen high-frequency parasitic ringing, optimized as an engineering compromise between voltage stress reduction and thermal efficiency.
* **Reliability Engineering:** Conducted rigorous component stress and derating analysis (e.g., MOSFET/Diode voltage stress kept ~23%) to ensure long-term stability and align with IPC-9592B industry standards.

## ⚙️ Simulation Results
* **Efficiency:** Achieved an estimated 85.24% efficiency in simulation, with primary losses identified within the Schottky diode.
* **Transient Response:** Successfully validated stability through transient analysis, observing a damped overshoot followed by stabilization within 2ms.
* **Ripple Performance:** Achieved a low output voltage ripple of ~0.115%, significantly exceeding the design requirement of ≤1%.

## 📂 Repository Contents
* `buck_converter_design.asc`: The primary LTspice schematic file.
