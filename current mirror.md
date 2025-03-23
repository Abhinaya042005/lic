
## Current Mirror

<p>A current mirror is an electronic circuit that replicates a reference current at its output, ensuring a stable and predictable current source. It typically consists of two or more matched transistors, where one transistor sets the reference current and the others mirror it. Current mirrors are widely used in analog circuits for biasing, amplification, and signal processing, offering high accuracy and stability. Variants like the Wilson and cascode current mirrors enhance performance by improving output resistance and reducing errors. Common in integrated circuits, current mirrors play a crucial role in maintaining consistent current flow in amplifiers, voltage regulators, and differential pairs.</p>

## <p>Design and analysis current mirro circuit as active load in amplifier circuit</p>

 ## circuit-1

![currentmirror11 crt](https://github.com/user-attachments/assets/5dcaece9-5c63-49f5-a654-21069524bee7)
<p>I<sub>total</sub>=(power/V<sub>dd</sub>)</p>
<p>=(1m/1.8)</p>
=0.5mA

<p>I<sub>ref</sub>=I<sub>d</sub>=(I<sub>total</sub>/2)</p>
<p>=0.5m/2</p>
=0.27mA

## DC Analysis
<p>The DC analysis of a current mirror circuit involves determining the reference current and analyzing how accurately it is mirrored at the output. In a basic BJT current mirror, the reference current is set by an external resistor and flows through a diode-connected transistor, establishing a base-emitter voltage. An identical transistor copies this current. However, practical factors like transistor mismatch, base currents, and the Early effect introduce minor deviations. Similarly, in a MOSFET current mirror, the gate-source voltage determines current mirroring, but channel length modulation can affect accuracy. Advanced designs like the Wilson and cascode current mirrors improve precision by increasing output resistance and reducing systematic errors.</p>
<p>MOSFET length - 180nm</p>
<p>width - 101um</p>
<p>V<sub>out</sub> = 1.162v </p>
<p>The above circuit is in saturation region that is V<sub>ds</sub>>V<sub>gs</sub>-V<sub>th</sub>.</p>

## Transient Analysis
<p>The transient analysis of a current mirror examines its response to time-varying signals and how quickly it stabilizes to mirror the reference current. When power is first applied, the transistors undergo a brief settling time as the base-emitter (or gate-source) voltages adjust to establish the desired current. During this phase, capacitive effects in the transistors, such as junction capacitances and stray parasitics, influence the circuit’s speed and stability. In BJTs, base charging delays can cause a short overshoot or undershoot in I<sub>out</sub>, while in MOSFETs, gate capacitance affects the transition speed. To improve transient performance, techniques like adding compensation capacitors or using active feedback circuits can help reduce settling time and enhance stability.</p>

![currentmirror11 dc](https://github.com/user-attachments/assets/9468cb07-154b-4edb-9a04-8846a2cea17b)
<p>The input voltage given is 0.5V and amplitude </p>

