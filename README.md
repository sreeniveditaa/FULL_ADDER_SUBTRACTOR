# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

FULL ADDER

![image](https://github.com/sreeniveditaa/FULL_ADDER_SUBTRACTOR/assets/147473268/15fe1ec1-94e6-4f8e-8c43-54029bb98471)

FULL SUBRACTOR

![image](https://github.com/sreeniveditaa/FULL_ADDER_SUBTRACTOR/assets/147473268/6da4cd8c-a54c-4bc8-a8d4-3c16f8f7dc2d)


**Procedure**

 STEP 1: Use module project name(input,output) to start the Verilog programmming. 
 STEP 2: Assign inputs and outputs using the word input and output respectively.
 STEP 3: Use defined keywords like wire,assign and required logic gates to represent the boolean expression. 
 STEP 4: Use each output to represnt onre for differnce and the other for borrow. 
 STEP 5: End the verilog program using keyword endmodule.

**Program:**

```
DEVOLOPED BY : SREE NIVEDITAA SARAVANAN
REGISTER NO. : 212223230213

```
```

module fulladdsub(a,b,cin,sum,carry,BO,DIFF);
input a,b,cin;
output sum,carry,BO,DIFF;
assign sum=(a^b^cin);
assign carry=(a&b)|(a&cin)|(b&cin);
assign DIFF=(a^b^cin);
assign BO=(~a&b)|(~(a^b)& cin);
endmodule

```

**RTL Schematic**

![Screenshot 2024-04-01 065107](https://github.com/sreeniveditaa/FULL_ADDER_SUBTRACTOR/assets/147473268/6597434c-de2b-4b54-bb7d-1211474f6a3e)


**Output Timing Waveform**

![Screenshot 2024-04-01 065524](https://github.com/sreeniveditaa/FULL_ADDER_SUBTRACTOR/assets/147473268/110e0030-798d-4db1-9f66-7d198caf1c25)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



