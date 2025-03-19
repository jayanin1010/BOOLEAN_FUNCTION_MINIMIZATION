### Name: Jayani N
### Reg no: 24900024


# EXP2-BOOLEAN FUNCTION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**


      module exp2(a,b,c,d,w,x,y,z,f1,f2);
      input a,b,c,d,w,x,y,z;
      output f1,f2;
      wire x1,x2,x3,x4,x5,y1,y2,y3,y4,y5;
      assign x1=((~a)&(~b)&(~c)&(~d));
      assign x2=(a&(~c)&(~d));
      assign x3=((~b)&(c)&(~d));
      assign x4=((~a)&(b)&(c)&(d));
      assign x5=(b&(~c)&(d));
      assign f1=x1|x2|x3|x4|x5;
      
      assign y1=(x&(~y)&(z));
      assign y2=((~x)&(~y)&z);
      assign y3=((~w)&x&y);
      assign y4=(w&(~x)&(y));
      assign y5=(w&x&y);
      assign f2=y1|y2|y3|y4|y5;
      endmodule





**Truth Table:**

![image](https://github.com/user-attachments/assets/bc0a0505-4fc0-40e9-96b3-26537bf9192a)

![image](https://github.com/user-attachments/assets/f2f7b7f7-0f23-47d2-b7f0-0f27c1d12948)



**RTL**

![Screenshot 2025-03-19 082859](https://github.com/user-attachments/assets/43e2bebb-c89c-454f-a2c9-3dfe274233d8)

![Screenshot 2025-03-19 084254](https://github.com/user-attachments/assets/77f305ee-4fa5-405b-9b70-aecde40ea7e3)



**Waveform**

![Screenshot 2025-03-19 084910](https://github.com/user-attachments/assets/ab529e03-3395-4706-ae73-2123dce2b70b)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

