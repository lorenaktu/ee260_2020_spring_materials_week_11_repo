---
title: 
author:
partner:
date:
---
## (5 pts)
Capture the following system behavior as an HLSM. The system counts the number of events on a single-bit input B and always outputs that number unsigned on a 16-bit output C, which is initially 0. An event is a change from 0 to 1 or from 1 to 0. Assume the system count rolls over when the maximum value of C is reached.

## (5 pts)
Create a high-level state machine that initializes a 16x32 register file’s contents to 0s, beginning the initialization when an input rst becomes 1. The register file does not have a clear input; each register must be individually written with a 0. Do not define 16 states; instead, declare a local storage item so that only a few states need to be defined. 

## (5 pts)
 Use the RTL design process to design a system that outputs the average of the most recent two data input samples. The system has an 8-bit unsigned data input I, and an 8-bit unsigned output avg. The data input is sampled when a single-bit input S changes from 0 to 1. Choose internal bitwidths that prevent overflow. 

## (5 pts)
Use the RTL design process to create an alarm system that sets a single-bit output alarm to 1 when the average temperature of four consecutive samples meets or exceeds a user-defined threshold value. A 32-bit unsigned input CT indicates the current temperature, and a 32-bit unsigned input WT indicates the warning threshhold. Samples should be taken every few clock cycles. A single-bit input clr when 1 disables the alarm and the sampling process. Start by capturing the desired system behavior as an HLSM, and then convert to a controller/datapath.

## (5 pts)
(a) Convert the laser-based distance measurer’s FSM, shown in this week's slides, to a state register and logic. (b) Assuming all gates have a delay of 2 ns and the 16-bit up-counter has a delay of 5 ns, and wires have no delay, determine the critical path for the laser-based distance measurer. (c) Calculate the corresponding maximum clock frequency for the circuit.

## (5 pts)
Design a data-dominated system that computes and outputs the sum of the absolute values of 16 separate 32-bit registers (not in a register file) storing signed numbers (do not consider how those numbers get stored). The computation of the sum should be done using a single equation in one state. The computation should be performed once when a single-bit input go changes from 0 to 1, and the computed result should be held at the output until the next time go changes from 0 to 1.


## (5 pts)
Convert the following C-like code, which calculates the greatest common divisor (GCD) of the two 8-bit numbers a and b, into a high-level state machine.

```c
Inputs: byte a, byte b, bit go
Outputs: byte gcd, bit done
GCD:
while(1) {
	while(!go);
	done = 0;
  while ( a != b ) {
    if( a > b ) {
    a = a - b;
    }
    else {
    b = b - a;
    }
  }
  gcd = a;
  done = 1;
}
```
