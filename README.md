NAME : ALIYA SHEEMA N
REGISTER NO : 23005529
# Exp 02 Implementation of Half Adder and Full Adder circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### Program
### Half Adder
module halfadder(sum,a,b,carry);

input a,b;

output sum,carry;

xor (sum,a,b);

and (carry ,a,b);

endmodule 

### RTL realization
![ha rtl](https://github.com/23005529/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139842207/89cd67ee-8a78-4a47-91e0-b286abafda32)

### TRUTH TABLE 
![ha tt](https://github.com/23005529/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139842207/5518341a-dfdd-4eda-99b5-3ee416500f7d)
### WAVEFORM
![wf ha](https://github.com/23005529/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139842207/3457e5e9-786f-4d98-b56b-6bb7cdd1d4ab)

### Program
### Full Adder
module fulladder(a,b,c,sum,carry);

input a,b,c;

output sum, carry;

xor(sum,a,b,c);

assign carry=a&b | b&c | a&c;

endmodule 
### RTL realization
![fa rtl](https://github.com/23005529/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139842207/0e710467-2979-4b4d-ba96-9f9519c02e63)
### TRUTH TABLE 
![fa tt](https://github.com/23005529/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139842207/ee508db8-9b21-4d77-9a06-76c3d7a0d69c)
### WAVEFORM
![wf fa](https://github.com/23005529/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139842207/6b778ad7-807a-4955-aa1b-475f7997b39f)
### Result:
Thus the given full adder and half adder are verified using verilog programming.

