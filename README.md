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

![WhatsApp Image 2024-12-02 at 9 33 56 PM](https://github.com/user-attachments/assets/a0cb4f7b-9b1e-4cca-a2b7-0ffd49883a89)


**Procedure**

Write the detailed procedure here

**Program:**

```
Full Adder:
 module fulladder(sum, cout, a, b, cin);
 input a;
 input b;
 input cin;
 output sum;
 output cout;
 wire w1,w2,w3;
 assign w1=a^b;
 assign w2=a&b;
 assign w3=w1&cin;
 assign sum=w1^cin;
 assign cout=w2|w3;
 endmodule

Full Subtractor:
 module fullsubtractor(a, b, cin, diff, borrow); 
input a; 
input b; 
input cin; 
output diff; 
output borrow; 
wire abar; 
assign abar= ~ a; 
assign diff=a^b^cin; 
assign borrow=(abar & b) | (b & cin) |(cin & abar); 
endmodule

```

 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
 
 Developed by: Shyam Kumar.S
 
 RegisterNumber: 24001160

**RTL Schematic**

Full Adder:
![3(fa)](https://github.com/user-attachments/assets/29496e16-6045-44d2-a252-5b6e0c799084)

Full Subtractor:
![3(fs)](https://github.com/user-attachments/assets/03288d4e-b11a-4166-816e-6dcd0202b583)

**Output Timing Waveform**

Full Adder:
![3 1(fa)](https://github.com/user-attachments/assets/fd27b6cb-565a-45c5-97bd-84079a8cf9b8)

Full Subtractor:
![3 1(fs)](https://github.com/user-attachments/assets/9937c3e3-1bdb-4998-b465-78fe2d651568)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



