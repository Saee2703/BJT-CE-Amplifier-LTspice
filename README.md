# BJT-CE-Amplifier-LTspice
BJT Common Emitter Amplifier — LTspice Simulation

A BC847B NPN transistor configured as a common emitter amplifier with a voltage divider biasing network — designed, biased, and verified entirely in LTspice XVII using transient analysis.
This simulation demonstrates fundamental analogue amplifier design — calculating the DC operating point, establishing a stable Q-point through voltage divider biasing, and verifying AC signal amplification through transient analysis.

Circuit Specifications
 Component   Value           Purpose
* Q1          BC847B          NPN Amplifying transistor
* V2          12V             DCSupply voltage
* R3          10.67KΩ         Upper voltage divider bias
* R4          11.18KΩ         Lower voltage divider bias
* R1          1KΩ             Collector resistor
* R2          1.18KΩ          Emitter resistor
* C3          47µF            Emitter bypass capacitor
* C2          10µF            Input coupling capacitor
* C1          10µF            Output coupling capacitor
* R5          10KΩ            Load resistor
* V1          SINE(0 10m 1K)  10mV peak 1KHz input signal

Simulation Command : .tran 10m

Results: 
  Measurement     Value
* Input voltage   V(vin)10mV peak
* Output voltage  V(vout)~1.2V peak
* Voltage         gain~120x
* Phase           shift180° — confirmed CE configuration
* Signal quality  Clean sinusoidal — no clipping
* Frequency       1KHz
  
Key Observations

* Voltage gain of approximately 120x confirmed — 10mV input amplified to 1.2V output
* 180 degree phase inversion visible — characteristic of common emitter configuration
* Voltage divider bias network provides stable Q-point — no signal clipping observed
* Emitter bypass capacitor C3 increases AC gain by bypassing emitter resistor
* Input and output coupling capacitors block DC while passing AC signal

Tools: LTspice XVII


<img width="1600" height="850" alt="Image" src="https://github.com/user-attachments/assets/1a47e899-46ab-47c5-ba81-8df74c957534" />
