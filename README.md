### ENCODER 8TO3 DATAFLOW Modelling

**AIM:**

To implement  Encoder 8 To 3 in Dataflow Modelling using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:** Quartus prime

**THEORY**

**Encoder 8 To 3**

The 8 to 3 line Encoder is also known as Octal to Binary Encoder. In 8 to 3 line encoder, there is a total of eight inputs, i.e., D0, D1, D2, D3, D4, D5, D6, and D7 and three outputs, i.e., A0, A1, and A2. In 8-input lines, one input-line is set to true at a time to get the respective binary code in the output side. Below are the block diagram and the truth table of the 8 to 3 line encoder.

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/0bc242c1-eb9e-4c47-afe5-30428470efc3)

Figure 01  Block Diagram of Encoder 8 * 3

**Truth Table**

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/35496b14-ae6e-4cd1-9abd-d6736b576575)

The logical expression of the term A0, A1, and A2 are as follows:

A0 = D1 + D3 + D5 + D7

A1 = D2 + D3 + D6 + D7

A2 = D4 + D5 + D6 + D7

Logical circuit of the above expressions is given below:

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/95acaee6-c873-4c75-89eb-ef09fb158053)

Figure 02  Encoder 8 * 3

**Procedure**
1.Understand the Encoder:

An 8-to-3 encoder has 8 input lines (D[7:0]) and 3 output lines (Y[2:0]).

Only one input should be high at a time.

2.Write the Boolean Equations:

Y[2] = D7 + D6 + D5 + D4

Y[1] = D7 + D6 + D3 + D2

Y[0] = D7 + D5 + D3 + D1

3.Use Dataflow Modeling:

Implement these equations using assign statements in Verilog or concurrent signal assignments in VHDL.

**PROGRAM**

/* Program for Encoder 8 To 3 in Dataflow Modelling and verify its truth table in quartus using Verilog programming.
```
module EXP05(din,a,b,c);
input [0:7] din;
output a,b,c;
assign a=(din[4]| din[5]| din[6]|din[7]);
assign b=(din[2]| din[3]| din[6]|din[7]);
assign c=(din[1]| din[3]| din[5]|din[7]);
endmodule
```
Developed by:DIVYASHREE B RegisterNumber:212224040081
*/

**RTL LOGIC FOR Encoder 8 To 3 in Dataflow Modelling**
![image](https://github.com/user-attachments/assets/0a7db31c-368d-41d8-aee1-037b9cb27f71)


**TIMING DIGRAMS FOR Encoder 8 To 3 in Dataflow Modelling**
![image](https://github.com/user-attachments/assets/0a7db31c-368d-41d8-aee1-037b9cb27f71)

**RESULTS**
 Thus the OUTPUT'S of encoder and decoder are verified by synthesizing and simulating the VERILOG code.



