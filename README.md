# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**
**Half adder:**
![434143307-48037410-d19c-421f-b1b9-be7405247d87](https://github.com/user-attachments/assets/1301c9c2-02fe-4208-a5a1-01b130a5aa40)

**Half subtractor:**
![434143391-f161ee04-4837-42b2-bc16-cb4c2b600f6a](https://github.com/user-attachments/assets/3d529eb8-9936-4b2a-aa11-05c6b55ad6c4)


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Chiiradeep R
RegisterNumber: 212224240028
*/
~~~
         module de(a,b,sum_a,carry_a,diff_s,borr_s);
         input a,b;
         output sum_a,carry_a,diff_s,borr_s;
         assign sum_a=a^b;
         assign carry_a= a&b;
         assign diff_s=a^b;
         assign borr_s=(~a&b);
         endmodule
~~~

**RTL Schematic**
![434127116-c1f0c226-8631-43d2-8af3-0921a92c746e](https://github.com/user-attachments/assets/8b3916f9-47d8-4d4e-812a-9b53c07c9241)


**Output/TIMING Waveform**
![434127153-abe937bd-e340-4953-b0e4-fa7670132b3f](https://github.com/user-attachments/assets/4e4a3998-4a91-4a31-ab34-e040a350d71b)

**Result:**
Thus, a half adder and half subtractor circuit has been implemented and it's truth table has been verified.
