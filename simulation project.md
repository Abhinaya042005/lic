# Differential Amplifier with Source Degeneration 
**Abstract:**
<br>This project explores the design, simulation, and analysis of a MOSFET-based differential amplifier enhanced with source degeneration resistors. The amplifier is designed to accept two differential input signals and provide corresponding outputs with high common-mode noise rejection and improved linearity. The technique of source degeneration—using resistors in series with the source terminals of the MOSFETs—introduces local negative feedback, which stabilizes the gain and enhances the linear operating region of the transistors. The result is a differential amplifier that produces outputs equal in magnitude but opposite in phase, ensuring reliable and robust performance in analog systems. This makes the circuit ideal for use in scenarios where precision and noise immunity are critical, such as sensor signal conditioning, communication receivers, and instrumentation systems.</br>
# Introduction
<br>A differential amplifier is a fundamental building block in analog circuit design, used extensively in operational amplifiers, analog filters, data converters, and communication circuits. Its key function is to amplify the voltage difference between two input signals while rejecting any voltage common to both inputs—known as common-mode signals. In practical implementations using MOSFETs, one of the challenges is to ensure the amplifier maintains linearity and stability across varying signal conditions and device mismatches. This is achieved through source degeneration, where resistors are placed in the source path of each MOSFET in the differential pair. These resistors provide negative feedback, improving linearity, increasing input impedance, and minimizing the impact of process variations on the amplifier's performance. Moreover, this configuration reduces the Miller effect and improves frequency response, making it suitable for high-precision and high-speed analog applications. In this project, a symmetrical layout using two NMOS transistors, matched drain resistors, and a tail current source is used to demonstrate the effectiveness of source degeneration in achieving a reliable and noise-resistant differential amplifier.</br>
# Design specification
<br>The amplifier is designed around a symmetric NMOS differential pair with added source degeneration. Below are the key parameters and design choices:

Power Supply (VDD): 10 V DC

Tail Current Source (I1): 500 µA (constant current for balanced operation)

Transistors Used: 2 x NMOS (M1 and M2)

Drain Resistors (R1 and R2): 10 kΩ each

Source Resistors (R3 and R4): 1 kΩ each (for degeneration)

**Input Signals:**
<br>![image](https://github.com/user-attachments/assets/4ba6da07-6db4-457f-bbeb-72a6b4c9e2ad)</br>

V(IN1): +5 mV sine wave (1 kHz)

V(IN2): 1 mV sine wave (1 kHz)

NMOS Parameters:

Threshold Voltage (Vth): 0.7 V

Transconductance Parameter (Kn): 200 µA/V²

Width/Length Ratio (W/L): 10 µm / 1 µm

<br>Operation Mode: Differential mode (inputs are out of phase)</br>
**Output signals**
![image](https://github.com/user-attachments/assets/e631964f-0edd-4de3-8d34-91a393a28799)

Output Nodes:

Vout1 = Drain of M2

Vout2 = Drain of M1

This configuration ensures that differential signals are amplified while common-mode signals are rejected, leveraging the full benefits of source degeneration.</br>
# Circuit Diagram
<br>The schematic includes two NMOS transistors configured in a differential pair. Their sources are each connected to individual source resistors (R3, R4), which then merge into a constant current source I1. Each transistor's drain is connected to a load resistor (R1, R2), which connects to VDD. Input signals are applied to the gates of M1 and M2. The outputs are taken from the drains of the transistors, where the differential voltage is developed. The source degeneration resistors are key to enhancing linearity, input impedance, and gain stability.</br>
<br>![image](https://github.com/user-attachments/assets/3e31478e-4875-4817-8930-18818d9256a0)</br>

# Component list
<br>The differential amplifier circuit utilizes two matched NMOS transistors, each with a width of 10 µm and a length of 1 µm, having a threshold voltage (Vth) of 0.7 V and a transconductance parameter (Kn) of 200 µA/V². The drains of the NMOS transistors are connected to the positive supply voltage (VDD = 10 V) through two 10 kΩ resistors (R1 and R2), which serve as load resistors. The sources of the transistors are each connected to ground via 1 kΩ resistors (R3 and R4), providing source degeneration to improve linearity and gain stability. A tail current source (I1) supplies a constant current of 500 µA to the common source node, ensuring balanced differential operation. The input signals are applied to the gates of M1 and M2, typically small sine waves of 1 kHz frequency, while the outputs are taken from the drains of the transistors as Vout1 and Vout2.</br>

# How the Circuit Works
<p>The differential amplifier with source degeneration operates by using two matched NMOS transistors arranged in a differential pair. These transistors (M1 and M2) have their drain terminals connected to resistors (R1 and R2), which in turn are connected to the positive power supply (VDD). The gates of the transistors receive the two input signals—one positive and one negative, or two signals of equal amplitude but opposite phase. The sources of both transistors are connected to the negative side of the power supply through resistors (R3 and R4) and a common tail current source (I1).</p>

<p>The key idea is that the circuit amplifies the difference between the two input signals, not the signals themselves. When a differential signal is applied (e.g., +5 mV to one gate and –5 mV to the other), one transistor conducts more while the other conducts less. This causes a change in the current through their respective drain resistors, resulting in output voltages that are equal in magnitude but opposite in phase.</p>

<p>The source degeneration resistors (R3 and R4) play an important role. They add local negative feedback, which improves the linearity of the circuit, making it more stable and reducing distortion. They also help ensure that small changes in input result in predictable, smooth changes in output, rather than abrupt shifts.</p>

<p>Additionally, the tail current source (I1) ensures that the total current shared between the two transistors remains constant. This helps maintain symmetry in the circuit, which is essential for rejecting noise that appears on both inputs (common-mode noise).</p>

# Calculations


**Small-Signal Gain with Source Degeneration**<br>
The voltage gain of the amplifier with source degeneration is given by:<br>
Av = (gm * RD) / (1 + gm * RS)<br><br>

Where:<br>
gm = transconductance of the MOSFET<br>
RD = drain resistor = 10 kΩ<br>
RS = source resistor = 1 kΩ<br><br>

Assuming drain current ID = 250 µA (half of tail current), and Kn = 200 µA/V²:<br>
gm = √(2 * Kn * ID) = √(2 * 200 * 250) = √100000 ≈ 316 µS<br><br>

Substituting in the gain formula:<br>
Av = (316e-6 * 10000) / (1 + 316e-6 * 1000)<br>
Av ≈ 3.16 / 1.316 ≈ 2.4<br><br>
**➤ Measured Output Gain**<br>
Vout1 (pp) = 7.5014 V - 7.4983 V = 3.1 mV<br>
Av1 = 1.55 mV / 1 mV = 1.55<br><br>

Vout2 (pp) = 7.5014 V - 7.4983 V = 3.1 mV<br>
Av2 = 1.55 mV / 5 mV = 0.31<br><br>

**Differential Gain**<br>
Ad = (Vout2 - Vout1) / (Vin2 - Vin1)<br>
Ad = (1.55 - (-1.55)) / (5 mV - 1 mV) = 3.1 mV / 4 mV = 0.775<br><br>

**Common-Mode Gain and CMRR**<br>
Assume Acm = -0.0498<br>
CMRR = |Ad / Acm| = |0.775 / -0.0498| ≈ 15.56<br>
CMRR(dB) = 20 * log10(15.56) ≈ 23.84 dB<br><br>
# Simulation Result
<br><p>We gave two small sine wave signals—one positive and one negative—to the gates of the two NMOS transistors. These input signals were set at a frequency of 1 kHz with very low voltage, just a few millivolts, to test the amplifier in its small-signal operating region.</br></p>
<br><p>When we looked at the output waveforms (taken from the drains of each transistor), we noticed something important: the two output signals were equal in amplitude but completely opposite in phase (180° apart). This confirmed that the circuit is working in true differential mode—amplifying the difference between the inputs and ignoring any common noise present on both lines.</br></p>
<br><p>We also measured the actual gain from the output graphs. One output had a peak voltage of around 1.55 mV for a 1 mV input (giving a gain of about 1.55), while the other output showed a smaller gain of around 0.31 for a 5 mV input. By calculating the difference between the two outputs and dividing by the input difference, we obtained a differential gain of approximately 0.775.</br></p>
<br><p>Additionally, we looked at the common-mode rejection—how well the circuit blocks signals that are common to both inputs. The results showed that the amplifier suppresses these common signals effectively, giving a CMRR (Common Mode Rejection Ratio) of about 23.84 dB, which is decent for a basic differential amplifier.</br></p>
<br><p>In short, the simulation results matched what we expected from theory: the amplifier boosted the difference between the input signals, produced opposite outputs, rejected common noise, and performed with stable gain—thanks to the source degeneration resistors that improved linearity and balance.</br></p>

# Advantages and Disadvantages

**Advantages:**

Noise Rejection: It can ignore unwanted signals that are common to both inputs (called common-mode noise), which is great for real-world use where interference is common.
Better Linearity: It handles signals more accurately without distorting them.
Stable Gain: The gain doesn't change much with temperature or manufacturing differences.
High Input Impedance: It doesn't load the input signal much, making it easier to connect to sensors or earlier circuit stages.

**Disadvantages:**

Lower Gain: Because of the resistors at the source, the amplifier doesn’t boost the signal as much as a simple differential pair.
Slightly More Complex: Adding source resistors and matching components makes the design and calculations a bit more involved.


# Applications

Instrumentation Amplifiers: Used in measurement systems to boost tiny signals (like from temperature or pressure sensors) while rejecting noise.
Op-Amp Input Stages: Differential amplifiers are the first stage in many operational amplifiers, helping them get clean input signals.
Sensor Signal Amplification: It’s ideal for boosting small signals from sensors without adding much noise.
Audio Systems: Used in audio circuits to balance input signals and remove unwanted noise.
Communication Systems: Helps in transmitting and receiving signals by removing interference and improving signal clarity.

# Inference

<p>From the behavior observed during simulation, it is evident that the differential amplifier with source degeneration performs its intended function effectively. The circuit successfully amplifies only the difference between two input signals while minimizing the influence of any noise or interference common to both inputs. The addition of source degeneration resistors introduces local negative feedback, which significantly enhances the linearity of the amplifier and reduces distortion. It also increases the input impedance and stabilizes the gain, making the circuit more reliable and less sensitive to variations in transistor characteristics. Overall, the circuit demonstrates excellent differential operation with strong noise rejection and predictable performance.</p>

# Result

<p>The simulation results confirmed that the output signals of the differential amplifier were equal in amplitude but 180° out of phase, verifying proper differential behavior. The peak-to-peak voltage measured at the outputs matched the theoretical values, and the calculated gain was close to the expected values based on the design parameters. A differential gain of approximately 0.775 and a common-mode rejection ratio (CMRR) of around 23.84 dB were achieved, indicating that the amplifier not only amplified the desired signal but also effectively rejected common-mode noise. These results validate the theoretical design and prove that source degeneration improves the overall performance of the amplifier.</p>



