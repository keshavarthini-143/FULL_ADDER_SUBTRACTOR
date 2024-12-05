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


![Screenshot 2024-12-05 204333](https://github.com/user-attachments/assets/1068e614-6df6-4cc9-98fc-dfae3781afbe)



FULL SUBTRACTOR


![Screenshot 2024-12-05 204511](https://github.com/user-attachments/assets/cdf6d331-3d0a-4df6-a7a0-02d8e1e60017)



**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: KESHAVARTHINI B    RegisterNumber:24900033
*/

FULL ADDER


module full_adder(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

wire w1,w2,w3;

assign sum=(a^b)^c;

assign w1=a&b;

assign w2=b&c;

assign w3=c&b;

assign carry=w1|w2|w3;

endmodule


FULL SUBTRACTOR


module half_subtractor(a,b,bin,diff,borrow);

input a,b,bin;

output diff,borrow;

wire c;

assign c=~a;

assign diff=a^b^bin;

assign borrow=(c&b)|(b&bin)|(bin&c);

endmodule



**RTL Schematic**

FULL ADDER


![Screenshot (41)](https://github.com/user-attachments/assets/e7bb0b4a-a224-430a-9cf5-8bf1770a9d98)


FULL SUBTRACTOR


![Screenshot (43)](https://github.com/user-attachments/assets/5d8fda80-e3e4-4b95-b330-aeff68a18c70)



**Output Timing Waveform**


FULL ADDER


![Screenshot (42)](https://github.com/user-attachments/assets/d1bc1d20-d1f1-4fcc-85fb-e0f9caee1681)



FULL SUBTRACTOR


![Screenshot (44)](https://github.com/user-attachments/assets/424e556e-5a3e-47ea-9dfa-301c71557730)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



