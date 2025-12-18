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
<img width="1390" height="790" alt="Screenshot 2025-12-18 190223" src="https://github.com/user-attachments/assets/a8ace60b-209f-4c7d-b17f-b35a319190a2" />
<img width="826" height="416" alt="Screenshot 2025-12-18 190305" src="https://github.com/user-attachments/assets/4795a4d2-42f1-45e1-a16c-9ec3a459d036" />

**Output Timing Waveform**
<img width="1039" height="522" alt="Screenshot 2025-12-18 190250" src="https://github.com/user-attachments/assets/3041cdc5-bfa6-4d33-ba6a-918624398861" />
<img width="1036" height="460" alt="Screenshot 2025-12-18 190327" src="https://github.com/user-attachments/assets/e59b1744-5eff-406a-adba-3c9f3c4ffda9" />

**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
