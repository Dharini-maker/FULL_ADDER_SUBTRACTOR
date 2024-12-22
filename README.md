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

**Truth Table**

FULL ADDER

![238adacf-3dcf-48c8-9f9f-ef3c2e0b7296](https://github.com/user-attachments/assets/814a446d-1263-44fd-a399-867a31c4f6f8)

FULL SUBTRACTOR

![a30cffd5-ae2f-421e-8765-ec29a26253af](https://github.com/user-attachments/assets/95593e4d-f868-4f42-aa66-5b21c92fc7ae)


**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:S.Dharini

RegisterNumber:24002206


i)FULL ADDER

module fa(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule

ii)FULL SUBTRACTOR

module fs(a,b,bin,diff,borr);

input a,b,bin;

output diff,borr;

assign difference= (a ^ b^bin);

assign borrow= (( ~a & b)|((~a^b)&bin));

endmodule


**RTL**

Full adder

![exp4 fa logic gate](https://github.com/user-attachments/assets/596ccbb3-e7c0-45a8-96b4-40aa4c0782d5)

Full subtractor

![exp4 fs logic gate](https://github.com/user-attachments/assets/e8f4efff-3549-42d3-b9d3-3f8dc382f915)


**Output**

Full adder

![exp4 fa op](https://github.com/user-attachments/assets/d5c5883c-89da-4516-82b8-73a3b7b0f5f1)

Full subtractor

![exp4 fs op](https://github.com/user-attachments/assets/66d7984d-ca91-4d59-b29d-64ac2e676104)




**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



