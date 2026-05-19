# Breadboard-CPU
This is my Breadboard CPU made from discrete logic gates. This CPU has a 4-bit data width and a 8-bit (Byte) instruction width. The CPU can perform instruction jump, load immediate to register, and 
Add/Subtraction arithmetic between 4 registers.

<img width="3773" height="1636" alt="20260502_204924" src="https://github.com/user-attachments/assets/50cdb289-010a-4f2b-b8e8-d634571a653e" />

** **
**Below, it documents the architecture and the design steps taken to build this Breadboard CPU**

**_1) ISA designing_**

This was my first step, as the hardware design is very dependent on the ISA.

Here are the planned 4 instructions that this CPU runs:

<img width="713" height="390" alt="Screenshot 2026-05-19 071219" src="https://github.com/user-attachments/assets/1394da21-2aac-4883-89bc-e89f0d153301" />

_Note: XX denotes don't care and PC denotes absolute value that PC will be set after running the jump instruction._


**_2) PC, reset, and clock design_**

After a proper ISA is planned, the next fundamental challenge is the PC and the clock.

Below, it shows my initial schematic to my variable frequency square wave Clock generator:



**_3) Register File design_**
Beside the register IC, the register file also contains control circuits for the mux used to direct the input data. Since enable required an extra input f

**_4) ALU design_**
The ALU is the component doing Adding and subtracting.

**_5) Control Circuit design_**
Note: while my ISA makes identifying registers easy while ALU select input is just a function of one Opcode bit, control circuit is still used for controlling the data input of the register files.

**_6) Programming_**
I have written a test program to test out the CPU.

The program is as follows

**_7) Conclusion_**
