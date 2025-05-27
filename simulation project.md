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

Input Signals:

V(IN1): +5 mV sine wave (1 kHz)

V(IN2): 1 mV sine wave (1 kHz)

NMOS Parameters:

Threshold Voltage (Vth): 0.7 V

Transconductance Parameter (Kn): 200 µA/V²

Width/Length Ratio (W/L): 10 µm / 1 µm

Operation Mode: Differential mode (inputs are out of phase)

Output Nodes:

Vout1 = Drain of M2

Vout2 = Drain of M1

This configuration ensures that differential signals are amplified while common-mode signals are rejected, leveraging the full benefits of source degeneration.</br>
**schematic view**
<br>The schematic includes two NMOS transistors configured in a differential pair. Their sources are each connected to individual source resistors (R3, R4), which then merge into a constant current source I1. Each transistor's drain is connected to a load resistor (R1, R2), which connects to VDD. Input signals are applied to the gates of M1 and M2. The outputs are taken from the drains of the transistors, where the differential voltage is developed. The source degeneration resistors are key to enhancing linearity, input impedance, and gain stability.</br>



