🔋 Closed-Loop DC-DC Buck Converter with PCB
Introduction

This project presents the design and hardware implementation of a closed-loop DC-DC Buck Converter developed as part of a Power Electronics project at IIT Guwahati.

The converter is designed to step down a DC input voltage to a regulated lower output voltage using a feedback-based closed-loop control system. The hardware implementation includes the main buck converter circuit, output-voltage sensing circuit, gate-driver circuit, and custom PCB design.

The feedback circuit continuously senses the output voltage and adjusts the switching control of the MOSFET to maintain a stable output voltage under changing operating conditions.

The project covers the complete hardware development process, from circuit design and PCB layout to hardware testing and demonstration.

⚡ Buck Converter – Main Power Circuit

The Buck Converter Main Circuit forms the core power stage of the project. It is designed to step down the input DC voltage to a lower regulated DC voltage using high-frequency MOSFET switching.

🔧 Key Components & Functions
🔹 MOSFET (IRF540NPBF) — Acts as the main high-speed switching device.
🔹 Freewheeling Diode (D1) — Provides a current path when the MOSFET is OFF.
🔹 Inductor (104 µH) — Stores and releases energy to maintain continuous output current.
🔹 Output Capacitors (C4, C5) — Reduce output-voltage ripple and provide a smoother DC output.
🔹 Gate Resistor (R3) — Connected to the MOSFET gate for proper gate-drive operation.
🔹 Input Capacitor (C1) — Helps reduce input-side voltage fluctuations.
🔹 Voltage Divider (R4, R5, R6) — Used for output-voltage sensing and feedback.
🔹 Heat Sinks — Provided for thermal management of the power semiconductor devices.
🔹 Connectors — Separate terminals are provided for input, output, ground, and gate-signal connections.
⚙️ Working Principle

The MOSFET is switched ON and OFF at high frequency. During the ON state, energy is transferred from the input source to the inductor and load. During the OFF state, the inductor maintains the load current through the freewheeling diode.

The inductor and capacitors smooth the switched waveform, producing a lower DC output voltage. The sensed output voltage can then be used by the feedback circuit to regulate the converter.

<img width="1517" height="790" alt="Screenshot 2026-08-21 231745" src="https://github.com/user-attachments/assets/cf7f61a1-6173-43d9-889c-2edaa792f9de" />


## 🖥️ PCB Design

The PCB was designed to achieve a **compact, organized, and reliable hardware implementation** of the closed-loop Buck Converter.

✨ **Key Design Highlights:**

* 🔹 **Integrated Power Stage** — MOSFET, diode, inductor and capacitors arranged on a single PCB.
* 🔹 **Gate Driver Section** — Dedicated area for driving the power MOSFET.
* 🔹 **Voltage Sensing** — Feedback/sensing circuitry incorporated for closed-loop regulation.
* 🔹 **Power Routing** — Suitable PCB tracks provided for the power-current path.
* 🔹 **Organized Layout** — Components strategically placed for clean and practical connections.
* 🔹 **External Connections** — Input, output and control/sensing terminals provided for testing.
* 🔹 **Hardware Ready** — The fabricated PCB was used for practical testing and demonstration.

### 📐 PCB Layout

*The PCB layout of the designed Closed-Loop Buck Converter is shown below.*
<img width="607" height="623" alt="Screenshot 2026-08-22 000133" src="https://github.com/user-attachments/assets/8e885557-3f27-4ad1-8de0-b431813e942b" />

## 🎯 Output Voltage Sensing & Feedback Circuit

The **Output Voltage Sensing Circuit** is an important part of the closed-loop Buck Converter. It monitors the converter output and generates a **feedback signal** that can be used to regulate the output voltage.

### 🔧 Key Design Highlights

* 🔹 **Voltage Divider Network** — Resistors **R20, R18 and R21** scale the Buck output voltage to a suitable sensing level.
* 🔹 **Error Amplifier (LF347)** — Compares the sensed output voltage with the reference/feedback signal.
* 🔹 **Feedback Network** — **R17, R19 and R22** provide the required feedback path around the op-amp.
* 🔹 **Protection Components** — **D4, D5, D8 and D9** are included for voltage protection/clamping.
* 🔹 **Dual Supply** — The LF347 is supplied using **+12 V and −12 V** rails.
* 🔹 **Output Feedback** — The op-amp output provides the control/feedback signal for the closed-loop system.
* 🔹 **Connectors** — Dedicated connectors are provided for the sensed voltage, supply and output connections.

### ⚙️ Working Principle

The **Buck output voltage** is first scaled through the resistor network. This reduced voltage is applied to the **LF347 op-amp**, where it is processed through the feedback network.

The resulting error/control signal is used by the closed-loop control system to adjust the switching operation of the converter, helping maintain the desired output voltage.

### 📐 Voltage Sensing Circuit

*The designed output-voltage sensing and feedback circuit is shown below.*

<img width="1297" height="790" alt="Screenshot 2026-08-21 233125" src="https://github.com/user-attachments/assets/a1e65b9d-53df-4e0b-b40f-4d972ed57ecb" />




