# Monostable multivibrator using 555 timer IC 
# Aim:

To design and implement a circuit using the 555 timer IC to generate a 0.5 ms pulse waveform in monostable mode, with trigger pulses derived from an astable multivibrator.

# Introduction
The 555 timer IC is one of the most widely used and versatile components in analog and digital electronics. It can be configured in three primary modes: astable, monostable, and bistable, each serving different purposes based on the desired functionality of the circuit.

**1. Astable Mode**
In astable mode, the 555 timer continuously oscillates between high and low states without requiring any external triggering. It produces a constant square wave output, making it useful for generating clock pulses, flashing LEDs, and tone signals. The time period and duty cycle of the waveform can be adjusted by selecting appropriate values for two resistors and one capacitor connected to the timer. Since it has no stable state, it is called "astable" (meaning "not stable").

**2. Monostable Mode**
In monostable mode, the 555 timer has one stable state (low) and one unstable state (high). When a negative trigger pulse is applied to the trigger pin, the timer output goes high for a fixed time duration (determined by an external resistor and capacitor), and then automatically returns to its stable low state. This mode is ideal for pulse width generation, timers, and applications requiring a single output pulse in response to an input event.

**4. Bistable Mode**
In bistable mode, the 555 timer has two stable states—high and low. The output can be toggled between these states using two external inputs: a trigger and a reset. Unlike the other modes, the timer does not change state automatically; it remains in its current state until triggered to change. This configuration is useful for applications such as flip-flops, memory storage, and toggle switches.
