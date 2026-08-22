# 🔋 Closed-Loop DC-DC Buck Converter with PCB

A hardware implementation of a **closed-loop DC-DC Buck Converter** designed and developed as a design project at IIT Guwahati under Sabri Nath Mam.

The project converts a higher DC input voltage into a regulated lower DC output voltage using **PWM control and feedback voltage sensing**. The complete system was designed, assembled and implemented on a custom PCB.

---

## ⚡ What is a Buck Converter?

A **Buck Converter** is a DC-DC power converter used to step down DC voltage.

The ideal output voltage is approximately:
Vout/Vin =D

where:
Vin = Input DC voltage, 
Vout = Output voltage, 
D = Duty Cycle

In the **closed-loop configuration**, the output voltage is continuously sensed and compared with the desired reference. The feedback signal is used to control the PWM duty cycle and maintain a regulated output.

---

## 🔄 Working Principle

The converter operates through the following stages:

**DC Input → MOSFET Switching → Inductor → Output Filter → Load**

The output voltage is sensed using a resistor-divider network and fed to the feedback/control circuit. The controller adjusts the PWM signal according to the output voltage, providing closed-loop regulation.


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
<img width="1295" height="802" alt="Screenshot 2026-08-21 233110" src="https://github.com/user-attachments/assets/a9520151-6e9b-4c3b-a230-82289be4338f" />

<!-- Add image here: Buck Main Circuit -->

---

## 📏 2. Output Voltage Sensing & Feedback

The output voltage is measured using a **resistor-divider network**. The sensed voltage is scaled down and provided to the feedback/control section.

The feedback circuit continuously monitors the output and helps maintain the required output voltage by controlling the switching duty cycle.
<img width="1297" height="790" alt="Screenshot 2026-08-21 233125" src="https://github.com/user-attachments/assets/ae8177ec-9d82-4520-9545-52b62492e755" />

<!-- Add image here: Output Voltage Sensing Circuit -->

---

## ⚙️ 3. Gate Driver Circuit

The gate-driver section provides the required gate-driving signal for the power MOSFET.

It provides electrical isolation and suitable drive conditions between the PWM control signal and the MOSFET gate, allowing reliable high-frequency switching.

<img width="1307" height="727" alt="Screenshot 2026-08-21 233151" src="https://github.com/user-attachments/assets/dbb0eb23-3c4e-481b-bb46-67885fd8cef0" />

<!-- Add image here: Gate Driver Circuit -->

---

## 🖥️ 4. PCB Design

The complete Buck Converter hardware was implemented on a **custom-designed PCB**.

The PCB layout includes the power stage, switching device, inductor, filtering components, sensing section, driver circuit and required connectors. Proper routing was used for the power and control sections.
<img width="607" height="623" alt="Screenshot 2026-08-22 000133" src="https://github.com/user-attachments/assets/8632914a-1c0c-49d3-bebc-4e229d61953f" />



<!-- Add image here: PCB Design / PCB Layout -->

---

## 🧩 5. Hardware Implementation

The designed circuit was physically assembled and tested as a hardware prototype.

The final setup integrates the **power stage, feedback sensing, gate driver and PCB**, forming a complete closed-loop Buck Converter system.

<img width="4624" height="3472" alt="IMG_20260424_091314" src="https://github.com/user-attachments/assets/b4ede9aa-3071-4755-8324-92a9aed39bda" />

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
📊 Results & Observations

The closed-loop Buck Converter was tested for the designed operating conditions. The measured output voltage and inductor current were observed using an oscilloscope.

For a 30 V input and 0.75 duty ratio, the theoretical output voltage is 22.5 V, while the measured output voltage was approximately 21.4 V. The observed inductor current was approximately 424 mA, confirming the expected continuous-conduction operation.

The practical results show that the converter successfully steps down the input voltage and maintains a stable output through the feedback-based control system.

<img width="1022" height="693" alt="Screenshot 2026-08-22 093023" src="https://github.com/user-attachments/assets/e2ebafca-0a80-4d4f-94ba-c6b1df2eaca4" />
<img width="1001" height="622" alt="Screenshot 2026-08-22 093036" src="https://github.com/user-attachments/assets/e50fe860-dbab-48b8-9472-1c3ed1a8d9b2" />

---
🎥 Demo Video

The working demonstration of the Closed-Loop Buck Converter is shown in the project demo video.

Demo: "C:\Users\HP\Downloads\whatsapp-video-2026-08-21-at-111043-pm_aFm9mGvO.mp4"

## ✅ Conclusion

A complete **closed-loop DC-DC Buck Converter** was successfully designed and implemented as a hardware project.

The project involved the design of the **power stage, output voltage sensing, gate-driver circuit and custom PCB**, providing practical experience in power electronics, switching converters, feedback control and PCB design.


<!-- Failed to upload "whatsapp-video-2026-08-21-at-111043-pm_wb68g3rv.mp4" -->


