# BOOLEAN_FUNCTION_MINIMIZATION

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

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. */

```
Developed by: Pooja A
RegisterNumber:212222240072
```

```
//Program to compute the function f1=a'b'c'd'+ac'd'+b'cd'+a'bcd+bc'd
//f2=xy'z+x'y'z+w'xy+wx'y+wxy
// simplify the logic using Boolean minimization/k map 
//compute f2 and write verilog code for f2 as like f1
module ex2(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
and(s,ydash,z);
and(t,x,y);
and(u,w,y);
or(f2,s,t,u);
endmodule//type code for f2 as like f1
```

**RTL realization**

**Output:**
![316221728-6cff111c-1347-40d2-9065-30789ccfdde0](https://github.com/poojaanbu0/BOOLEAN_FUNCTION_MINIMIZATION/assets/119390329/23942ee3-7e6f-437d-9383-848f59cbee47)


**RTL**
![316221743-f8821bf3-7cd6-49e5-8e6d-f583923eed10](https://github.com/poojaanbu0/BOOLEAN_FUNCTION_MINIMIZATION/assets/119390329/6f42fafe-5f17-43ed-b2c3-1491da0d2793)

**Logic symbol & Truthtable:**
![319535984-1320c49e-13f6-45f6-a28d-63a4c5fde8cd](https://github.com/poojaanbu0/BOOLEAN_FUNCTION_MINIMIZATION/assets/119390329/39dc7f2f-a568-4330-9cae-86e0fc22642e)

![319536399-2b76ba1f-67ec-4969-b9c6-8f0b975f551f](https://github.com/poojaanbu0/BOOLEAN_FUNCTION_MINIMIZATION/assets/119390329/ea4ef1eb-7f63-4324-8ccb-4cdc4b889739)



**Timing Diagram**

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

