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

Full Adder

<img width="593" height="542" alt="image" src="https://github.com/user-attachments/assets/4d3dfa27-2b6b-4a2f-9d1c-a1a76ba68b72" />





Full Subtractor

<img width="606" height="532" alt="image" src="https://github.com/user-attachments/assets/4cc12fc2-f030-4c64-9ee1-c5dbc19a3c20" />



**Procedure**

Write the detailed procedure here

**Program:**
```
Full Adder

module exp4(df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule


Full Subtractor

module full_subtractor(diff, borrow, a, b, bin);
  output diff;
  output borrow;
  input a;
  input b;
  input bin;
  assign diff = a ^ b ^ bin;
  assign borrow = (a & b) | ((a ^ b) & bin);
endmodule

```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**

Full-Adder

<img width="1032" height="598" alt="image" src="https://github.com/user-attachments/assets/1bb85f08-4b50-478b-a5fa-dc8f5205fb80" />

Full Subtractor
<img width="1033" height="597" alt="image" src="https://github.com/user-attachments/assets/e1719d64-d63c-4dec-bf35-02a2349afa00" />

**Output Timing Waveform**

Full-Adder

<img width="1038" height="593" alt="image" src="https://github.com/user-attachments/assets/7b10a4f4-583e-44e4-90a9-ab6cc1c2a81a" />

Full Subtractor

<img width="1025" height="498" alt="image" src="https://github.com/user-attachments/assets/b5786b7d-17c5-4e56-a741-92ac45ed1247" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



