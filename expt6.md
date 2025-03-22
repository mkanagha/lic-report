# Experiment 6
## Aim: 
Design and analyse current mirror circuit as a  active load in amplifier circuit.
## Circit diagram:  
**Part A**


![Image](https://github.com/user-attachments/assets/eae4e924-2b8e-48bd-8642-c0476619949e)



**Part B** 
![Image](https://github.com/user-attachments/assets/1a3cc7d7-b1b4-4551-93a4-d08dda42fc8b)



## Theory:
A current mirror is a circuit that copies a reference current (I_REF) to one or more output branches while maintaining a constant current regardless of load variations. The circuit is widely used in analog IC design, particularly in biasing circuits, active loads, and current sources.  
The fundamental concept behind a current mirror is that two matched transistors (MOSFETs) with the same gate-source voltage (V_GS) should conduct the same drain current if they operate in the saturation region.  
For MOSFETs operating in saturation, the drain current is given by:
![Image](https://github.com/user-attachments/assets/eb3e0505-5b88-4365-a8e0-9ddf5eeb9d01)  
where:
𝜇𝑛= Electron mobility  
𝐶𝑜𝑥= Gate oxide capacitance per unit area  
W/L = Width-to-length ratio of the MOSFET  
VGS = Gate-to-source voltage  
VTH= Threshold voltage  
If two MOSFETs are identical (same W/L ratio and process parameters) and have the same V_GS, they should theoretically conduct the same drain current.  
## Procedure:
**Part A**  
1)Desgin for Av<=-10V/V  
Vdd=1.8V  
p<=1mW  
Design for current mirror ratio 1:1 and 1:2.  
2) Analysis the current mirror circuit. DC analysis.  
3)  Analyse the current mirroring maintain W/L same as first design.  
**case 1)** L=180n (W/L)=x  
**case 2)** L=500n (W/L)= x  
**case 3)** L=1u (W/L)=x  
4) Transient and AC analysis.    
To analysis: Max output swing and bandwidth.   
___
**Part B**  
Design the differential amplifer using the same desgin specification as experiment 3.  
perform DC analysis, Transient analysis and AC analysis.  
___  
## Calulation :
![Image](https://github.com/user-attachments/assets/b2b17a7b-181b-4ccc-8997-b7a1b983458d)  
## Design for current mirror ratio 1:1, when L=180nm
I_REF=I_X  
 (W/L) Of mosfet 1: 13.5u/180n  
 (W/L) Of mosfet 2:  13.5u/180n  
 (W/L) Of mosfet 3:  13.5u/180n

![Image](https://github.com/user-attachments/assets/dbb4ba08-e501-4185-8c41-4e788c5bb515)




  
