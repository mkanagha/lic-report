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
 (W/L) Of mosfet 1(PMOS): 12.6u/180n  
 (W/L) Of mosfet 2(PMOS):  12.6u/180n    
 (W/L) Of mosfet 3(NMOS ):  6.3u/180n
 Vin = 0.6603V  
 ![Image](https://github.com/user-attachments/assets/9435623b-2b56-4cbd-93c4-2f43017efc0d)

Since both the mosfet have same current flowing through it. The Vgs, Vds values are as shown below.  
![Image](https://github.com/user-attachments/assets/ca89ef2c-bed2-401f-85d9-b6b101bfc1c4)

 
Saturation Condition for MOSFETs:
For an NMOS transistor to be in saturation:
VDS>VGS−Vth
​VDS=1.54
VGS=0.66
Vth=0.4V  
therefore MOSFET is in saturation.  
For PMOS (M1 & M2):

Saturation Condition:

∣𝑉𝑆𝐷∣>∣𝑉𝑆𝐺∣−∣𝑉𝑡ℎ∣
M1:
𝑉𝑆𝐷=1.26𝑉,
𝑉𝑆𝐺=0.53𝑉,
𝑉𝑡ℎ=−0.4𝑉
VSD=1.26V,
VSG=0.53V,
Vth=−0.4V
1.26𝑉>(0.53𝑉−(−0.4𝑉))=0.93𝑉
In Saturation.

M2:
𝑉𝑆𝐷=1.79𝑉,
𝑉𝑆𝐺=0𝑉,
𝑉𝑡ℎ=−0.4𝑉
VSD=1.79V,
VSG=0V,
Vth=−0.4V
1.79𝑉>(0𝑉−(−0.4𝑉))=0.4𝑉
In Saturation.  
All three MOSFET are in saturation. 
**Transient Analysis**
Vin  
![Image](https://github.com/user-attachments/assets/85aeb216-5b66-4c4e-97b2-9b02e661ef2f)  
Vout  

![Image](https://github.com/user-attachments/assets/f0440ce6-d395-4b34-b2f3-1805fc6b01d9)  
Vout max swing(peak to peak) = 1.68V- 0.971V= 0.709V 
If considering max positive swing from DC operating point (1.54V), it is 1.68V - 1.54V = 0.14V.  
If considering max negative swing from DC operating point, it is 1.54V - 0.91V = 0.63V.  
**AC analysis**  
![image](https://github.com/user-attachments/assets/bffde00e-e5e2-4139-8614-7ab03d8d1889)

The Gain of this is 16dB.  
**For 1:2 ratio current mirror**

let I_REF=0.185mA and I_X=2*I_REF=0.37mA since the I_TOTAL is remines same and hence P_TOTAL remains same.  
Here ,The aspect ratio of MOSFET M1 is twice of M2.
(W/L) of MOSFET 1= 200u/180n.  
(W/L) of MOSFET 2= 100u/180n.  
(W/L) of MOSFET 3= 8.115u/180n. 
**DC ANALYSIS**  
![image](https://github.com/user-attachments/assets/65fc03a8-78f0-458b-bc6c-879e4d522570)  
Current through M1 and M3 is same (0.37mA)  
vout and vx has been incresed from the previous case.  
**Transient Analysis**  
vin  
![image](https://github.com/user-attachments/assets/66b2d1d2-3827-456e-b3b8-4b49d0440e7d)
vout  
![image](https://github.com/user-attachments/assets/cb9f4dc7-4ff1-4358-a861-98365717a074)  
Max o/p swing(peak to peak) = 1.766-1.691=0.075V   
**AC analysis**  
![image](https://github.com/user-attachments/assets/37ca2b25-4a47-459c-8bc8-872e492c17c2)
The gain is 15dB.
**For 1:3 ratio current Mirror**   
let I_REF=0.138mA and I_X=3*I_REF =0.4166mA

since the I_TOTAL is remines same P_TOTAL also remains same.
Here ,The aspect ratio of MOSFET M1 is thrice of M3.
(W/L) of MOSFET 1= 300u/180n.  
(W/L) of MOSFET 2= 100u/180n.  
(W/L) of MOSFET 3= 13.36u/180n. 
**DC ANANLYSIS**  
![image](https://github.com/user-attachments/assets/7734a9ba-00c0-4322-acea-6a85477c0137)  
**TRANSIENT ANALYSIS**  
Vin
![image](https://github.com/user-attachments/assets/f976a74a-e31a-4afd-b4b8-6e35bed8a131)  
Vout
![image](https://github.com/user-attachments/assets/d557cce1-0674-481e-abb3-cc45dbae897a)
Max o/p swing(peak to peak) = 1.732-0.325 =1.407V 
**AC analysis**  
![image](https://github.com/user-attachments/assets/96f2b9fe-e7bb-4a60-a576-da4a6ac1540a)
The gain is increased to 28dB.  
**For 1:4 ratio current Mirror**   
let I_REF=0.111mA and I_X=4*I_REF =0.4444mA

since the I_TOTAL is remines same P_TOTAL also remains same.
Here ,The aspect ratio of MOSFET M1 is thrice of M3.
(W/L) of MOSFET 1= 400/180n.  
(W/L) of MOSFET 2= 100u/180n.  
(W/L) of MOSFET 3= 14.14u/180n. 

**DC Analysis**
![image](https://github.com/user-attachments/assets/460138db-dc77-4a2e-a416-26891e9b7df0)
**Transient Analysis**  
Vin
![image](https://github.com/user-attachments/assets/f70a534f-a2d5-4b98-842c-1e4b50f4911a)
Vout  
![image](https://github.com/user-attachments/assets/4b3e687f-39e7-4df2-be3d-d88d84d39c19)
Max o/p swing(peak to peak) = 1.733-0.332=1.401 V  
**AC analysis**  
![image](https://github.com/user-attachments/assets/f231c4d7-2a08-4e90-88fb-d90eaffbb555)  
The gain is 30dB.  
**For 2:1 ratio current Mirror**   
let I_REF=0.37mA and I_X=I_REF/2=0.185mA  

since the I_TOTAL is remines same P_TOTAL also remains same.  
Here ,The aspect ratio of MOSFET M1 is thrice of M3.  
(W/L) of MOSFET 1= 200/180n.  
(W/L) of MOSFET 2= 100u/180n.  
(W/L) of MOSFET 3= 5.75u/180n. 

**DC Analysis**  
![image](https://github.com/user-attachments/assets/fba0d105-9cca-4621-9ff4-b8b954fbeb06)  
**Transient Analysis**  
Vin  
![image](https://github.com/user-attachments/assets/341cf66f-a3b7-4125-a36c-63c9ba7999df)  
Vout  
![image](https://github.com/user-attachments/assets/dbcc82de-4570-4b78-ae37-c8b502cc1521)
**AC Analysis**  
![image](https://github.com/user-attachments/assets/90c12279-5470-461f-a83d-99add2a99be2)
The gain is 28dB.  

| Current Mirror Ratio | I_REF (mA) | I_X (mA) | V_IN (V) | V_OUT (V) | V_X (V) | Gain (dB) |
|----------------------|------------|----------|----------|----------|----------|-----------|
| 1:1                | 0.185      | 0.185    | 0.6603     | 1.54     | 1.066    | 16        |
| 1:2                | 0.185      | 0.37     | 0.6603     | 1.7417   | 1.23011  | 15        |
| 1:3                | 0.138      | 0.4166   | 0.6603     | 1.2151   | 1.24607  | 28        |
| 1:4                | 0.111      | 0.4444   | 0.6603     | 1.24656  | 1.2574   | 30        |
| 2:1                | 0.37       | 0.185    | 0.6603     | 1.22783  | 1.23002  | 28        |

## Analysis of copying / mirroring of current when current mirror ratio is varied
## Differential amplifier using Current mirror



## Inference  









  
