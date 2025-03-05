 # Aim:Design and analysis of differential amplifier circuit
 <br><p>Design differential amplifier circuit for V<sub>dd</sub>=2.2v, p <= 2.2mW, V<sub>ocm</sub> = 1.25v, V<sub>p</sub> = 0.4v</p></br>
  # Abstract</br>
 <p>  we need to design a differential amplifier with specific voltage and input signal requirements. The task involves performing four key analyses: DC Analysis to determine the operating point, Transient Analysis to observe how the amplifier responds to changing signals,Frequency Response to check its performance across different frequencies, and Parameter Extraction to gather important details like gain, common-mode rejection ratio (CMRR), and impedance. The goal is to ensure the amplifier works effectively within the given specifications.</p>
 
  # Theory 
 <p>A differential amplifier is a type of electronic amplifier that amplifies the difference between two input signals. It has two inputs: a non-inverting input and an inverting input. The amplifier increases the voltage difference between these inputs while rejecting any voltage common to both, called the common-mode voltage. This makes it highly effective for applications where the signal needs to be isolated from noise or interference. Differential amplifiers are widely used in signal processing, instrumentation, and communication systems due to their ability to amplify weak signals while rejecting noise.</p>
 
 # Circuit:1
 ![Image](https://github.com/user-attachments/assets/90d7ae6a-ae1f-4d14-be85-82091d06334a)
 # DC analysis
 <p>The DC analysis of a differential amplifier circuit focuses on determining the biasing conditions when no input signal is applied. It ensures that the transistors operate in their active region by calculating the quiescent current and voltage across the components, such as resistors and transistors. This helps set the operating point of the amplifier, ensuring it is stable and ready to amplify signals correctly. The analysis involves calculating key values like collector currents and voltages, which ensures that the circuit is properly biased to avoid distortion or improper operation when an AC signal is later applied.</p>

 ![Image](https://github.com/user-attachments/assets/23217ced-a48d-47aa-8fa9-80eb82d68d44)
 <br><p>This differential amplifier circuit has two resirtor each of 1.9kohm, two voltage source of 1.2v,V<sub>dd</sub>=2.2v </p>
 <p>MOSFET length= 180nm</p>
 <p>width=0.4175um</p>
 <p>V<sub>in cm</sub>=1.2v</p>
 <p>V<sub>o cm</sub>=1.25v</p>
 <p>from the above simulation operating point is (V<sub>out</sub>, i<sub>d</sub>) = (1.25v, 0.5mA).</p></p>
 
 # Transient analysis
 <p>Transient analysis of a differential amplifier circuit examines how the circuit responds to time-varying input signals over time, especially during switching events or signal changes. It simulates the amplifier's behavior when subjected to fast changes, such as signal pulses or step inputs. This analysis helps determine important characteristics like rise time, fall time, settling time, and the stability of the amplifier. By observing the transient response, it ensures the amplifier can handle real-world dynamic inputs without distortion or excessive delays.</p>

![Image](https://github.com/user-attachments/assets/8f0a89c7-c187-440d-9da9-1efea338e3a9)
 <p>Their is 180degree phase shift between input and output.</p>
 <p>A<sub>v</sub> = V<sub>out</sub>/V<sub>in</sub></p>
 <p>A<sub>v</sub> = 0.042/0.03= 1.4</p>
 
 # AC analysis
 <p>The AC analysis of a differential amplifier focuses on evaluating how the circuit responds to small time-varying input signals. It involves calculating the 
 voltage gain, determining the frequency response (including bandwidth and cutoff frequencies), and analyzing the amplifier's impedance. The analysis uses small-signal models for the transistors to determine how the amplifier amplifies the input signals and behaves across different frequencies. It helps ensure the amplifier performs as desired for real-world signals, with proper gain and frequency response.</p>
 
 ![Image](https://github.com/user-attachments/assets/03fe020a-9cb1-4d91-9b14-ed086cf61785)
  <p>Gain remains constant as their is no change in R<sub>d</sub>.From the above smulation the maximum frequency range is 15.9GHz and low frequency range is 100MHz.</p>
 <p>The bandwidth of this circuit is BW = f<sub>h</sub>-f<sub>l</sub></p>
 <p>BW= 15.9GHz-100MHz = 15.96GHz</p>
 
 # Input swing
 <p>An input sweep of a differential amplifier circuit involves varying the input voltage over a range and observing the output response. This test helps assess the amplifier’s linearity, gain, and dynamic range. By sweeping the input signal, typically from a minimum to maximum value, you can observe how the output changes, checking for issues like saturation or clipping. The input sweep is useful for evaluating the amplifier’s behavior under different input conditions, ensuring that the amplifier performs consistently within its operating range without distortion.</p>

![Image](https://github.com/user-attachments/assets/97f182ea-a694-4dc6-a79b-3e2cfe8a554a)
<p>The DC offset here is done by taking the average of V<sub>in min</sub> and V<sub>in max</sub></p>
<p>V<sub>in min</sub>=V<sub>t N</sub> + V<sub>p</sub></p>
<p>V<sub>in max</sub>=V<sub>dd</sub>-R<sub>d</sub>I<sub>ss</sub>/2 = V<sub>t</sub></p>

# Circuit2
 ![Image](https://github.com/user-attachments/assets/ffb73f83-5029-4326-b690-51f91a135ba4)
 
 # DC analysis
 ![Image](https://github.com/user-attachments/assets/fea17265-17bb-41bc-b47b-ea41968a2da1)
 <p>In this circuit we have replaced the R3 resistor o a current source.Also it has two resistor of 1.8955kohm each, two voltage source of 1.2v,V<sub>dd</sub>=2.2v,current source of 1mA.</p>
 <p>I<sub>1</sub>=P/V<sub>dd</sub> = 2.2mW / 2.2v = 1mA</p>
 <p>current source is replaced of value 1mA</p>
 <p>MOSFET length = 180nm</p>
 <p>width = 6.2um</p>
 <p>V<sub>in cm</sub>=1.2v</p>
 <p>V<sub>o cm</sub>=1.252v</p>
 <p>from the above simulation the operating point is (V<sub>out</sub>, i<sub>d</sub>)= (1.252v, 0.5mA) </p>

 # Transient analysis
 <p>V<sub>in</sub>:</p>
 ![Image](https://github.com/user-attachments/assets/6462f6f1-a12a-4b6c-92d9-c62909f9d00d)
 <p>V<sub>out</sub>:</p>
 ![Image](https://github.com/user-attachments/assets/6c7a6dd9-b644-42b8-bcdb-e0947bd38a8a)
 <p>V<sub>in out</sub>:</p>
 ![Image](https://github.com/user-attachments/assets/00710043-63e0-495b-a862-598f54bf35c8)
 <p>from the above simulation the gain of the circuit is A<sub>v</sub>=V<sub>out</sub>/V<sub>in</sub></p>
 <p>V<sub>out</sub> = 1.267-1.225 = 0.042V</p>
 <p>V<sub>in</sub> = 1.21-1.18 = 0.03V</p>
 <p>A<sub>v</sub>=0.073/0.029 = 2.5V/V</p>
 
 # AC analysis
 <p>The dc offset is 1.2v , amplitude is 15m and frequency 1KHz.</p>
 
 ![Image](https://github.com/user-attachments/assets/04c4a1c5-a1e8-4c38-9230-0250bc1b2f11)
 <p>The high frequency range is 296.93GHz and low frequency range is 100MHz</p>
 <p>the bandwidth of the simulation is calculated by f<sub>h</sub> - f<sub>l</sub></p>
 <p> BW = 296.93GHz-100MHz = 296.8GHz</p>

  # Input swing
  <p>The dc offset voltage should be changed to avg V<sub>in</sub>.The amplitude is kept at 850m and frequency at 1k.</p>
 
  ![Image](https://github.com/user-attachments/assets/b1a15040-7634-4e90-bb3e-477975d02b92)
 
  # circuit 3
  ![Image](https://github.com/user-attachments/assets/ce3ef149-0844-41ad-a564-420df73556af)
  <p>For this circuit we have replaced the 1mA current to nMOS and added voltage source of 0.76v.</p>

  # DC Analysis
  ![Image](https://github.com/user-attachments/assets/44faef9d-3e33-4fd6-8221-1c87622a0fc6)
  <p>MOSFET length = 180nm</p>
  <p>width=  </p>
  <p>V1 = 0.76v</p>
  <p>V<sub>o cm</sub> =1.250v</p>
  <p>from the simulation the operating point is (1.250v, 0.5mA).</p>

  # Transient analysis
  <p>V<sub>in</sub>:</p>
  ![Image](https://github.com/user-attachments/assets/478da79b-0ba3-481c-95ad-56f88522322b)
  <p>V<sub>out</sub>:</p>
  ![Image](https://github.com/user-attachments/assets/a206938c-90cc-403a-b3f1-0a66b5431693)
  <p>V<sub>in out</sub>:</p>
  ![Image](https://github.com/user-attachments/assets/a32ceda6-5602-4e74-9873-99c02480c4c8)
  <p>from this simulation the we can calculate by</p>
  <p>V<sub>out</sub> = 1.254-1.246 = 8mV</p>
  <p>also let V<sub>in</sub> be 1.214-1.185 = 0.029V</p>
  <p>gain for this mosfet replaced circuit is =8mA/0.029v = 0.275V/V.</p>

   # AC analysis
   ![Image](https://github.com/user-attachments/assets/ebb2ed2c-2504-491a-ba41-52eccef7b1e4)
   <p>In this circuit for 1.2v dc offset voltage, amplitude as 15m and 1KHz frequency.</p>
   image

   # Input swing
   ![Image](https://github.com/user-attachments/assets/5119b871-f280-4e6b-966b-beba47f8eb6e)
   <p>for this circuit the output waveform is flipped</p>

   # Result:
  <p>In this experiment, we analyze the performance of a differential amplifier across three distinct circuit configurations:</p>
  <p>Circuit 1: Differential Amplifier with Resistor R<sub>ss</sub></p>
  <p>In this configuration, a resistor R<sub>ss</sub> is used to establish the emitter bias current for the differential amplifier. The bias current is determined 
  by the voltage across R<sub>ss</sub> and its resistance value. However, this approach has limitations:</p>
 <p>Bias Stability: The emitter current is sensitive to variations in power supply voltage and transistor parameters, leading to potential shifts in the operating 
 point.</p>
 
 <p>Circuit 2: Differential Amplifier with Ideal Current Source</p>
 <p>Here, the resistor R<sub>ss</sub>is replaced by an ideal current source that provides a constant 1 mA bias current. This modification offers significant 
 improvements:</p>
 <p>Bias Stability: The ideal current source maintains a steady bias current, ensuring a stable operating point regardless of power supply fluctuations or transistor
 variations.</p>

<p>Circuit 3: Differential Amplifier with NMOS Transistor as Current Source</p>
<p>In this configuration,R<sub>ss</sub> is replaced by an NMOS transistor acting as a current source, with its gate voltage V<sub>b</sub> set to 0.76 V. This 
 setup offers a practical approach to implementing a current source:</p>
<p>Bias Stability: The NMOS transistor provides a relatively constant bias current. However, the actual current may vary due to transistor parameter variations 
 and temperature changes.</p>

# Inference
<p>In the comparative analysis of the three differential amplifier circuits, the choice of tail current implementation significantly influences performance. The first circuit, utilizing a resistor R<sub>ss</sub>, exhibits sensitivity to power supply variations and transistor mismatches, leading to potential instability in the bias current and reduced common-mode rejection ratio. This is due to the resistor's limited ability to maintain a constant current under varying conditions. In contrast, the second circuit employs an ideal current source, ensuring a stable bias current that is largely unaffected by external fluctuations, thereby enhancing both stability and CMRR. The third circuit replaces R<sub>ss</sub> with an NMOS transistor configured as a current source with a gate voltage V<sub>b</sub></sub> of 0.76 V. This active current source provides improved performance over the resistor by offering higher output impedance, which contributes to better bias stability and CMRR. However, it may still be susceptible to variations due to transistor parameters and temperature changes. Overall, transitioning from a passive resistor to active current sources in differential amplifier designs leads to enhanced performance, with ideal current sources offering the most significant improvements. </p>





 
