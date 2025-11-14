# simple-processor
Simple 16-bit Processor in Verilog

Instruction format is 32-bit:

[31:27] op_type

[26:22] destreg

[21:17] srcreg

[16]    immediate?

[15:11] srcreg2

[10:0]  unused

if immediate:

[15:0]  immediate value

Instructions in inst_data.mem for testbench are as follows:
MOV R0, 5
MOV R1, 6
MOV R2, 0
MOV R3, 6
ADD R2, R2, R0
SUB R3, R3, 1
JNZ 4
MOV R5, R2
HALT

Result should be 30 in GPR5
