# Experiment no 1
## Analysis of CS Amplifier using 180 nm technology file in LTspice simulator

## Aim of the Experiment
The aim of this experiment is to analyze the given MOSFET model by performing the following:  
a) **Operating Point Analysis**: Determine the DC biasing conditions, including node voltages and currents, to ensure proper transistor operation.  
b) **Transient Analysis**: Study the time-domain response of the circuit when subjected to a varying input signal.  
c) **AC Analysis**: To verfiy the gain vs frequency graph.  
## Absract 
This report presents an analysis of two MOSFET-based amplifier configurations: a common-source (CS) amplifier with a resistive load and a common-source amplifier with an active PMOS load. The study focuses on comparing gain, bandwidth, and power consumption using LTSpice simulations. The channel length is fixed at 180 nm, and the total power dissipation is constrained to 100 µW with . The results show that replacing with a PMOS current source significantly improves gain and bandwidth, while also affecting power dissipation. The impact of W/L ratio variation on performance is also discussed.
## Theroy
A common source amplifier is the amplifier configuration that is most frequently used in analog electronics. It provides high voltage enhancement and is typically used in signal amplification applications. The behavior of the amplifier is observed in three domains: DC analysis, distortion, operating point, and transient analysis, which assesses time. Remaining in the saturation region for proper reinforcement (VOV = VGS-VTH). The drain current is specified in
id = 1/2kn(vov)2
vds, and the ID provides the operating point of the MOSFET.Sudden changes in pulse input or voltage: how the amplifier responds to time signals such as: Operation is affected by the charge and discharge of capacitors, including coupling and bypass capacitors. 
## Components Required
- NMOS And PMOS Transistor
- Resistor (R1 = 3kΩ)
- DC Voltage Source (V1 = 1.8V)
- AC Signal Source (V2 = SINE(0.9 50m 1k))
  ## Circuit diagram
![Image](https://github.com/user-attachments/assets/b271e1b6-80c8-4d37-8714-79851d8a12f7)
 
## Circuit parameters
The NMOS operates in the saturation region, with acting as the load. The gain is determined by the transconductance and the drain resistance: Av=-(gm*Rd)
Uses a fixed as the load of Rd=3K ohm.
Vgs=0.9 V,Vdd=1.8 V,W=1250nm,L=180 nm
Power considered for design=100 µW
# operating point of the MOSFET 
![Image](https://github.com/user-attachments/assets/1fbaa9d8-8ccd-40b1-8fdd-a2b3e9919255)
# Transient analysis of the MOSFET 
![Image](https://github.com/user-attachments/assets/28dce660-56d6-41c0-a38f-b1be3c581b05)
![Image](https://github.com/user-attachments/assets/700cb4bb-e808-41e1-b874-1a22475e1218)

# AC Analysis of the MOSFET
![Image](https://github.com/user-attachments/assets/e2100f7b-022a-4c0f-a797-003958320766)
Gain:7.83dB 
# CS Amplifier with a PMOS Current Source (Active Load)
## circuit diagram
![Image](https://github.com/user-attachments/assets/e2c05b4f-7aed-4e8a-8bf0-5534593456f0)
Instead of a passive resistor, a PMOS acts as an active load, functioning as a current source. Offers higher gain due to increased output resistance. Av = -(gm*rop)
Vdd=1.8V,Vgs=0.9V,Vb=0.5V,W=2010 nm,L=180 nm
# Operating point 
![Image](https://github.com/user-attachments/assets/cf2a7a4f-48d7-4332-bb8f-f77ed6ac5b46)
# Transient analysis 

![Image](https://github.com/user-attachments/assets/5b6daeab-f9a6-4706-b9ec-a55b6636f601)
![Image](https://github.com/user-attachments/assets/5f7a83cf-5508-4e84-9257-7a2507eb98ba)

# AC analysis
![Image](https://github.com/user-attachments/assets/350dc2f0-da2b-4d59-86f6-d18e9a928a65)
Gain: 22 dB

# Result and Observation From simulation
## Comparison of two circuits
gain: the PMOS as a active load have more gain than nmos with Rd resistor 
gain with Rd : 7.83dB
gain with PMOS as active load: 22 dB
## Bandwidth(fH)
With Rd: ~4.1GHz
With PMOS Load: >196GHz
Higher bandwidth in PMOS configuration due to improved output impedance.
## Aspect ratio 
Increasing W/L of NMOS increases transconductance , improving gain and  
Increasing PMOS W/L increases output resistance, increasing gain but reducing bandwidth due to higher parasitic capacitance.
comparison :
aspect ratio of nmos with load resistor: W/L =0.203u/180n
aspect ratio of pmos as active load: W/L=2100n/180n
keeping the lenght of the MOSFET same in both the cases.
# Inference
From the LTspice simulation and analysis of the CS amplifier with a resistive load versus the CS amplifier with a PMOS current source (active load), we can draw the following conclusions:  
**Gain Improvement**:  
The gain of the CS amplifier with a passive resistor as the load is 7.83  dB
The gain significantly improves to 22dB when using a PMOS current source as an active load.  
This improvement is due to the higher output impedance provided by the active PMOS load.  
**Bandwidth Comparison**:  
The amplifier with a passive resistor has a bandwidth of approximately 4.1GHz.  
The amplifier with a PMOS current source has a bandwidth greater than 196GHz.  
The increased bandwidth in the PMOS load configuration is attributed to the improved output impedance.  
**Aspect Ratio Effects**:  
Increasing W/L of NMOS increases transconductance leading to higher gain.  
Increasing W/L of PMOS increases the output resistance, further improving gain but at the cost of increased parasitic capacitance, which may reduce bandwidth.  
The aspect ratio of the NMOS transistor in the resistive load circuit is 0.203 µm / 180 nm, while in the PMOS active load configuration, the PMOS aspect ratio is 2100 nm / 180 nm.  
**Power Consumption Considerations**:  
The total power dissipation is constrained to 100 µW in both cases.  
The PMOS active load configuration offers  power efficiency and performance.  

This experiment demonstrates the importance of optimizing W/L ratios and understanding the impact of different load configurations in MOSFET amplifier design.
The PMOS active load configuration achieves higher gain, better voltage swing, and improved bandwidth while maintaining the same power dissipation as the resistive load configuration. This makes it a more efficient choice for amplifier design.









 
    
