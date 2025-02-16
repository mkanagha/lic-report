# Experiment no 1
## Analysis of CS Amplifier using 180 nm technology file in LTspice simulator

## Aim of the Experiment
The aim of this experiment is to analyze the given MOSFET model by performing the following:
a) **Operating Point Analysis**: Determine the DC biasing conditions, including node voltages and currents, to ensure proper transistor operation.
b) **Transient Analysis**: Study the time-domain response of the circuit when subjected to a varying input signal.
c) **AC Analysis**: To verfiy the gain vs frequency graph.
## Absract 
This report presents an analysis of two MOSFET-based amplifier configurations: a common-source (CS) amplifier with a resistive load and a common-source amplifier with an active PMOS load. The study focuses on comparing gain, bandwidth, and power consumption using LTSpice simulations. The channel length is fixed at 180 nm, and the total power dissipation is constrained to 100 µW with . The results show that replacing with a PMOS current source significantly improves gain and bandwidth, while also affecting power dissipation. The impact of W/L ratio variation on performance is also discussed.

## Components Required
- NMOS And PMOS Transistor
- Resistor (R1 = 3kΩ)
- DC Voltage Source (V1 = 1.8V)
- AC Signal Source (V2 = SINE(0.9 50m 1k))
  ## Circuit diagram
![Image](https://github.com/user-attachments/assets/59ceb1e1-c123-48f7-bc9a-d02b40dbb94e)
## Theroy
A common source amplifier is the amplifier configuration that is most frequently used in analog electronics. It provides high voltage enhancement and is typically used in signal amplification applications. The behavior of the amplifier is observed in three domains: DC analysis, distortion, operating point, and transient analysis, which assesses time. Remaining in the saturation region for proper reinforcement (VOV = VGS-VTH). The drain current is specified in
id = 1/2kn(vov)2
vds, and the ID provides the operating point of the MOSFET.Sudden changes in pulse input or voltage: how the amplifier responds to time signals such as: Operation is affected by the charge and discharge of capacitors, including coupling and bypass capacitors. 
## Circuit parameters
The NMOS operates in the saturation region, with acting as the load. The gain is determined by the transconductance and the drain resistance: Av=-(gm*Rd)
Uses a fixed as the load of Rd=3K ohm.
Vgs=0.9 V,Vdd=1.8 V,W=1250nm,L=180 nm
Power considered for design=100 µW
# operating point of the MOSFET 
![Image](https://github.com/user-attachments/assets/9330dddb-2248-489d-90f9-68af0b6a4f5f)
# Transient analysis of the MOSFET 
![Image](https://github.com/user-attachments/assets/662890ad-32f7-4179-8fa9-236a4749c7c7)
![Image](https://github.com/user-attachments/assets/0c8aaddf-7480-44c2-ad58-87989c78a9e9)
# AC Analysis of the MOSFET
![Image](https://github.com/user-attachments/assets/45cf6212-da0d-42a3-bb2f-3edafde4df84)
Gain:2.2 V/V , 6.8 dB
# CS Amplifier with a PMOS Current Source (Active Load)
## circuit diagram













 
    
