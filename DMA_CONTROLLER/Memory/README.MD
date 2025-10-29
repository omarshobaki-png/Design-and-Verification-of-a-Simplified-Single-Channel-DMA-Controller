# Memory Module

## Overview
This module implements a **synchronous Memory unit** in Verilog, designed to store data transferred by the DMA controller during UART-to-Memory communication.  
It supports both read and write operations with addressable memory cells, ensuring accurate data storage and retrieval.

## Design Description
The Memory module:
- Stores incoming data from the DMA controller  
- Allows controlled read and write access  
- Uses an address input to specify the data location  
- Operates synchronously with the system clock  

The design emphasizes timing precision and data integrity, ensuring correct operation under all transfer conditions.

## Files
- `memory.v` — Main Verilog file defining the memory structure and control logic  
- `memory_tb.v` — Testbench for simulating and verifying read/write operations  

## Simulation and Verification
The Memory module was tested using **ModelSim** to verify:
- Correct write and read sequences  
- Data stability during access cycles  
- Proper address decoding and synchronization with the clock signal  

Simulation waveforms confirm correct data storage and retrieval at each memory address during DMA-controlled transfers.

## Key Features
- Synchronous read/write behavior  
- Parameterized address and data width  
- Reliable data storage with timing synchronization  

## Tools Used
- Intel Quartus Prime – HDL synthesis and design  
- ModelSim – Functional simulation and waveform analysis  

## Result
The Memory module successfully supports the DMA controller by storing incoming UART data and providing stable access to stored values during operation.
