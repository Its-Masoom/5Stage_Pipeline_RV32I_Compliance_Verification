# RV32I
RV32I stands for RISC-V 32 bit Integer Type Processor. It is a basic processor in which other extensions i.e M(Multiplication), F(Floating Point) etc can be added.
The following types of instructions are supported by this processor:
- R Type (SLL, SLT, SLTU, SRL, SRA, ADD, SUB, XOR, OR, AND)
- I Type (ADDI, ANDI, ORI, XORI, SLTI, SLTIU, SLLI, SRLI, SRAI, LB, LH, LW, LBU, LHU, JALR)
- S Type (SB, SH, SW)
- U Type (LUI, AUIPC)
- J Type (JAL)
- B Type (BEQ, BNE, BLT, BGE, BLTU, BGEU)
> **Note:** RTL folder in this repo contains the design system verilog files for this processor.


## Compliance Testing

Compliance testing is **to check whether the processor under development meets the open RISC-V standards or not**. There are some tests available online that tries to cover the corner cases of all the instructions type listed above. These tests are contributed by open source community and are updated from time to time. In order to call your design to be fully complianced with RISC-V International Standards, one should pass all these tests successfully. These tests are available online by the name riscv-non-isa arch test.
> **Note:** riscv-arch-test folder in this repo contains the tests that we have passed by our processor.


## Framework for Testing
RISCOF framework is used which is a python based framework that enables testing of a RISC-V target (hard or soft implementations) against a standard RISC-V golden reference model using a suite of RISC-V architectural assembly tests.
> In our case, we have compared our designed RTL  with golden reference model named sail

## Result

Using riscof framework generates a report that shows how many tests are passed and how many failed. You can find the report in riscof_work/report.html. As the report is in HTML language so you need to render it for better view if you want to see the result or you can click the [link](https://htmlpreview.github.io/?https://github.com/Its-Masoom/5_Stage_Pipeline_RV32I_Compliance_Verification/blob/main/riscof_work/report.html) to see the rendered report.
