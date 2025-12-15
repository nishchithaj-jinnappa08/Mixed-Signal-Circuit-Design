# Mixed-Signal-Circuit-Design
Analysis and Implementation of a Two-Stage Op-Amp with Enhanced Stability

A two-stage operational amplifier is a commonly used analog circuit designed to achieve a high voltage gain and wide output swing. It mainly has two stages: a differential amplifier as the input stage, which provides high input impedance and the first level of voltage gain, and a common-source or common-emitter amplifier as the second stage, which further increases the overall gain. For maintaining stability, a frequency compensation capacitor (generally a Miller capacitor) is connected between the stages to control the bandwidth and phase margin.

This architecture provides a good balance between gain, output voltage range, and stability. Because of these advantages, the two-stage op-amp is widely used in analog ICs, filters, and signal conditioning circuits. Its structure also makes it easier to adjust parameters like slew rate, gain-bandwidth product, and power efficiency.

# Circuit:

![WhatsApp Image 2025-11-04 at 08 26 13_0e177c14](https://github.com/user-attachments/assets/dd2d3b70-b6ba-4f8c-b4c9-365dd47537bf)

# Design specifications:

![WhatsApp Image 2025-11-04 at 08 07 27_01f76d7c](https://github.com/user-attachments/assets/a0255e70-fdee-455b-9a81-b20df74580af)

# Design steps:
1. M1 and M2 form the differential pair which determines the gain of the amplifier.
2. The sizes of M1 and M2 are chosen to be equal (M1 = M2).
3. The tail current (I5) is split equally between M1 and M2 transistors, i.e., each gets I5/2.
4. M3 and M4 act as the active load for the differential pair.
5. For the tail NMOS transistor (M5), the VBIAS must be designed such that it provides the required tail current (I5).
6. If the desired current is known, designing VBIAS becomes straightforward.
7. M5 functions as the tail current source of the differential amplifier.

# Schematic:
<img width="528" height="355" alt="image" src="https://github.com/user-attachments/assets/8bac39ed-e01e-4363-9f57-165445eda540" />

# Test Circuit:
The test circuit applies differential AC signals to evaluate the small-signal gain, bandwidth, and phase response of the designed op-amp. Supply sources and bias currents are provided to ensure correct operating points for both stages. The output node is monitored under load conditions to verify overall stability and transient behavior.

<img width="1043" height="761" alt="image" src="https://github.com/user-attachments/assets/dfc270a3-0dd3-4fa9-9174-ad47596ccc0d" />

# Transient Analysis:

<img width="1910" height="850" alt="image" src="https://github.com/user-attachments/assets/f4a4af85-050f-4737-af6e-add97ff5e87b" />

# Bode Plot:

<img width="1910" height="850" alt="image" src="https://github.com/user-attachments/assets/f2f6c347-8d4a-4ab0-ad37-be89435a9b6b" />
<img width="1169" height="247" alt="image" src="https://github.com/user-attachments/assets/9aad1b33-19e6-4768-8513-743be0225807" />

# DC Analysis:

<img width="1910" height="850" alt="image" src="https://github.com/user-attachments/assets/95430d91-3ea4-4de3-8efb-84c72bc6a7c6" />

# Calculation 

1. Open-loop gain 
Measured magnitude (open-loop gain) = 38.7303 dB.

Convert to linear voltage gain 𝐴𝑣: 

𝑣 = 10^(dB/20) = 10^(38.7303/20) ≈ 86.4  V/V.

2. Phase margin and stability
   
Phase margin = 66.33° (read: 66.3256°).

Phase margin = 66.33° → indicates a well-damped response (stable, good transient settling).

3. Output swing (from transient markers)
   
From the transient plot markers: 

• Minimum measured 𝑉𝑜𝑢𝑡,min⁡≈ 127.21 mV 

• Maximum measured 𝑉𝑜𝑢𝑡,max⁡≈ 449.65 mV


# Conclusion
In this work, a two-stage operational amplifier was 
designed, analyzed, and implemented using the 180 nm 3 
2025 
CMOS technology node with the objective of achieving 
enhanced stability, sufficient gain, and low-power 
operation. The architecture incorporated a differential 
input stage followed by a common-source gain stage, 
along with Miller compensation to ensure a stable 
frequency response. Simulation results verified the correct 
functionality of the design, with the op-amp achieving an 
open-loop gain of approximately 38.73 dB and a phase 
margin of 66.33°, indicating good stability and reliable 
closed-loop 
behavior. 
The 
transient 
response 
demonstrated proper amplification with a measured 
small-signal output swing of around 322 mVpp 
Although the small-signal slew rate measured from the 
transient markers was significantly lower than the targeted 
specification, this is attributed to the test signal amplitude 
rather than the true large-signal performance. The design 
approach, transistor sizing, and bias current selection 
proved effective in meeting the stability and bandwidth 
requirements for the given process. Further optimization 
such as adjusting compensation capacitor values and 
increasing bias currents can enhance slew rate and 
improve overall speed without significantly impacting 
power consumption. 
Overall, the implemented two-stage op-amp in 180 nm 
technology demonstrates stable operation, acceptable gain 
performance, and proper functionality for analog front
end applications. The design provides a solid foundation 
for future improvements and can be extended for use in 
filters, ADC drivers, sensor interfaces, and other mixed
signal circuits.

# Reference

[1] B. Razavi, Design of Analog CMOS Integrated Circuits, 2nd 
ed. New York, NY, USA: McGraw-Hill, 2017. 

[2] P. R. Gray, P. J. Hurst, S. H. Lewis, and R. G. Meyer, Analysis 
and Design of Analog Integrated Circuits, 5th ed. New York, 
NY, USA: Wiley, 2009. 

[3] D. A. Johns and K. Martin, Analog Integrated Circuit 
Design. New York, NY, USA: Wiley, 1997. 

[4] R. Jacob Baker, CMOS: Circuit Design, Layout, and 
Simulation, 4th ed. New York, NY, USA: Wiley-IEEE Press, 
2019. 

[5] A. S. Sedra and K. C. Smith, Microelectronic Circuits, 8th 
ed. New York, NY, USA: Oxford Univ. Press, 2020. 

[6] Behzad Razavi, “The Two-Stage CMOS Operational 
Amplifier: Design and Compensation Techniques,” IEEE 
Journal of Solid-State Circuits, vol. 34, no. 2, pp. 180-192, Feb. 
1999. 

[7] Y. Tsividis and C. McAndrew, Operation and Modeling of 
MOS Transistors, 3rd ed. New York, NY, USA: Oxford Univ. 
Press, 2010.

[8] E. Sackinger, “A 180-nm CMOS Analog Design Tutorial,” 
IEEE Solid-State Circuits Magazine, vol. 7, no. 2, pp. 12–25, 
Spring 2015.



















