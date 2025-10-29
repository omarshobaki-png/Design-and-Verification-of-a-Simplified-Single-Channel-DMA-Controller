# DMA Controller (Direct Memory Access)

## Overview
This module implements a **Direct Memory Access (DMA) Controller** in Verilog as part of the UART-to-Memory transfer system.  
The DMA controller autonomously transfers data between peripherals and memory **without continuous CPU involvement**, improving performance and reducing latency.

## Design Description
The DMA is responsible for:
- Reading data from the UART buffer when available  
- Writing data into sequential memory addresses  
- Tracking the number of remaining transfers  
- Signaling when the transfer operation is complete through a **done** flag  

The design is implemented using a **Finite State Machine (FSM)** that transitions through stages of reading, writing, and completion.

## Files
- `dma.v` — Main Verilog module implementing the DMA controller logic  
- `dma_tb.v` — Testbench for verifying DMA behavior and control timing  

## Simulation and Verification
The DMA module was simulated using **ModelSim**.  
The testbench verifies:
- Correct sequencing of read and write operations  
- Accurate address increments for memory writes  
- Proper handling of the done signal after the last transfer  

Waveform analysis confirms proper coordination between the DMA, UART, and Memory modules, ensuring reliable data flow.

## Key Features
- Fully automated data transfer control  
- FSM-based operation with clear state transitions  
- Supports parameterized data and address widths  
- Generates completion and control signals for system synchronization  

## Tools Used
- Intel Quartus Prime – for Verilog compilation  
- ModelSim – for simulation and waveform analysis  

## Result
The DMA successfully manages UART-to-Memory data transfers, maintaining proper timing and signaling while offloading repetitive tasks from the CPU.
