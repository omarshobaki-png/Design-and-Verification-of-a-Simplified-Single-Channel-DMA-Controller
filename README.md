# Verilog Hardware System – DMA, Memory, and UART Modules

**Course:** ENCS3310 – Advanced Digital Systems Design  
**Project Title:** Design and Verification of a Simplified Single-Channel DMA Controller for UART-to-Memory Data Transfer  
**Prepared by:**  
- Saifeddin Saleh — 1231474  
- Omar Shoubaki — 1230329  
**Instructor:** Dr. Ayman Hroub  
**Date:** 12/8/2025  

## Project Overview
This project implements and verifies a simplified single-channel Direct Memory Access (DMA) controller that transfers data from a UART peripheral to memory without continuous CPU supervision.  
All modules were designed and simulated in Verilog, following a modular hardware architecture that includes:
- A simplified UART module (data source)  
- A Memory module (data destination)  
- A DMA controller that handles data movement automatically  

Each module is verified with an individual testbench and observed using ModelSim simulation waveforms.


## Repository Structure

This repository contains three main Verilog modules, each in its own folder, along with a final project report.

| Module | Description | Link |
|---------|--------------|------|
| **DMA Controller** | Handles data transfer between UART and Memory automatically using FSM logic. | [View DMA Module](./DMA/README.md) |
| **Memory Module** | Implements synchronous memory for storing transferred data. | [View Memory Module](./Memory/README.md) |
| **UART Module** | Provides buffered data to the DMA for transfer, simulating serial communication. | [View UART Module](./UART/README.md) |
| **Project Report** | Full technical documentation of the project design, simulation, and results. | [Download PDF](./Project_Report_1231474_1230329.pdf) |


## Simulation and Verification
Each module includes its own testbench:
- `uart_tb.v` – verifies buffered byte output behavior  
- `memory_tb.v` – validates memory read/write functionality  
- `dma_tb.v` – simulates the full UART-to-Memory data transfer sequence  

Simulation waveforms confirm:
- Correct timing between read and write operations  
- Accurate data transfer from UART to memory  
- Proper signaling of the done flag after all bytes are moved  

## Tools Used
-Quartus II 9.0
- Logisim – (Optional) for logic visualization  

## Results
- The integrated system successfully transfers data from UART to memory automatically.  
- Simulation confirmed correct timing, sequencing, and data integrity.  
- The done signal asserted correctly upon completion of data transfer, indicating proper FSM operation.  

## Conclusion
The project demonstrates a functional and efficient hardware-based data transfer system that reduces CPU load and ensures predictable timing.  
By combining UART, Memory, and DMA modules into one cohesive design, it highlights the value of modular Verilog development, FSM control logic, and simulation-driven verification in advanced digital systems design.
