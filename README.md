**Experiment**<br> Common source amplifier analysis</br>
<br>This experiment is done to show the AC,DC,Transient analysis of common source amplifier</br>
<br><p>A common source amplifier is one of the most fundamental amplifier configuration.In common source amplifier configuration using MOSFET the source terminal is common to both input and output.</p><br/>
![Image](https://github.com/user-attachments/assets/275fcbf0-86b9-4b9f-bd4c-49fa6eaffd4d)
<br>**Component Details**</br>
<br>This circuit consist of CMOSN (NMOS transistor) tsmc , resistor across drain and two voltage source each connect to R<sub>d</sub> and gate terminal.</br>
<br>MOSFET length - 180nm</br>
<br>MOSFET width - 0.315um</br>
<br>supply voltage - 1.8v</br>
<br>Resistor - 1k</br>
<br>**DC Analysis**</br>
<br>To determine the operating point.</br>
<br>![Image](https://github.com/user-attachments/assets/546797b1-7747-4b34-9e46-71ef578c3cce)</br>
<br>From the simulation V<sub>out</sub> = 1.744v, V<sub>in</sub> = 0.9v , I<sub>d</sub> = 5.5A</br>
<br>If power dissipation is 100uW across R<sub>d</sub> then the current through resistor is 5.5uA.</br> 
<br>The output load line is given by the equation V<sub>out</sub> = V<sub>dd</sub>-(I<sub>d</sub>*R<sub>d</sub>)</br>
<br>As the calculated current does not match the the simulated value ,maintain the MOSFET length at 180nm by adjusting width to desired current value.</br> 
<table>
  <tr>
    <td>Length</td>
    <td>Width</td>
    <td>I<sub>d</sub></td>
  </tr>
  <tr>
    <td>180nm</td>
    <td>0.1um</td>
    <td>11.2uA</td>
  </tr>
  <tr>
    <td>180nm</td>
    <td>0.15um</td>
    <td>29.5uA</td>
  </tr>
  <tr>
    <td>180nm</td>
    <td>0.2um</td>
    <td>37.9uA</td>
  </tr>
  <tr>
    <td>180nm</td>
    <td>0.25um</td>
    <td>45.7uA</td>
  </tr>
  <tr>
    <td>180nm</td>
    <td>0.3um</td>
    <td>53.2uA</td>
  </tr>
  <tr>
    <td>180nm</td>
    <td>0.316um</td>
    <td>55.6uA</td>
  </tr>
</table>
<br>v<sub>ds</sub>=v<sub>d</sub>-v<sub>s</sub></br>
<br>1.8-0 = 1.8v</br>
<br>As v<sub>ds</sub>>v<sub>ov</sub></br> the mosfet is in saturation region.</br>
<br>From the above calculations the operating point is (V<sub>ds</sub>,I<sub>d</sub>) = (1.8v,55.6uA)</br>
<br>**Transient Analysis**</br>
<br>![Image](https://github.com/user-attachments/assets/547746fc-1925-4d24-a741-9fcc5da06f99)</br>
<br><p>This is a time domain simulation technique used to observe the circuit response to time varying inputs.In this circuit for the input we need to give sinusoidal voltage signal in which the DC offset is 0.9v and the V<sub>peak</sub> is 50mV and the frequency is 1KHz the AC amplitude will be 1V. For this circuit analysis we had given stop time as 3ms.</p></br>
<br><p>From the above graph we can calculated the gain of the circuit.</p></br>
<br>A<sub>v</sub>sub>=V<sub>out</sub>/V<sub>in</sub></br>
<br>A<sub>v</sub>=1.75v / 950mV</br>
<br>A<sub>v</sub>=1.8V/V</br>
<br><p>which will match the theortical value calculated by A<sub>v</sub>=gmR<sub>d</sub></p></br>
<br>Where gm=K<sub>n</sub>V<sub>ov</sub></br>
<br><p>From graph we can clearly observe their is an 180 degree phase shift that is exibited by common souce configuration.</p></br>
<br><p>Therefore we can conclude that its gain > 1 and has 180 degree phase shift therefore its an NMOS common source amplifier.</p></br>
<br>**AC Analysis**</br>
<br><p>In this AC analysis we will evaluate the frequency response cure of the given circuit.By applying the small analysis for the given circuit. In this Analysis we need to check in which frequency it act as a linear amplifier</p></br>  
<br><p>While doing simulation we need to select the decade as type of sweep, with starting frequency as 0.1Hz and the stoping frequency as 1THz.</p></br> 
<br>![Image](https://github.com/user-attachments/assets/32f529dd-7913-4d45-b704-1f3af2d1d71d)</br>
<br>**Frequency response**</br>
<br><p>In this due to higher frequency the parasitic capacitor will get activated.</p></br>
<br><p>At lower frequency the coupling capacitors will get activated.</p></br>

