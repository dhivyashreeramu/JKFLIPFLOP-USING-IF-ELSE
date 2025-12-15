# JKFLIPFLOP-USING-IF-ELSE

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**

Study the JK Flip-Flop Functionality

Refer to the JK flip-flop truth table to understand its operation:

J = 0, K = 0 → No change

J = 0, K = 1 → Reset

J = 1, K = 0 → Set

J = 1, K = 1 → Toggle

Create a New Verilog Project

Open the Verilog simulation tool (ModelSim / Xilinx Vivado / Quartus / Icarus Verilog).

Create a new project and add a new Verilog module file for the JK flip-flop.

Write the Verilog Code for JK Flip-Flop

Define inputs: J, K, clk (and reset if required).

Define output: Q (and Q_bar if required).

Use an always block triggered on the positive edge of the clock.

Implement the JK logic using a case statement or conditional statements.

Save and Compile the Design

Check for syntax errors.

Ensure the design compiles successfully without warnings or errors.

Create a Testbench

Write a separate Verilog testbench module.

Declare the required input signals as reg and outputs as wire.

Instantiate the JK flip-flop module.

Generate a clock signal using an always block.

Apply all possible combinations of J and K inputs at different clock cycles.

Simulate the Design

Run the simulation.

Observe the output Q for each combination of J and K.

Ensure changes occur only at the active clock edge.

Verify Using Functional Table

Compare the simulated output with the JK flip-flop truth table.

Confirm:

No change for J=0, K=0

Reset for J=0, K=1

Set for J=1, K=0

Toggle for J=1, K=1

Analyze the Waveforms

Use the waveform viewer to verify timing relationships.

Ensure proper synchronization between inputs and clock.

Document the Results

Record observations.

Capture waveform screenshots if required.

Conclude that the JK flip-flop functions as expected.

**PROGRAM**

```
module jkff(j,k,clk,q,qbar);
input j,k,clk;
output reg q,qbar;
initial 
begin
q=1'b0;
q=1'b1;
end 

always @(posedge clk)
begin 
q<=(j&~q)|(~k&q);
qbar<=~q;
end
endmodule
```
**RTL LOGIC FOR FLIPFLOPS**
![WhatsApp Image 2025-12-15 at 13 01 46_80310d99](https://github.com/user-attachments/assets/88f857b9-0ced-40a8-ab78-908f3ada3c22)


**TIMING DIGRAMS FOR FLIP FLOPS**
![WhatsApp Image 2025-12-15 at 13 24 51_2698bb4d](https://github.com/user-attachments/assets/5ee66dc6-ad85-4135-bf4e-6fa561ccf001)


**RESULTS**
 thus the program To implement JK flipflop using verilog and validating their functionality using their functional tables sucessfully
