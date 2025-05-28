# Monostable multivibrator using 555 timer IC 
 ## AIM:
 Generating the waveform with Pulse width Modulation of 0.5ms using 555IC
## THEORY:
A monostable multivibrator is a circuit that, when triggered externally, produces a single output pulse of a fixed duration. The 555 timer IC is a versatile and widely used component in timer, delay, and oscillator applications. In monostable mode, the timer remains in a stable low state until an external trigger causes it to switch to the high state for a specific time determined by external resistor (R) and capacitor (C) values.
The output pulse width 𝑇
T is given by the formula:
T=1.1×R×C
This setup is particularly useful for creating time delays, pulse stretching, and waveform shaping.
The 555 timer integrated circuit (IC) is one of the most popular and versatile components used in analog electronics. It was introduced by Signetics in 1972 and has since found widespread applications in timers, oscillators, pulse generation, and waveform shaping circuits. The 555 timer can operate primarily in three modes: astable, monostable, and bistable. In this project, we focus on the astable and monostable modes to generate precise pulse waveforms and control pulse widths for applications such as pulse width modulation (PWM), timing delays, and triggering circuits.

The objective of this project is to design and simulate two experimental setups using the 555 timer IC in LTspice simulation software.

The first setup is an astable multivibrator generating a PWM waveform with a fixed pulse width of approximately 0.5 milliseconds.
The second setup is a monostable multivibrator triggered by the output of the astable circuit after passing through a differentiator and clipper stage. The monostable circuit produces a single output pulse whose width can be varied externally by changing component values.
By simulating these circuits, we aim to understand the working principles of the 555 timer in generating and controlling pulse signals and to explore the practical aspects of triggering monostable pulses from an astable source.

## CIRCUIT DIAGRAM:
Internal ckt of 555 IC.
![image](https://github.com/user-attachments/assets/913086fc-1b63-4a11-b35c-ad68983efe2f)
Pin configuration of 555 IC 
![image](https://github.com/user-attachments/assets/0395c7a1-f34a-470d-a5fd-e76631325fd4)
## METHOLOGY 
1. Astable Multivibrator Stage
Configuration: 555 timer in astable mode.
Function: Generates a continuous square wave (PWM) with a pulse width of ~0.5 ms.
Design Equation:
![image](https://github.com/user-attachments/assets/afad82cf-9a41-404f-8951-759b47e5ce6f)
Output: Used as input to the differentiator stage.
2. Differentiator Circuit
Configuration: RC High-Pass Filter.
Function: Converts the square wave into sharp spikes (positive and negative).
Design: A small capacitor in series with a resistor to ground.
3. Clipper Circuit
Configuration: Diode and Zener diode based.
Function: Clamps the differentiated spike to a safe level to ensure proper triggering of the monostable timer.
Output: Single negative-going pulse used to trigger monostable stage.
4. Monostable Multivibrator Stage
Configuration: 555 timer in monostable mode.
Function: Generates a single output pulse on each trigger.
Design Equation:
T=1.1×R×C
Adjustability: Pulse width is varied by changing the external R or C.
## simulattion results:
   INPUT WAVE @ trigger pin  
![image](https://github.com/user-attachments/assets/c809e1dc-4dc0-4a67-aee7-5ff40c20b56a)  
output wave @ output pin and @ capcitor pin between threshold and discharge    
![image](https://github.com/user-attachments/assets/796c481a-4eae-4086-aa29-6c6d9d6d34ec)    
## Astable multivibrator and monostable multivibrator using 555 timer IC  
# Circuit Diagram  
Internal ckt  
![image](https://github.com/user-attachments/assets/5b5b7ea8-ee50-4074-a082-98a4dab85cab)  
# Procedure  
Build the circuit as per the Circuit diagram.  
Calculate the resistor R and capacitor C for Astable multivibrator Differentiator, clipper and Monostable multivibrator.  
Analyze the capacitor charging and discharging Voltage per time.  
Analyze the ton period when input is triggered.  
# LT spice ckt diagram  
![image](https://github.com/user-attachments/assets/dc901f92-0b3c-4529-bcc5-d62d30873ae4)  
## result 
**case**   
V1 is Output of the Astable Multivibrator, V2 is Capacitor Voltage of Astable Multivibrator, V3 is Output of Differentiator, V4 is Capacitor Voltage of Monostable Multivibrator, Vout is Output of Monostable Multivibrator pulse width is 0.5ms

![image](https://github.com/user-attachments/assets/85cb6c32-7a69-49a5-99b6-f2844ec14a54)  







## Conclusion
The simulation successfully demonstrates the pulse shaping and timing functionalities using 555 timers in astable and monostable configurations. The combination of differentiator and clipper stages provides a clean trigger signal, and the monostable timer reliably generates output pulses of fixed duration. The circuit is versatile and can be extended for timing, pulse generation, or digital interfacing applications.
