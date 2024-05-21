# 5-Stage Pipelined RISC-V Processor

## Introduction

This project involves the implementation of a single-cycle RISC-V processor, followed by the design of a 5-stage pipelined processor. The project culminates in the execution of a bubble sort algorithm on both processors, with a comparative analysis of their performance.

## Objectives

1. Convert bubble sort pseudocode to RISC-V assembly code and verify its execution on the Venus simulator.
2. Modify a single-cycle processor to support the bubble sort algorithm.
3. Pipeline the processor and test individual instructions to ensure functionality.
4. Implement hazard detection circuitry to handle data, control, and structural hazards using forwarding, stalling, and flushing techniques.
5. Compare the performance of the single-cycle processor with the pipelined processor in terms of execution time.

## Methodology

### Task 1: Bubble Sort Pseudocode to Machine Code

- **Implementation**: The bubble sort algorithm was implemented in RISC-V assembly and tested on the Venus simulator.
- **Single-Cycle Processor Modifications**: The lab 11 module was modified to include branch operations and support for the `funct3` bit of `bgt` and `blt` instructions. Additional changes were made to the ALU, data memory, and instruction memory to handle 64-bit operations and an 8-byte offset.

### Task 2: Pipelined RISC-V Processor

- **Pipeline Stages**: Added IF/ID, ID/EX, EX/MEM, and MEM/WB intermediary registers.
- **Data Passing**: Implemented a 3-to-1 MUX and forwarding unit for data passing within the pipeline. Integrated the forwarding unit with the hazard detection unit to optimize data transfer and minimize stalls.

### Task 3: Implementing Hazard Detection

- **Hazard Detection Circuitry**: Integrated circuits to handle data, structural, and control hazards. Implemented mechanisms to pause or flush the pipeline as needed.

### Task 4: Performance Comparison

- **Single-Cycle Processor**: Took approximately 300 ns for execution, with each instruction taking 1 ns.
- **Pipelined Processor**: Took approximately 800 ns for execution. The expected speedup was not achieved, resulting in 400 cycles.

## Challenges

- **Technical Support**: Limited technical support and time constraints posed significant challenges.
- **Instruction Support**: Adding support for `slli`, `blt`, and `bgt` instructions was complex and required significant effort.
- **Pipelining Logic**: Understanding and implementing pipelining logic was challenging.
- **Simulations**: Troubleshooting simulation errors and integrating branch conditions were particularly difficult.

## Conclusion

Despite numerous challenges, including limited technical support, time constraints, and the complexity of RISC-V processor design, we successfully created a pipelined processor capable of handling the majority of risks. The project provided valuable insights into processor design, hazard detection, and performance optimization.

## Repository Structure

- **/src**: Contains the source code for the single-cycle and pipelined processors.
- **/assembly**: Contains the RISC-V assembly code for the bubble sort algorithm.
- **/docs**: Contains documentation and reports related to the project.
- **/test**: Contains test benches and simulation files.
