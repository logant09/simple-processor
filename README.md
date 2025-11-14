# simple-processor
Simple 16-bit Processor in Verilog

Instruction format is 32-bit:
 IR [31:27]  [26:22]  [21:17]  [16]  [15:11]  [10:0]
    op_type  destreg  srcreg   imm?  srcreg2  unused
                       if immediate: |<----imm----->|

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
