# Mixed-Signal-Circuit-Design
Analysis and Implementation of a Two-Stage Op-Amp with Enhanced Stability

A two-stage operational amplifier is a commonly used analog circuit designed to achieve a high voltage gain and wide output swing. It mainly has two stages: a differential amplifier as the input stage, which provides high input impedance and the first level of voltage gain, and a common-source or common-emitter amplifier as the second stage, which further increases the overall gain. For maintaining stability, a frequency compensation capacitor (generally a Miller capacitor) is connected between the stages to control the bandwidth and phase margin.

This architecture provides a good balance between gain, output voltage range, and stability. Because of these advantages, the two-stage op-amp is widely used in analog ICs, filters, and signal conditioning circuits. Its structure also makes it easier to adjust parameters like slew rate, gain-bandwidth product, and power efficiency.

# Circuit

![WhatsApp Image 2025-11-04 at 08 26 13_0e177c14](https://github.com/user-attachments/assets/dd2d3b70-b6ba-4f8c-b4c9-365dd47537bf)

# Design specifications

![WhatsApp Image 2025-11-04 at 08 07 27_01f76d7c](https://github.com/user-attachments/assets/a0255e70-fdee-455b-9a81-b20df74580af)

# Design steps
1. M1 and M2 form the differential pair which determines the gain of the amplifier.
2. The sizes of M1 and M2 are chosen to be equal (M1 = M2).
3. The tail current (I5) is split equally between M1 and M2 transistors, i.e., each gets I5/2.
4. M3 and M4 act as the active load for the differential pair.
5. For the tail NMOS transistor (M5), the VBIAS must be designed such that it provides the required tail current (I5).
6. If the desired current is known, designing VBIAS becomes straightforward.
7. M5 functions as the tail current source of the differential amplifier.

# Schematic

<img width="817" height="826" alt="image (1)" src="https://github.com/user-attachments/assets/d6b66642-7ee2-4138-884e-1083ed51faf1" />

# Simulation

![2 (1)](https://github.com/user-attachments/assets/18ff7c5f-e2f1-40e4-92b0-18ec17b09a19)









