# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full SubtraCtor circuit and verify its truth table in Quartus using Verilog programming.

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

**FULL ADDER**

![Screenshot 2025-01-02 200923](https://github.com/user-attachments/assets/c5bf6725-3d6a-4908-9485-86e669acfee5)

**FULL SUBSTRACTOR**

![Screenshot 2025-01-02 201003](https://github.com/user-attachments/assets/2991bfef-c2bf-4a3f-a527-077d6715c229)

**Procedure**

write the detailed procedure here 

1 type the program in quartes software.

2 compile and run rhe program .

3 generate the RTL schematic and save the logic diagram.

4 create nodes for inputs and outputs to generate the timing diagram .

5 for different input combinations generate the timing diagram

**Program:**

**FULL ADDER**

module fulladder(

input a,b,c,

output sum,carry);

wire w1,w2,w3;

assign sum=a^b^c; assign w1=a&b;

assign w2=b&c;

assign w3=c&a;

assign carry=w1|w2|w3;

endmodule

**FULL SUBRACTOR**

module fullsub(a,b,c,diff,borr);

input a,b,c;

output diff,borr;

wire w1,w2,w3,w4,w5,w6;

xor g1(diff,a,b,c);

and g2(w4,w1,b);

and g3(w5,w1,b);

nd g4(w6,b,c);

or g5(borr,w4,w5,w6);

endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:H.VEDHANTH RegisterNumber: */24003775

**RTL Schematic**

**FULL ADDER**

![Screenshot 2025-01-02 200413](https://github.com/user-attachments/assets/259720a4-c2cb-4b6b-bec9-85e1ba03b43f)

**FULL SUBSTRACTOR**

![Screenshot 2025-01-02 200450](https://github.com/user-attachments/assets/6587962a-0ae3-4095-8789-32d1def54bfd)

**Output Timing Waveform**

**FULL ADDER**

![Screenshot 2025-01-02 200137](https://github.com/user-attachments/assets/43cf8d06-273b-45e9-9c8c-e8a3dd824740)

**FULL SUBSTRACTOR**

![Screenshot 2025-01-02 200210](https://github.com/user-attachments/assets/8aa59c14-da6e-4155-8935-d80a573cb3c0)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.

