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
    <td>  </td>
    <td>  </td>
    <td>  </td>
  </tr>
  <tr>
    <td>  </td>
    <td>  </td>
    <td>  </td>
  </tr>
  <tr>
    <td>  </td>
    <td>  </td>
    <td>  </td>
  </tr>
  <tr>
    <td>  </td>
    <td>  </td>
    <td>  </td>
  </tr>
</table>
![Image](https://github.com/user-attachments/assets/547746fc-1925-4d24-a741-9fcc5da06f99)
![Image](https://github.com/user-attachments/assets/32f529dd-7913-4d45-b704-1f3af2d1d71d)

