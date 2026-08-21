# 🔋 Closed-Loop DC-DC Buck Converter with PCB

A hardware implementation of a **closed-loop DC-DC Buck Converter** designed and developed as part of the Power Electronics Laboratory at IIT Guwahati.

The project converts a higher DC input voltage into a regulated lower DC output voltage using **PWM control and feedback voltage sensing**. The complete system was designed, assembled and implemented on a custom PCB.

---

## ⚡ What is a Buck Converter?

A **Buck Converter** is a DC-DC power converter used to step down DC voltage.

The ideal output voltage is approximately:

 \(V_{out} = D \times V_{in}\)

where:

- \(V_{in}\) = Input DC voltage
- \(V_{out}\) = Output voltage
- \(D\) = Duty Cycle

In the **closed-loop configuration**, the output voltage is continuously sensed and compared with the desired reference. The feedback signal is used to control the PWM duty cycle and maintain a regulated output.

---

## 🔄 Working Principle

The converter operates through the following stages:

**DC Input → MOSFET Switching → Inductor → Output Filter → Load**

The output voltage is sensed using a resistor-divider network and fed to the feedback/control circuit. The controller adjusts the PWM signal according to the output voltage, providing closed-loop regulation.

**Basic control loop:**

`Output Voltage → Voltage Sensing → Feedback → PWM Control → MOSFET → Buck Converter`

<!-- Add image here: Overall/Block diagram of the closed-loop Buck Converter -->

---

## 🔌 1. Buck Main Circuit

The main power stage consists of the switching MOSFET, freewheeling diode, inductor, output capacitors and resistive load.

The MOSFET acts as the main switching device. The inductor stores and transfers energy, while the diode provides the current path when the MOSFET is OFF. The output capacitors reduce voltage ripple.

### Main Components

- MOSFET
- Diode
- Inductor
- Capacitors
- Resistors
- Heat Sink
- Input/Output Connectors

<!-- Add image here: Buck Main Circuit -->

---

## 📏 2. Output Voltage Sensing & Feedback

The output voltage is measured using a **resistor-divider network**. The sensed voltage is scaled down and provided to the feedback/control section.

The feedback circuit continuously monitors the output and helps maintain the required output voltage by controlling the switching duty cycle.

<!-- Add image here: Output Voltage Sensing Circuit -->

---

## ⚙️ 3. Gate Driver Circuit

The gate-driver section provides the required gate-driving signal for the power MOSFET.

It provides electrical isolation and suitable drive conditions between the PWM control signal and the MOSFET gate, allowing reliable high-frequency switching.

<!-- Add image here: Gate Driver Circuit -->

---

## 🖥️ 4. PCB Design

The complete Buck Converter hardware was implemented on a **custom-designed PCB**.

The PCB layout includes the power stage, switching device, inductor, filtering components, sensing section, driver circuit and required connectors. Proper routing was used for the power and control sections.

<!-- Add image here: PCB Design / PCB Layout -->

---

## 🧩 5. Hardware Implementation

The designed circuit was physically assembled and tested as a hardware prototype.

The final setup integrates the **power stage, feedback sensing, gate driver and PCB**, forming a complete closed-loop Buck Converter system.

<!-- Add image here: Final Hardware / PCB Photograph -->

---

## 📋 Component Overview

| Component | Purpose |
|---|---|
| MOSFET | High-frequency switching |
| Diode | Freewheeling current path |
| Inductor | Energy storage and current smoothing |
| Capacitors | Filtering and ripple reduction |
| Resistors | Voltage sensing and circuit control |
| Optocoupler | Signal isolation |
| Heat Sink | MOSFET thermal management |
| Connectors | Input, output and signal connections |

---

## 📐 Key Formula

For an ideal Buck Converter:

\[
\boxed{V_{out}=D\,V_{in}}
\]

Therefore,

\[
\boxed{D=\frac{V_{out}}{V_{in}}}
\]

where \(D\) represents the PWM duty cycle.

---

## ✅ Conclusion

A complete **closed-loop DC-DC Buck Converter** was successfully designed and implemented as a hardware project.

The project involved the design of the **power stage, output voltage sensing, gate-driver circuit and custom PCB**, providing practical experience in power electronics, switching converters, feedback control and PCB design.


