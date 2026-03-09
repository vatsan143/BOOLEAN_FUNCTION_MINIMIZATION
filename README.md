# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

Digital logic circuits can be implemented using Boolean expressions and verified using Hardware Description Languages (HDLs) such as Verilog. Verilog allows the designer to describe the behavior and structure of digital circuits using simple programming constructs.

In this experiment, the given logic function is implemented using basic logic gates such as NOR and NAND gates. The circuit is purely combinational, meaning the output depends only on the present inputs and not on any previous state. Hence, continuous assignment statements are used in Verilog to model the logic behavior.

The inputs are first applied to intermediate logic gates to generate internal signals. These internal signals are declared as wire data types because they carry continuously driven values. The final output is obtained by applying logical operations on these intermediate signals.

The Verilog code is compiled and simulated using Intel Quartus Prime software. Functional verification is performed by applying different combinations of inputs and observing the corresponding output in the simulation waveform. This confirms that the implemented logic function matches the expected truth table and operates correctly.

Thus, Quartus provides an efficient platform for design, simulation, and verification of digital logic circuits before hardware implementation.

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.


**Program:**

Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 
```
module funct1(a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1=((~a & ~b & ~c & ~d)|(a & ~c & ~d)|(~b & c & ~d)|(b & ~c & d));
endmodule

module funct2(w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2=((x & ~y & z)|(~x & ~y & z)|( ~w & x & y)|(w & ~x & y)|(w & x & y));
endmodule
```

Developed by: RegisterNumber: 25018756



**RTL realization:**



F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

<img width="1920" height="1080" alt="17664859006188779294576152428389" src="https://github.com/user-attachments/assets/2bbdb91c-3109-4d2e-b162-a2b320a8b894" />


F2=xy’z+x’y’z+w’xy+wx’y+wxy

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8ecc9d44-fc34-42b5-b3f1-6b6713dc4c0c" />





**Output(Timing Diagram RTL):**



F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

F1=B'D'+ABC'+A'BD(MINIMISED)


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/80f37857-7a37-4e2e-94e6-780bf4392baf" />



F2=xy’z+x’y’z+w’xy+wx’y+wxy

F2=y'z+ wy + xy(MINIMISED)


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/86d7ab81-9a12-44dc-bef1-5b8c175fc2b8" />




**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.




