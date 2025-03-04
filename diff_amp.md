 # Aim:Design and analysis of differential amplifier circuit
 <br><p>Design differential amplifier circuit for V<sub>dd</sub>=2.2v, p <= 2.2mW, V<sub>ocm</sub> = 1.25v, V<sub>p</sub> = 0.4v</p></br>
  # Abstract</br>
 <p>  we need to design a differential amplifier with specific voltage and input signal requirements. The task involves performing four key analyses: DC Analysis to determine the operating point, Transient Analysis to observe how the amplifier responds to changing signals,Frequency Response to check its performance across different frequencies, and Parameter Extraction to gather important details like gain, common-mode rejection ratio (CMRR), and impedance. The goal is to ensure the amplifier works effectively within the given specifications.</p>
 
  # Theory 
 <p>A differential amplifier is a type of electronic amplifier that amplifies the difference between two input signals. It has two inputs: a non-inverting input and an inverting input. The amplifier increases the voltage difference between these inputs while rejecting any voltage common to both, called the common-mode voltage. This makes it highly effective for applications where the signal needs to be isolated from noise or interference. Differential amplifiers are widely used in signal processing, instrumentation, and communication systems due to their ability to amplify weak signals while rejecting noise.</p>
 
 # Circuit:1
 image
 # DC analysis
 <p>The DC analysis of a differential amplifier circuit focuses on determining the biasing conditions when no input signal is applied. It ensures that the transistors operate in their active region by calculating the quiescent current and voltage across the components, such as resistors and transistors. This helps set the operating point of the amplifier, ensuring it is stable and ready to amplify signals correctly. The analysis involves calculating key values like collector currents and voltages, which ensures that the circuit is properly biased to avoid distortion or improper operation when an AC signal is later applied.</p>
 image
 <br><p>This differential amplifier circuit has two resirtor each of 1.9kohm, two voltage source of 1.2v,V<sub>dd</sub>=2.2v </p>
 <p>MOSFET length= 180nm</p>
 <p>width=0.4175um</p>
 <p>V<sub>in cm</sub>=1.2v</p>
 <p>V<sub>o cm</sub>=1.25v</p>
 
 # Transient analysis
 <p>Transient analysis of a differential amplifier circuit examines how the circuit responds to time-varying input signals over time, especially during switching events or signal changes. It simulates the amplifier's behavior when subjected to fast changes, such as signal pulses or step inputs. This analysis helps determine important characteristics like rise time, fall time, settling time, and the stability of the amplifier. By observing the transient response, it ensures the amplifier can handle real-world dynamic inputs without distortion or excessive delays.</p>
 image
 <p>Their is 180degree phase shift between input and output.</p>
 <p>A<sub>v</sub> = V<sub>out</sub>/V<sub>in</sub></p>
 <p>A<sub>v</sub> = 0.042/0.03= 1.4</p>
 <p># AC analysis</p>
 <p>The AC analysis of a differential amplifier focuses on evaluating how the circuit responds to small time-varying input signals. It involves calculating the 
 voltage gain, determining the frequency response (including bandwidth and cutoff frequencies), and analyzing the amplifier's impedance. The analysis uses small-signal models for the transistors to determine how the amplifier amplifies the input signals and behaves across different frequencies. It helps ensure the amplifier performs as desired for real-world signals, with proper gain and frequency response.</p>
 image
 <p>Gain remains constant as their is no change in R<sub>d</sub>.From the above smulation the maximum frequency range is 15.9GHz and low frequency range is 100MHz.</p>
 <p>The bandwidth of this circuit is BW = f<sub>h</sub>-f<sub>l</sub></p>
 <p>BW= 15.9GHz-100MHz = 15.96GHz</p>
 
 # Input sweep
 <p>An input sweep of a differential amplifier circuit involves varying the input voltage over a range and observing the output response. This test helps assess the amplifier’s linearity, gain, and dynamic range. By sweeping the input signal, typically from a minimum to maximum value, you can observe how the output changes, checking for issues like saturation or clipping. The input sweep is useful for evaluating the amplifier’s behavior under different input conditions, ensuring that the amplifier performs consistently within its operating range without distortion.</p>
 image

 # Circuit2
 image
 <p># DC analysis</p>
 image 
 
 
 
