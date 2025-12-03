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
<img width="817" height="826" alt="image" src="https://github.com/user-attachments/assets/d11f373d-d22c-428f-9107-37e0d21d6bf6" />

# Test Circuit
The test circuit applies differential AC signals to evaluate the small-signal gain, bandwidth, and phase response of the designed op-amp. Supply sources and bias currents are provided to ensure correct operating points for both stages. The output node is monitored under load conditions to verify overall stability and transient behavior.

<img width="1043" height="761" alt="image" src="https://github.com/user-attachments/assets/dfc270a3-0dd3-4fa9-9174-ad47596ccc0d" />

# Transient Analysis
<img width="1910" height="850" alt="image" src="https://github.com/user-attachments/assets/f4a4af85-050f-4737-af6e-add97ff5e87b" />

# Bode Plot
<img width="1910" height="850" alt="image" src="https://github.com/user-attachments/assets/f2f6c347-8d4a-4ab0-ad37-be89435a9b6b" />
<img width="1169" height="247" alt="image" src="https://github.com/user-attachments/assets/9aad1b33-19e6-4768-8513-743be0225807" />

# DC Analysis
<img width="1910" height="850" alt="image" src="https://github.com/user-attachments/assets/95430d91-3ea4-4de3-8efb-84c72bc6a7c6" />



















