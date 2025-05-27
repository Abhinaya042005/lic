# Analog Calculator Using Op-Amps

# Abstract
This project explores the design and implementation of a basic analog calculator capable of performing addition, subtraction, and multiplication operations using operational amplifiers (Op-Amps). The goal is to illustrate analog computing principles through the construction of circuits based on the widely used 741 op-amp. Each arithmetic operation utilizes distinct op-amp configurations: summing amplifiers, differential amplifiers, and log/antilog amplifiers. The result demonstrates real-time signal processing capabilities of analog computation with minimal components.
# Introduction
Analog computing, though largely eclipsed by digital processing in mainstream applications, remains relevant in niche areas such as signal conditioning, real-time audio processing, and embedded analog control systems. This project seeks to revive the practical understanding of analog computation through the implementation of an analog calculator.

The project targets:
Introducing core op-amp configurations for arithmetic functions.
Demonstrating mathematical operations in real-time without digital conversion.
Applying theoretical electronics principles in practical circuit design.
The operational amplifier 741 is chosen due to its widespread availability, robustness, and educational value. Despite its limitations in speed and bandwidth, it provides an excellent platform for exploring analog signal operations.

# Circuit Diagrams and Working Principles
**Addition Circuit: Summing Amplifier**
Working Principle:

A summing amplifier in inverting mode takes multiple voltage inputs through resistors and produces an output proportional to the negative sum of those inputs.

Working:
The op-amp operates in the inverting mode, summing the current from each input:
V<sub>out</sub> = -R<sub>f</sub> &times; (V<sub>1</sub>/R<sub>1</sub> + V<sub>2</sub>/R<sub>2</sub> + ... + V<sub>n</sub>/R<sub>n</sub>)


