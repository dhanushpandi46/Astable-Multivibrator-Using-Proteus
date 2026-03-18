## Experiment No: 5
ASTABLE MULTIVIBRATOR USING 555 TIMER Using Proteus
## Aim
To design and simulate an Astable Multivibrator using NE555 in Proteus Design Suite and observe the continuous square wave output.
## Apparatus Required
•	NE555 Timer IC
•	Resistor R1 = 10 kΩ
•	Resistor R2 = 100 kΩ
•	Capacitor C = 0.01 µF
•	DC Power Supply (5V or 9V)
•	CRO / Oscilloscope
•	Connecting wires
## Circuit Diagram
Pin Configuration of 555 Timer:

<img width="692" height="421" alt="image" src="https://github.com/user-attachments/assets/eee9f457-44b9-409f-8a3f-f599fe2f85ff" />

•	Pin 1 → Ground
•	Pin 2 → Trigger
•	Pin 3 → Output
•	Pin 4 → Reset (Connected to Vcc)
•	Pin 5 → Control Voltage (Bypass with 0.01 µF capacitor optional)
•	Pin 6 → Threshold
•	Pin 7 → Discharge
•	Pin 8 → Vcc
## Connections:
•	R1 → Between Vcc and Pin 7
•	R2 → Between Pin 7 and Pins 2 & 6
•	C → Between Pins 2 & 6 and Ground
•	Output → Pin 3
## Theory
•	The NE555 timer is a widely used integrated circuit for generating precise time delays and oscillations. When operated in astable mode, it functions as a free-running oscillator that continuously produces a square wave without any external triggering signal. In this mode, a capacitor connected to the circuit charges through resistors R1 and R2 and discharges through R2 repeatedly. The internal voltage divider of the 555 timer creates two reference levels at 1/3 Vcc and 2/3 Vcc. 
•	When the capacitor voltage reaches 2/3 Vcc, the upper comparator resets the flip-flop and turns ON the discharge transistor, causing the capacitor to discharge. When the voltage falls to 1/3 Vcc, the lower comparator sets the flip-flop, turning OFF the discharge transistor and allowing the capacitor to charge again. This continuous charging and discharging process generates a square wave at the output (Pin 3) and an exponential waveform across the capacitor. The time period of oscillation is given by T=0.693(R1+2R2)CT = 0.693 (R1 + 2R2) CT=0.693(R1+2R2)C, and the frequency depends on the values of R1, R2, and C. Thus, the 555 timer in astable mode acts as a simple and reliable square wave generator used in clock circuits, LED flashers, and pulse generation applications.
## Procedure
1.	Open Proteus software.
2.	Select NE555 IC, resistors, capacitor, and CRO.
3.	Connect circuit in astable configuration.
4.	Apply 5V supply.
5.	Run simulation.
6.	Observe square wave output at Pin 3.
7.	Measure time period and frequency.
## Tabulation
| Sl. No | Capacitor Voltage (Vc)      | Condition       | Output Voltage (Vo) |
| ------ | --------------------------- | --------------- | ------------------- |
| 1      | 1/3 VCC ≈ 1.67 V            | Trigger level   | Output HIGH (5 V)   |
| 2      | Charging (1.67 → 3.33 V)    | During TON      | Output = 5 V        |
| 3      | 2/3 VCC ≈ 3.33 V            | Threshold level | Output LOW (0 V)    |
| 4      | Discharging (3.33 → 1.67 V) | During TOFF     | Output = 0 V        |
| 5      | Reaches 1/3 VCC             | Cycle repeats   | Output HIGH         |


## Waveforms
•	Output (Pin 3) → Square wave
•	Capacitor voltage → Exponential charging & discharging waveform

<img width="691" height="439" alt="image" src="https://github.com/user-attachments/assets/d664a63b-1ed7-4877-9e6a-565ca53fc890" />

## Result
The Astable Multivibrator using NE555 Timer IC was successfully designed and simulated in Proteus.
A continuous square wave output was obtained.
The practical frequency closely matches the theoretical frequency.
## Conclusion
•	The 555 timer works as a free-running oscillator in astable mode.
•	Frequency depends on R1, R2, and C values.
•	Increasing R or C decreases frequency.
•	Used in clock generation, LED flashing, and tone generation.
## Viva Questions
1.	What are the operating modes of 555 timer?

Operating Modes: Monostable, Astable, and Bistable modes.

2.	What are the threshold levels in astable mode?

Threshold Levels in Astable Mode: The capacitor charges and discharges

3.	Write the frequency formula.

f=(R1​+2R2​)C1.44​

4.	What is duty cycle?

Duty Cycle: The percentage of time the output remains HIGH in one complete cycle.

5.	What happens if R2 increases?

If R2 Increases: The time period and duty cycle increase while frequency decreases.
