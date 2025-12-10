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
**Full Adder**


<img width="429" height="395" alt="image" src="https://github.com/user-attachments/assets/c28189bf-c94b-4308-8a5c-e958f20370bb" />


**Full Subtractor**


<img width="438" height="393" alt="image" src="https://github.com/user-attachments/assets/df142bfb-4555-4e2f-b034-c2feda8ceaab" />


**Procedure**

1.Type the program in Quartus software.
2.Compile and run the program. 
3.Generate the RTL schematic and save the logic diagram.
4.Create nodes for inputs and outputs to generate the timing diagram. 
5.For different input combinations generate the timing diagram.

**Program:**
Full Adder
```
module full_adder (
    input  wire a, b, cin,   // Inputs
    output wire sum, carry   // Outputs
);

    // Logic equations
    assign sum   = a ^ b ^ cin;                  // XOR for sum
    assign carry = (a & b) | (b & cin) | (a & cin); // Majority function for carry

endmodule
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
*/
<img width="857" height="243" alt="image" src="https://github.com/user-attachments/assets/059e9e3c-0ec1-4f0d-a78d-858f234b9183" />

Full Subtractor
```
module full_subtractor (
    input  wire a, b, bin,       // Inputs
    output wire diff, borrow     // Outputs
);

    // Logic equations
    assign diff   = a ^ b ^ bin;                  // Difference
    assign borrow = (~a & b) | (~(a ^ b) & bin);  // Borrow logic

endmodule
```
Program to design a full adder and full subtractor circuit and verify its truth table in quartus using Verilog programming.
<img width="717" height="250" alt="image" src="https://github.com/user-attachments/assets/a6d29930-d873-4fc3-b164-84a8842f3dd6" />


Developed by:LOHINI S
RegisterNumber:25015038

**RTL Schematic**
Full Adder:

<img width="996" height="761" alt="image" src="https://github.com/user-attachments/assets/4478863e-e5aa-4b24-a2cd-6716d5cc9437" />

Full Subtractor:
<img width="1003" height="641" alt="image" src="https://github.com/user-attachments/assets/e9799e26-a695-4166-8470-f8bb4605e975" />


**Output Timing Waveform**
Full Adder

<img width="1300" height="335" alt="image" src="https://github.com/user-attachments/assets/40d13a55-3d35-4941-bfb7-25714aecd630" />



Full Subtractor

<img width="1315" height="347" alt="image" src="https://github.com/user-attachments/assets/b4223102-ad90-40a9-a84e-b7aa68fd135b" />




**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



