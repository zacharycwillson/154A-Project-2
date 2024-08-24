# Project 2 README

Student 1: Zachary Willson (922725803)
Student 2: Qihan Guan (922758317)

## Project Status
Lock is completed and working as expected. Submission includes the Panel subcircuit from partner Qihan Guan along with my implimentations of
subcircuit 2 Input Panal and subcircuit 3 Lock. Lock subcircuit uses an input decoder,meta-state demux and substate demuxes to have an abstracted 2 input logic. The lock follows an implimentation of four meta states having 4 substates each.

## Known Issues
There are no known issues at this moment.

## References

## Generative AI Use
I used ChatGPT for Prompt 1

### Prompt 1
I am using logisim for a project. I need to have the selector on the mux turn 1 on the rising edge of input V and stay 1 for one clock cycle, then turn back to 0 until the next rising edge of input v. How may this be implimented? 

### Response 1
To implement this in Logisim, you can use a D flip-flop to detect the rising edge of input V and generate a single clock cycle pulse that controls the selector of the multiplexer (mux). Here's how you can implement it:

Step-by-Step Implementation:
Detect Rising Edge of V:

Use a D flip-flop to store the previous value of V.
XOR the current value of V with the previous value to detect the rising edge. When there's a transition from 0 to 1 (rising edge), the XOR will output 1.
Generate Single-Cycle Pulse:

After detecting the rising edge, you want to generate a 1 for one clock cycle. You can feed the XOR output into another D flip-flop that is clocked by the system clock. The output of this flip-flop will be a 1 for one clock cycle.
Connect to Mux Selector:

Use the output of the D flip-flop from step 2 as the control input for the mux selector.
Circuit Diagram Outline:
V → XOR (with delayed V using a D flip-flop) → Output = Rising Edge Detect
Rising Edge Detect → D flip-flop (clocked) → Mux Selector Input
This ensures that the mux selector turns to 1 on the rising edge of V and stays at 1 for exactly one clock cycle before going back to 0.

Let me know if you need further clarification!
### Changes 1
I added an AND gate after the suggested XOR to ensure the 1 from the flip flop only outputs when V is 1

### Prompt 2
My other prompt...

### Response 2
The other response...

### Changes 2
The other changes made...
