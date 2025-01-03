### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**
Open Quartus Prime software.

Create a new project and include a Verilog file for the counters.

Write the Verilog code for both counters.

Compile the project to check for errors.

Simulate the design to observe the waveform outputs.

Compare the outputs against the truth table to verify functionality.

Generate the RTL schematics and timing diagrams.

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

![Screenshot 2024-12-18 144346](https://github.com/user-attachments/assets/cd63cd3c-6826-4687-bed8-18d81a122548)

Developed by : THAMIZH.S
RegisterNumber : 24900483


*/

**RTL LOGIC UP COUNTER**
![Screenshot 2024-12-17 182825](https://github.com/user-attachments/assets/546a844e-3d55-4bb5-8b43-d77d179768ee)

**TIMING DIAGRAM FOR IP COUNTER**
![Screenshot 2024-12-18 143615](https://github.com/user-attachments/assets/0af06030-29d7-4989-af32-b82a0f9e4690)


**TRUTH TABLE**
![Screenshot 2024-12-17 181627](https://github.com/user-attachments/assets/cdd6e47d-a50d-4f6e-898a-c8e2a39a92fc)

**RESULTS**





Both the 4-bit ripple counter and the 4-bit synchronous up counter were successfully implemented in Verilog, and their functionality was validated using simulation results.
