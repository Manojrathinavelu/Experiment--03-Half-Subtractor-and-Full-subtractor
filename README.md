```
NAME: R MANOJ KARTHIK
REGISTER NO: 212222240061
```
# EXP-04-IMPLEMENTATION OF HALF SUBTRACTOR AND FULL SUBTRACTOR CIRCUIT

## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## EQUIPMENTS REQUIRED:
1. Hardware – PCs, Cyclone II , USB flasher
2. Software – Quartus prime
 
## THEORY:
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.
Half Subtractor Full Subtractor
### Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

### Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## PROCEDURE:
1. Connect the supply (+5V) to the circuit
2. Switch ON the main switch
3. If the output is 1, then the led glows.



## PROGRAM:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: R MANOJ KARTHIK
RegisterNumber: 212222240061

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
```

## TRUTH TABLE:
### HALF SUBTRACTOR
![image](https://github.com/Jaiganesh235/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/118657189/ff3bf8aa-be1d-4bc0-aeba-dbfb48b15787)


### FULL SUBTRACTOR
![image](https://github.com/Jaiganesh235/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/118657189/6308e249-bf33-4446-a3fb-743f4fa45410)


## RTL REALIZATION:
### HALF SUBTRACTOR
![image](https://github.com/Jaiganesh235/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/118657189/895e7f9d-d8bb-49d8-ba6a-c107f3c89115)

### FULL SUBTRACTOR
![image](https://github.com/Jaiganesh235/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/118657189/51bf96e2-c127-4392-b9aa-4f802622f27a)


## OUTPUT WAVEFORM:
### HALF SUBTRACTOR
![image](https://github.com/Jaiganesh235/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/118657189/0bff9ecc-05a8-4553-9fbc-c6cb7fff99dd)

### FULL SUBTRACTOR
![image](https://github.com/Jaiganesh235/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/118657189/d3b3213a-27e0-49f3-9a55-be7d65b9f57e)

## RESULT:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
