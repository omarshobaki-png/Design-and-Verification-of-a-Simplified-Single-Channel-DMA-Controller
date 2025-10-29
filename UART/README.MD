# UART Module (Universal Asynchronous Receiver Transmitter)

## Overview
This module implements a simplified **UART** in Verilog for data transfer within the DMA-based communication system.  
Instead of performing full serial transmission, it provides buffered byte-level access to focus on verifying data transfer mechanisms.

## Design Description
The UART module:
- Outputs a byte of data when the DMA asserts a read enable signal  
- Operates on the system clock with synchronized output timing  
- Generates valid data outputs one clock cycle after read requests  
- Simplifies UART behavior by omitting baud rate generation and framing  

This abstraction allows efficient simulation and testing of data movement between UART, DMA, and Memory modules.

## Files
- `uart.v` — Main Verilog module implementing UART buffer and control logic  
- `uart_tb.v` — Testbench used for simulating UART data generation and timing  

## Simulation and Verification
The UART module was simulated using **ModelSim** to confirm:
- Correct output timing relative to DMA read enable signals  
- Sequential delivery of data bytes from the UART buffer  
- Reliable coordination with the DMA controller  

Simulation results verified proper byte delivery to the DMA for each read cycle.

## Key Features
- Simplified buffered UART model for simulation efficiency  
- Compatible with DMA-controlled read operations  
- Fully synchronous with the system clock  
- Supports customizable data width  

## Tools Used
- Intel Quartus Prime – for HDL compilation  
- ModelSim – for functional simulation and waveform validation  

## Result
The UART module successfully provides reliable data output to the DMA controller, enabling seamless UART-to-Memory transfers within the complete Verilog system.
