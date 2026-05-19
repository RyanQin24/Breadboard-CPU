# Breadboard-CPU
This is my Breadboard CPU made from discrete logic gates. This CPU has a 4-bit data width and a 8-bit (Byte) instruction width. The CPU can perform instruction jump, load immediate to register, and 
Add/Subtraction arithmetic between 4 registers.

<img width="3773" height="1636" alt="20260502_204924" src="https://github.com/user-attachments/assets/50cdb289-010a-4f2b-b8e8-d634571a653e" />

&nbsp;

Here is the high-level diagram:

<img width="865" height="1002" alt="Screenshot 2026-05-19 120219" src="https://github.com/user-attachments/assets/a7ab9c89-e007-40d0-b78d-57242fdde6ae" />


** **
**Below, it documents the architecture and the design steps taken to build this Breadboard CPU**

**_1) ISA designing_**

Since the hardware design/implementation is very dependent on the ISA, this is definitely my first step!

Here are the planned 4 instructions that this CPU runs:

<img width="713" height="390" alt="Screenshot 2026-05-19 071219" src="https://github.com/user-attachments/assets/1394da21-2aac-4883-89bc-e89f0d153301" />

_Note: XX denotes don't care and PC denotes absolute value that PC will be set after running the jump instruction._

** **

**_2) PC, reset, and clock design_**

After a proper ISA is planned, the next fundamental challenge is the PC and the clock.

Below, it shows my initial schematic to my variable frequency square wave Clock generator:



**_3) Register File design_**

Beside the register IC, the register file also contains control circuits for the mux used to direct the input data.

Note: for the case of R0 (Register 0 with value always being 0), it is a special case. Instead of using physical registers, R0 is effectively always zero by wiring ground to R0 input on ALU's mux.

**_4) ALU design_**
The ALU is the component doing Adding and subtracting.

**_5) Control Circuit design_**

Control circuit is required to ensure registers (PC and data) transition to the right state. Below, I specify how the control circuit handles 

**_6) Programming_**
I have written a test program to test out the CPU.

The program is written below with instruction encoded according to my ISA in part 1).

**_7) Conclusion_**
