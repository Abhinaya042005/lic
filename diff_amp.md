 # Aim:Design and analysis of differential amplifier circuit
 <br><p>Design differential amplifier circuit for V<sub>dd</sub>=2.2v, p <= 2.2mW, V<sub>ocm</sub> = 1.25v, V<sub>p</sub> = 0.4v</p></br>
 <br> # Abstract</br>
 <p>  we need to design a differential amplifier with specific voltage and input signal requirements. The task involves performing four key analyses: DC Analysis to determine the operating point, Transient Analysis to observe how the amplifier responds to changing signals,Frequency Response to check its performance across different frequencies, and Parameter Extraction to gather important details like gain, common-mode rejection ratio (CMRR), and impedance. The goal is to ensure the amplifier works effectively within the given specifications.</p>
 <br> # Theory 
 <p>A differential amplifier is a type of electronic amplifier that amplifies the difference between two input signals. It has two inputs: a non-inverting input and an inverting input. The amplifier increases the voltage difference between these inputs while rejecting any voltage common to both, called the common-mode voltage. This makes it highly effective for applications where the signal needs to be isolated from noise or interference. Differential amplifiers are widely used in signal processing, instrumentation, and communication systems due to their ability to amplify weak signals while rejecting noise.</p>
 # Circuit:1
 <p>DC analysis</p>
 <p>The DC analysis of a differential amplifier circuit focuses on determining the biasing conditions when no input signal is applied. It ensures that the transistors operate in their active region by calculating the quiescent current and voltage across the components, such as resistors and transistors. This helps set the operating point of the amplifier, ensuring it is stable and ready to amplify signals correctly. The analysis involves calculating key values like collector currents and voltages, which ensures that the circuit is properly biased to avoid distortion or improper operation when an AC signal is later applied.</p>
 image
 <br><p>This differential amplifier circuit has two resirtor each of 1.9kohm, two voltage source of 1.2v,V<sub>dd</sub>=2.2v </p>
 <p>MOSFET length= 180nm</p>
 <p>width=0.4175um</p>
 <p>V<sub>in cm</sub>=1.2v</p>
 <p>V<sub>o cm</sub>=1.25v</p>
 <p># AC analysis</p>
 <p>The AC analysis of a differential amplifier focuses on evaluating how the circuit responds to small time-varying input signals. It involves calculating the **voltage gain**, determining the frequency response (including bandwidth and cutoff frequencies), and analyzing the amplifier's impedance. The analysis uses small-signal models for the transistors to determine how the amplifier amplifies the input signals and behaves across different frequencies. It helps ensure the amplifier performs as desired for real-world signals, with proper gain and frequency response.</p>
 image
 
 
 
