**Experiment-1**<br> Common source amplifier analysis</br>
<br>This experiment is done to show the AC,DC,Transient analysis of common source amplifier</br>
<br>**Theory:**</br>
<br><p>A common source amplifier is one of the most fundamental amplifier configuration.There are three different configuration in which the mosfet can be connected(drain, gate,source)the most popular being common source and common drain configuration. The Moseft acts as an amplifier in the saturation region of operation where V<sub>gs</sub>>V<sub>th</sub>,V<sub>gd</sub><V<sub>th</sub> and V<sub>ds</sub>>=V<sub>ov</sub> for an N channel mosfet.In common source amplifier configuration using MOSFET the source terminal is common to both input and output.</p><br/>
<br><p>The drain current: 1/2 K<sub>n</sub>V<sub>ov</sub><sub>2</sub>.</p></br>
<br><p>where V<sub>ov</sub>=V<sub>gs</sub>-V<sub>th</sub> and K<sub>n</sub>=U<sub>n</sub>C<sub>ox</sub>W/L</p></br>
<br>**Circuit-1**</br>
![Image](https://github.com/user-attachments/assets/275fcbf0-86b9-4b9f-bd4c-49fa6eaffd4d)
<br>**Component Details**</br>
<br>This circuit consist of CMOSN (NMOS transistor) tsmc , resistor across drain and two voltage source each connect to R<sub>d</sub> and gate terminal.</br>
<br>MOSFET length - 180nm</br>
<br>MOSFET width - 0.315um</br>
<br>supply voltage - 1.8v</br>
<br>Resistor - 1k</br>
<br>**DC Analysis**</br>
<br><p>This is done to ensure the mosfet operates in saturation and to calculate the DC operating point of the transistor.This helps in determination of the biaing resistors.This helps in obtaining the correct operating point despite the fluctuatioon in the other parameters.</p></br>
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
<br><p></p>Transient Analysis is done to analysis the response of the circuit to time varying signals. This helpfull to determine the signal distortion ,DC shift between the input and the output. This plays the key role in detecting issues like phase distortion. This is essential for high speed applications like communication systems.</p></br> 
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
<br>**Circuit-2**</br>
<br>**Theory**</br>
<br><p></p>A diode connected mosfet transistor always is in saturation and acts as a amplifier. The different type of analysis are DC Analysis, AC analysis and transient analysis. The drain current obtained is given by the formula:</p></br>
<br>I<sub>d</sub>=1/2K<sub>n</sub>V<sub>ov</sub><sub>2</sub> ; V<sub>ov</sub>=V<sub>gs</sub>-V<sub>th</sub> and K<sub>n</sub>U<sub>n</sub>C<sub>ox</sub>W/L
<br>![Image](https://github.com/user-attachments/assets/8e90316f-c5da-4e86-9363-d0995e4d03c0)</br>
circuit daigram image
<br>**Component Details**</br>
<br><p>This circuit consist of two CMOS (NMOS and PMOS)tsmc, and two voltage source one at drain terminal of first MOSFET other at gate terminal of second MOSFET.</p></br>
<br>Mosfet length - 180nm</br>
<br>Mosfet width - 85um</br>
<br>Supply voltage - 1.8v</br>
<br>**DC Analysis**</br>
<br><p>DC Analysis is done to ensure the mosfet operates in saturation and to calculate the DC operating point of the transistor.This helps in getting a correct operating point despite the fluctuation in the other parameters.</p></br>
<br>![Image](https://github.com/user-attachments/assets/2b61b087-1095-4424-8173-03ec7f93c23b)</br>
<br>V<sub>out</sub>=1.66V, V<sub>in</sub>=0.6V,I<sub>d</sub>=55.5uA.</br>
<br>Given power diddipation is 100uW, then the current will be I<sub>d</sub>=Power/Voltage=55.5uA.</br>
<table>
  <tr>
    <td>Width(um)</td>
    <td>I<sub>d</sub>(uA)</td>
    <td>Vout(V)</td>
  </tr>
  <tr>
    <td>0.2</td>
    <td>26.7</td>
    <td>1.56</td>
  </tr>
  <tr>
    <td>0.4</td>
    <td>34.06</td>
    <td>1.62</td>
  </tr>
  <tr>
    <td>0.6</td>
    <td>42.8</td>
    <td>1.64</td>
  </tr>
  <tr>
    <td>0.8</td>
    <td>51.9</td>
    <td>1.65</td>
  </tr>
  <tr>
    <td>0.88</td>
    <td>55.6</td>
    <td>1.66</td>
  </tr>
</table>
<br>V<sub>ds</sub>=V<sub>d</sub>-V<sub>s</sub>=1.66-0=1.66V</br>
<br>From the above calculation the operating point = (1.66V,55.6uA)</br>

<br>**Transient Analysis**</br>
<br><p></p>This is done to analysis the response of the circuit to time varying signals. This is helpful determine the signal distortion, DC shift between the input and the output. This plays key role in detecting issues like phase distortion. This is essential for high speed applications like communication systems.</p></br>
<br>![Image](https://github.com/user-attachments/assets/b0167887-69c4-44fb-91ba-da4359a80bd3)</br>
<br>From the graph we can calculate the gain of the circuit</br>
<br>A<sub>v</sub>=V<sub>out</sub>/V<sub>in</sub></br>
<br>A<sub>v</sub>=1.7V/0.75V</br>
<br>A<sub>v</sub>=2.26V/V</br>
<br>**AC Analysis**</br>
<br><p></p>AC Analysis is the small signal analysis of the circuit.This is done to determine the gain of the amplifier circuit.This also helps to analysis the frequency response of the amplifier circuit.The gain is given by A<sub>v</sub>=-g<sub>m</sub>R<sub>d</sub></p></br> 
<br>During the process of AC simulation we need to select the decade as type of sweep, with starting frequency as 0.1Hz and the stoping frequency as 1THz.</br>

<br>**Inference**</br>
<br><p>**AC Analysis**: This deals with circuit powered by alternating current soources, where voltage and current change direction periodically. Analyzes steady state behaviour using phasor or representataion, impedance, and frequency response.</p></br>
<br><p>**DC Analysis**: It focuses on circuits powered by direct current sources, where voltage and current remain constant over time.Uses ohm's laws kirchhof's laws, and network theorems for solving circuit parameters</p></br>
<br><p>**Transient Analysis**: Examines circuit behaviour during the transition from one steady state condition to another .Involves solving differential equations related to capacitors and inductors,which store and release energy.</p></br>
