AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

 Equipments Required:
 Hardware – PCs, Cyclone II , USB flasher
 Software – Quartus prime
 Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

 Half Subtractor Full Subtractor
 Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

 Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

Procedure



Write the detailed procedure here 


 Program:
 
HALF SUBTRACTOR:

module HalfSub(a,b,difference,borrow);

input a,b;

output difference,borrow;

assign difference=(a^b);

assign borrow=(~a&b);

endmodule

FULL SUBTRACTOR:

module FullSub(a,b,c,difference,borrow);

input a,b,c;

output difference,borrow;

assign borrow=(~a&(b^c)|(b&c));

assign difference=(a^b^c);

endmodule


Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: JENIFER.A

RegisterNumber:  22009141

LOGIC GATES

![logic gate sub](https://user-images.githubusercontent.com/121572543/211150649-d7a5adc8-9049-4874-9287-ea38d1416f7d.png)




 Output:
 
 Truthtable

HALF SUBTRACTOR

![SUB 1](https://user-images.githubusercontent.com/121572543/211150407-66701961-4c9a-4446-863a-a0c6ada5caeb.png)


FULL SUBTRACTOR

![SUB 2](https://user-images.githubusercontent.com/121572543/211150416-7ab43516-a7e9-4b67-9261-24037682199e.png)


 RTL realization
 
 HALF SUBTRACTOR
 ![RTL1](https://user-images.githubusercontent.com/121572543/211150437-b4cdf6a3-6891-4e3e-afbb-25fd13b9756a.png)

 FULL SUBTRACTOR
 
![RTL2](https://user-images.githubusercontent.com/121572543/211150521-c4f3bb32-7fd1-4ddf-9aaa-a02816f5929a.png)


 Timing diagram 
 
HALF SUBTRACTOR

![timing diagram1](https://user-images.githubusercontent.com/121572543/211150545-46361478-65d1-45a1-8712-af9e59d3152e.png)

FULL SUBTRATOR

![timing diagram2](https://user-images.githubusercontent.com/121572543/211150568-370d1414-d301-459e-b08d-2edbc0a78c2f.png)


 Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
