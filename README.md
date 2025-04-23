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

![WhatsApp Image 2025-04-23 at 10 38 24_a3aa9f2f](https://github.com/user-attachments/assets/4b36e56a-9505-491b-a66d-5f13f361c39a)


Full Subtractor

![WhatsApp Image 2025-04-23 at 10 39 07_5af7ccc1](https://github.com/user-attachments/assets/dabc813b-d32c-448f-812e-e57bf1a63456)



**Procedure**

1. Type the program in Quartus software.
 2. Compile and run the program.
 3. Generate the RTL schematic and save the logic diagram.
 4. Create nodes for inputs and outputs to generate the timing diagram.
 5. For different input combinations generate the timing diagram.

**Program:**

Full Adder
```
module exp4fa(a,b,cin,sum,carry);
 input a,b,cin;
 output sum,carry;
 assign sum=( (a ^ b)^cin);
 assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
```

Full Subtractor
```
module exp4fullsub(a,b,bin,difference,borrow);
 input a,b,bin;
 output difference,borrow;
 assign difference= ( (a ^ b)^bin);
 assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));
 endmodule
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.*/

Developed by:Jones Benedict A P

RegisterNumber:212224040142




**RTL Schematic**

Full Adder

![image](https://github.com/user-attachments/assets/e629169c-6f82-4cd4-8bed-ce92cf021fe9)

Full Subtractor


![image](https://github.com/user-attachments/assets/fd567c85-4157-4724-bbd2-bb10ebf85860)





**Output Timing Waveform**

Full Adder
![image](https://github.com/user-attachments/assets/aec20a4e-439f-47a6-84e3-87520e23736f)

Full Subtractor

![image](https://github.com/user-attachments/assets/08118640-ff08-4ba7-9297-34d9706837fe)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



