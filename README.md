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

<img width="429" height="395" alt="3im3" src="https://github.com/user-attachments/assets/79182231-28c4-4248-b34d-4d4a90de1c4e" />

FULL SUBTRACTOR

<img width="438" height="393" alt="3im4" src="https://github.com/user-attachments/assets/7b5712ad-100c-4171-82e8-681b3827a1f4" />


**Procedure**

Write the detailed procedure here

**Program:**


~~~
Developed by:Branzen B V
RegisterNumber: 21222510000
~~~

~~~
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

module Exp4(a,b,cin,sum,carry,diff,borrow);
input a,b,cin;
output sum,carry,diff,borrow;
wire adash;
not (adash,a);
assign sum = a^b^cin;
assign carry = (a&b)|(b&cin)|(a&cin);
assign diff = a^b^cin;
assign borrow = (adash&b)|(b&cin)|(adash&cin);
endmodule
~~~

**RTL Schematic**

<img width="1920" height="1080" alt="3im5" src="https://github.com/user-attachments/assets/abb9a8e3-3346-44d6-990c-59ae7f0ead34" />


**Output Timing Waveform**

<img width="1920" height="1080" alt="3im6" src="https://github.com/user-attachments/assets/169008dc-3aec-4381-8208-b5bae4705909" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



