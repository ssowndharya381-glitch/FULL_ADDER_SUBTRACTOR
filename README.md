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

**Procedure**
1. Type the program in Quartus software.     
 2. Compile and run the program.   
 3. Generate the RTL schematic and save the logic diagram.   
 4. Create nodes for inputs and outputs to generate the timing diagram.   
 5. For different input combinations generate the timing diagram.   



**Program:**

module fa(a,b,cin,sum,carry);    
input a,b,cin;    
output sum,carry;    
assign sum=( (a ^ b)^cin);    
assign carry= ( (a & b)| ( cin &(a ^ b )));    
endmodule    

module fs(a,b,bin,difference,borrow);    
input a,b,bin;    
output difference,borrow;    
assign difference= ( (a ^ b)^bin);    
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));    
endmodule    

**RTL Schematic**
<img width="1669" height="719" alt="Screenshot 2025-12-03 145735" src="https://github.com/user-attachments/assets/c7f6a537-f342-48f0-9de6-27112eed0bb7" />

<img width="1563" height="721" alt="Screenshot 2025-12-03 145751" src="https://github.com/user-attachments/assets/b487edca-1943-4574-8f4c-858bd6dd8dee" />




**Output Timing Waveform**
<img width="1495" height="776" alt="Screenshot 2025-12-03 145815" src="https://github.com/user-attachments/assets/da8aea5f-eb20-4be7-9eeb-4c9e114c75f6" />

<img width="1476" height="763" alt="Screenshot 2025-12-03 145836" src="https://github.com/user-attachments/assets/97cd2c30-32ba-45a2-acda-54fe93c7e5a4" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



