# logic-gates
AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

Equipments Required:
Hardware – PCs, Cyclone II , USB flasher Software – Quartus prime Theory Adders are digital circuits that carry out addition of numbers.

Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin
![163552156-a13e5a56-c638-4110-97d9-8896907c8d25](https://user-images.githubusercontent.com/123359969/214290158-52984a11-9890-43a7-b6cb-1e8b0a4b236c.png)


Figure -01 HALF ADDER
![163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d](https://user-images.githubusercontent.com/123359969/214290215-87062a33-26ed-4e77-a3ca-ce88dd0bdcb7.png)


Figure -02 FULL ADDER
Procedure
Connect the supply (+5V) to the circuit Switch ON the main switch If the output is 1, then the led glows.

Program:

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: santhosh L

RegisterNumber: 22008479

Half Adder Verilog Code:
module half_adder(a, b, s, c);
input a, b;
output s, c;
xor(s, a, b);
and(c, a, b);
endmodule


Full Adder Verilog Code:

module full_adder(x, y, z, s, c, x1, x2, x3, x4);
input x, y, z;
output s, c, x1, x2, x3, x4;
xor(x1, x, y);
xor(s, x1, z);
and(x3, x, y);
and(x4, x1, z);
or(c, x3, x4);
endmodule

Logic symbol & Truthtable RTL realization

Output:
RTL
![half_adder_rtl](https://user-images.githubusercontent.com/123359969/214290439-6d3e4d25-26e5-498e-a47c-fdef372858c9.png)

![full_adder_rtl](https://user-images.githubusercontent.com/123359969/214290465-5722206b-c0e8-4ad3-baa0-c05aef83f06d.png)

TIMING DIAGRAM
![half_adder_timingdiag](https://user-images.githubusercontent.com/123359969/214290506-5716b583-9571-40bb-b411-728a728518a8.png)
![full_adder_timingdiag](https://user-images.githubusercontent.com/123359969/214290552-d5201700-cd31-46b6-a9d2-db33154ab5a1.png)

TRUTH TABLE
 ![half_adder_truthtable](https://user-images.githubusercontent.com/123359969/214290602-e0fcae72-e6d4-4fb4-a04d-243b582ef3ae.png)
![full_adder_truthtable](https://user-images.githubusercontent.com/123359969/214290625-47aa5415-299d-48d1-bbbc-2b39598cc52e.png)


Result:
Thus implementation of half adder and full adder circuit are verified
