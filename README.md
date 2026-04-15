# RISC-V 32-bit Pipelined Processor (Verilog)

## Overview

This project implements a **32-bit RISC-V processor with a 5-stage pipeline architecture** using **Verilog HDL**.
The design follows the standard RISC-V instruction execution flow and demonstrates how pipelining improves processor performance by allowing multiple instructions to be processed simultaneously.

The processor supports a subset of **RV32I instructions** and includes modular components such as ALU, control unit, register file, memory modules, and pipeline registers.

---

## Architecture

The processor is designed using a **5-stage pipeline**:

1. **Instruction Fetch (IF)**

   * Fetch instruction from Instruction Memory
   * Program Counter (PC) increments by 4

2. **Instruction Decode (ID)**

   * Decode instruction
   * Read source registers from Register File
   * Generate control signals

3. **Execute (EX)**

   * Perform arithmetic or logical operations using the ALU
   * Calculate branch target address

4. **Memory Access (MEM)**

   * Read or write data from/to Data Memory

5. **Write Back (WB)**

   * Write the result back to the Register File

---

## Pipeline Stages

| Stage | Description                               |
| ----- | ----------------------------------------- |
| IF    | Instruction fetch from memory             |
| ID    | Instruction decoding and register reading |
| EX    | ALU operation and branch calculation      |
| MEM   | Data memory access                        |
| WB    | Write results back to registers           |

---

## Implemented Modules

The processor consists of several hardware modules:

* Program Counter (PC)
* PC Adder
* Instruction Memory
* Register File
* Control Unit
* ALU Control
* Arithmetic Logic Unit (ALU)
* Immediate Generator
* Data Memory
* Pipeline Registers (IF/ID, ID/EX, EX/MEM, MEM/WB)

---

## Instruction Flow

Instruction execution follows this datapath:

Instruction Memory → Register File → ALU → Data Memory → Register File

Each instruction progresses through the pipeline stages in consecutive clock cycles.

---

## Supported Instructions

Example instructions implemented:

* ADD
* SUB
* AND
* OR
* ADDI
* LW
* SW
* BEQ

---

---

## Simulation

The design can be simulated using:

* ModelSim
* Vivado


---

## Learning Outcomes

This project demonstrates:

* CPU datapath design
* Pipeline processor architecture
* Hardware design using Verilog HDL
* Control signal generation
* Instruction level parallelism

---

## Author

Rohit Baskey

---


