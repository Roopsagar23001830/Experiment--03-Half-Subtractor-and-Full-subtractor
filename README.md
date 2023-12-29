# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure

1.Connect the supply (+5V) to the circuit.
2.Switch ON the main switch.
3.If the output is 1, then the led glows

Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: ROOP SAGAR S L

RegisterNumber:  212223040175
*/

1. Program to design a half subtractor:

module ex4(a,b,diff,borr);
input a,b;
output diff,borr;
assign diff=(a^b);
assign borr=((~a)&b);
endmodule 

2. Program to design a full subtractor:

module ex41(a,b,bin,diff,borr);
input a,b,bin;
output diff,borr;
assign diff=a^b^bin;
assign borr=((~a)&b)|(b&bin)|((~a)&bin);
endmodule 

## Output:

## Truthtable
HALF SUBTRACTOR:

![Screenshot 2023-12-29 145429](https://github.com/Roopsagar23001830/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/145972515/c08feeeb-6ee3-4aed-83eb-9f80685440f3)

FULL SUBTRACTOR:

![Screenshot 2023-12-29 145537](https://github.com/Roopsagar23001830/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/145972515/c24e79af-271a-446b-8630-879b000a7311)

##  RTL realization
HALF SUBTRACTOR:

![Screenshot 2023-12-29 145051](https://github.com/Roopsagar23001830/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/145972515/98cd5758-b666-4c3c-ba96-62698fec7fbd)

FULL SUBTRACTOR:

![Screenshot 2023-12-29 144023](https://github.com/Roopsagar23001830/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/145972515/b61e1e58-d83d-43c0-a580-e440fe1a2ffe)

## OUTPUT WAVEFORM
HALF SUBTRACTOR:

![Screenshot 2023-12-29 145229](https://github.com/Roopsagar23001830/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/145972515/d28df082-5a61-4f1c-8027-beaf957dbb07)

FULL SUBTRACTOR:

![Screenshot 2023-12-29 144244](https://github.com/Roopsagar23001830/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/145972515/8f2dd2c7-7bc5-416e-8c14-f4f77cda0958)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
