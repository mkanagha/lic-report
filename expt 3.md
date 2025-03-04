# Experiment-3  
# Title: To Design Differential Amplifier  
## Aim : Design and analyse the MOS differential amplifier ckt for the following specifications Vdd=2V, P<=1mW,Vin=1V, Vocm=1.1V,Vp=0.4.  
Perform DC analysis, transient analysis,frequency respose and extract the required parameters.  
## Circuit Diagram
**With Resistor Rss.**  
![Image](https://github.com/user-attachments/assets/36031ebb-1406-4f04-96cd-192fd445c1f2)  
**With current source**  
![Image](https://github.com/user-attachments/assets/f4708ed9-d9f8-4465-ba04-ee07d79cff9e)  

**When the current source is replaced by NMOSFET**  
![Image](https://github.com/user-attachments/assets/2a208a29-d99b-42bb-8d9a-e49d194c0abd)
## Theory
A differential amplifier is a circuit that amplifies the difference between two input signals while rejecting any signals common to both inputs. It is widely used in analog circuit design, particularly in operational amplifiers and communication systems.

The basic differential amplifier consists of two identical transistors with their emitters (or sources in MOSFETs) connected together and biased by a current source. The outputs are taken from the collectors (or drains) of the transistors. The circuit operates based on the difference between the two input voltages, making it highly effective in eliminating common-mode noise and interference.

In an ideal differential amplifier, only the differential input signal affects the output, while any common-mode signal is completely rejected. However, in practical implementations, factors such as mismatched components and circuit imperfections introduce some degree of common-mode gain.

The circuit can be analyzed using small-signal models to determine its gain, input impedance, and output characteristics. The gain of a differential amplifier is determined by the transconductance of the transistors and the load resistance used in the circuit. For improved performance, active loads such as current mirrors are often used instead of resistors.

Differential amplifiers are fundamental components in modern electronic systems, forming the input stage of most operational amplifiers and other analog signal-processing circuits.
# Procedure:   
**Step 1**
DC analysis: Design RSS and Rd.  
Find the q point of the mosfet.    
Analysis :  
1)Increase ViCm to 1.2V and observe Vocm,Vp. justify the results.  
2) Calulate maximum input swing and output swing.  
3) Gain equation using small signal model.  

**Step 2**  
Transient analysis.   
Apply Vin p-p max and verify the o/p, calculate gain if the o/p is linear.  
**Step 3**  
Ac analysis.    
Find te 3dB bandwidth.  
## With Rss resistor
Dc analysis:
when ViCm = 1V
Vocm=1.1V
Vp=0.4V
Id=0.25mA  
Aspect Ratio=W/L=19.363/180n  
![Image](https://github.com/user-attachments/assets/a76109bf-f904-4dba-aabb-cbbbfa041a37)
Q point of the mosfet:(Vds,Id)@Vgs constant=(0.7V,0.25m)@Vgs=0.6V

![image](https://thub.com/user-attachments/assets/ef7ebb49-df71-4195-8d35-65dd2094e162)

## Analysis:
**a)** when ViCm is 1.2V
Vout,Vp and Id increases respectively.
Vout=0.75V
Vp=0.54V
Id=0.35mA
Vgs 0.675V

![Image](https://github.com/user-attachments/assets/fb0d9642-a89d-4298-86f0-d8f66ed2e903)
# Transient analysis
Input waveform  
![Image](https://github.com/user-attachments/assets/88e2c471-56c4-4dae-a794-b94d2a63d52b)  
Output waveform  
![Image](https://github.com/user-attachments/assets/a67b27d1-3268-47b9-b41b-7c151c0f8236)
Both Input and Output Waveform together  
![Image](https://github.com/user-attachments/assets/ab0162d8-d47f-48db-b2b9-0b197cabe643)
Thus for the given values in question the MOSFET amplifies.
## Calulation of gain(theortical)
Vin (Input Peak-to-Peak):  
Maximum voltage ≈ 1.04V
Minimum voltage ≈ 0.95V  
Vin P-P = 1.04V - 0.95V = 0.09V  
Vout (Output Peak-to-Peak)  
Maximum voltage ≈ 1.53V  
Minimum voltage ≈ 0.654V  
Vout P-P = 1.53V - 0.654V = 0.876V  
The voltage gain(Av)=Vout(p-p)/Vin(p-p)
Therefore ,the gain =9.73 V/V  
Gain in dB=20log( 9.73)
Gain in dB=19.78V/V
## Practical gain using simulation.  
Gain=19.57V/V.    
![Image](https://github.com/user-attachments/assets/0303ea29-ddc7-449e-b934-57f83dea5b19)  
There is a deviation in pratical and theortical gain, due to formation of internal parastic capacitance and resistance induced due to it.

## When the amplitude of the input wave is changed.
The gain remains same.
The amplitude is increased the sine wave is clipped off.  

![Image](https://github.com/user-attachments/assets/02cd7552-4270-4c68-8a50-7fd78ab6431e)
Both input and output graph.  
![Image](https://github.com/user-attachments/assets/ae9bd35f-ea0d-4d8d-bf8d-d3c62183ddbf)

Since the input same for both MOSFET , the graph will be also same(Transient analysis)  
Gain of this from simulation is  
![image](https://github.com/user-attachments/assets/e76d9c25-7738-40af-aa46-84f161e7f6bb)
## Now the Rss is replaced current source which is called current mirror.
As shown in the fig  b)
**DC analysis**
![Image](https://github.com/user-attachments/assets/816bcd73-d54e-4065-aebb-1e35f098e5e0)  
Same as previous.
**Transient Analysis**  
Input wave
![Image](https://github.com/user-attachments/assets/a733962e-ccd1-42e5-b77e-47fb5c4d7c23)
Output wave  


both input and output wave  












