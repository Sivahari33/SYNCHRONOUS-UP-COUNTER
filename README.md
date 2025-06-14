### SYNCHRONOUS UP COUNTER

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
1.Initialize the shift register to a known state (e.g., all zeros).

2.Input a bit serially into the shift register.

3.Shift the contents of the register one position to the right (or left).

4.Output the shifted bit from the last stage of the register.

5.Repeat steps 2-4 for each bit you want to input and shift.

**PROGRAM**
 
![397905858-9cfd4a57-816c-40a7-a1ff-ee00c6d940ea](https://github.com/user-attachments/assets/322b33c1-65bb-47da-983b-9f8841ef4024)

Developed by:SIVAHARIBALAN K
RegisterNumber:24007220
![397905880-d17a043b-aabe-44fc-8a65-a08cba89f986](https://github.com/user-attachments/assets/2a6be4c8-91aa-44b6-ab65-4a7e069bae5e)


**RTL LOGIC UP COUNTER**
![397905866-1a17d74b-1ce6-471d-b962-e950d5c8ff4e](https://github.com/user-attachments/assets/259b2557-a91e-435f-a5b7-3d94ab6eaeaf)

**TIMING DIAGRAM FOR IP COUNTER**
![397905880-d17a043b-aabe-44fc-8a65-a08cba89f986](https://github.com/user-attachments/assets/2a6be4c8-91aa-44b6-ab65-4a7e069bae5e)
**TRUTH TABLE**
![397905895-db284906-f159-43a8-8dc0-c85b1a234658](https://github.com/user-attachments/assets/4b1f8709-dd5f-4320-8ac7-ce3784c8a395)

**RESULTS**
Hence a 4 bit synchronous up counter is implemented correctly.
