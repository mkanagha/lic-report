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
Circuit Description The MOSFET differential amplifier consists of:

Two identical NMOS transistors operating in the saturation region. A current source that provides a constant biasing current (Id). Load resistors (Rd) or active loads (current source/NMOS current mirror). The output signals (Vout1 and Vout2) are taken from the drain terminals of the MOSFETs.

**Circuit Configurations Explored:**

Circuit 1: Uses a resistor Rd as the load.
Circuit 2: Replaces Rd with a current source, ensuring more stable operation.
Circuit 3: Uses an NMOS transistor as a current source, improving integration in IC design.\

Operating Principle
A. Biasing and Q-Point Setting
The Q-point (operating point) is set to ensure the transistors work in saturation mode, where: [ ID =(1/2) un Cox (W/{L) (VGS - Vth)^2 ] By adjusting W/L ratio and Rd, we achieve the desired current (Id1 = Id2 = 0.25mA) and voltage (Vds = 0.7V).\
B. Small-Signal Analysis and Gain Calculation The small-signal voltage gain is given by:
Av = -gmRD
where 𝑔m (transconductance) is:
gm = 2ID/(Vgs - Vth)
For Circuit 1 (resistor load), gain depends on Rd.
For Circuit 2 & 3 (current source/NMOS mirror), the gain is higher because the effective resistance is larger than a passive resistor.
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
![Image](https://github.com/user-attachments/assets/db6eff39-b593-48ef-9578-05ac28579cbc)
both input and output wave  
![Image](https://github.com/user-attachments/assets/749b7102-763e-428d-b648-97a903836f25)
The MOSFET is amplifing at this point.
**Ac analysis**
Gain will be same   
![Image](https://github.com/user-attachments/assets/2a1b7db8-cd5a-4ed1-90ae-e67eadf59151)  
## Now the current mirror is replaced by MOSFET with same current flowing through it.
As shown in fig  c)
**DC analysis**
![Image](https://github.com/user-attachments/assets/ab66536e-2c37-4a67-9165-16c27e425c8a)
**Transient Analysis**
Input wave
![Image](https://github.com/user-attachments/assets/37925b8a-49c1-4ce8-b0f2-6540ce24bbda)  
Output wave  
![Image](https://github.com/user-attachments/assets/5a35f557-628d-4515-a6a1-d21684d6e9ce)
Both input and output  
![Image](https://github.com/user-attachments/assets/6124d247-24ff-4a8a-873d-6e06af90e7aa)
**Ac analysis**
![Image](https://github.com/user-attachments/assets/56fb8a47-d510-4751-843b-cbfa526a3f87)
# INFERENCE
From the analysis of the MOS differential amplifier under three different configurations—using a resistor (Rss), a current mirror, and an NMOSFET as a current source—the following conclusions can be drawn:

**DC Analysis**:
1)The quiescent operating points (Q-points) of the MOSFETs were successfully established, ensuring stable biasing conditions in all configurations.  
2)When ViCm was increased from 1V to 1.2V, the output voltage (Vout), peak voltage (Vp), and drain current (Id) increased, confirming the expected behavior of the amplifier.  
3)The current mirror and NMOS current source provided better bias stability than the simple resistor (Rss), reducing variations in drain current and improving overall circuit consistency.  
**Transient Analysis:**  
1)The MOSFET successfully amplified the input sine wave in all configurations, confirming proper operation.  
2)Increasing the input amplitude led to output waveform clipping, indicating the limits of the amplifier’s linear operation.
3)The symmetry of the waveform in transient plots suggests that all configurations maintained balanced differential operation.  
**AC Analysis & Gain Comparison:**  
1)The gain remained the same across all three configurations within expected tolerances.  
2)The theoretical gain (9.73 V/V or 19.78 dB) closely matched the practical gain (19.57 dB) observed in simulations, with only slight deviations due to parasitic effects.  
3)While the gain did not change across configurations, the stability of the gain improved when using a current mirror and NMOS current source, as they provided a more stable tail current and reduced common-mode variations.  
**Bandwidth & Linearity:**  
The 3dB bandwidth analysis confirmed effective amplifier operation across a specified frequency range.  
The gain remained consistent across different input amplitudes until reaching the clipping threshold, highlighting the need to keep input signals within an appropriate range.   
## Conclusion:  
1)The MOS differential amplifier functioned effectively across all configurations, demonstrating stable DC biasing, transient response, and AC performance.  
2)While the gain remained the same for all three circuits, bias stability improved when using a current mirror or NMOS current source instead of Rss.  
3)The NMOS current source provided the most stable biasing, ensuring consistent operation and minimizing variations due to external factors.  
4)Parasitic effects and waveform clipping were observed, reinforcing the importance of careful design in practical implementations.  
Overall, the experiment validated the theoretical principles of differential amplification, confirming that different biasing techniques impact circuit stability rather than gain.  







