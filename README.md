NAME: LOKESH M

REFERENCE NUMBER: 23001615
# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

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


#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)



### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
# Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
```
module exp3(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```



# RTL realization:


![halfadRTL](https://github.com/Lokesh23001615/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979337/4ae908b1-830f-4624-96b6-c6e9fcb3f45c)

# TIMING DIAGRAM:

![halfadtt (2)](https://github.com/Lokesh23001615/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979337/965e5f54-193b-4fc0-a623-8f05980aef3a)

# Truth table:


![halfadtt](https://github.com/Lokesh23001615/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979337/e8a117af-5c55-411f-a33f-29210a2648f3)

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

#### Figure -02 FULL ADDER 

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)


# Program:
```
module exp3(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule
```
# RTL Realisation:

![fullad](https://github.com/Lokesh23001615/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979337/00bba758-daef-462e-bc23-9c367de2bbde)

# TIMING DIAGRAM:

![fulladder](https://github.com/Lokesh23001615/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979337/313a6d33-0811-46b6-966a-4edf189022b9)

# Truth Table: 

![fulladtt](https://github.com/Lokesh23001615/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979337/7ff0e16f-f33f-4a6d-a371-68671980eb4a)


### Result:

Thus the given logic functions are implemented and their operations are verified using verilog programming
