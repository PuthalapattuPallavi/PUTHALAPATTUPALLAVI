# Configurable Accelerator IP on OpenFrame

## Project Overview

This project implements a **Configurable Hardware Accelerator** for **Matrix Multiplication / FIR Filtering**, designed to be integrated into the **OpenFrame user area**. The accelerator supports **parameterizable bit-widths** and a configurable number of **MAC (Multiply-Accumulate) units**, allowing trade-offs between **throughput, latency, and hardware resource utilization**.

It demonstrates an **M.Tech-level hardware design** project combining **RTL design, FSM control, and system-level performance analysis**.

---

## Features

- **Matrix Multiplier / FIR Filter:** Core computation engine.
- **Configurable MAC Units:** Adjust the number of parallel multiply-accumulate units.
- **Parameterizable Bit-Width:** Supports different operand widths for flexibility.
- **Hybrid Computation:** Mix of serial and parallel computation for optimal resource usage.
- **Done / Ready Flags:** Signals to indicate completion of computation.
- **OpenFrame Integration:** Fully compatible with the OpenFrame user area for simulation and verification.

---

## Project Motivation

Matrix multiplication and FIR filtering are **key operations in DSP, AI, and scientific computing**. Hardware acceleration of these operations allows:

- Faster computation compared to software implementations.
- Lower power consumption.
- Resource-efficient designs by optimizing MAC unit usage.
- Exploration of **parameterized hardware architectures** suitable for real-time applications.

---

## Architecture

### Core Design

- **MAC Array:** Configurable number of multiply-accumulate units.
- **Shift Registers:** For serial input/output handling.
- **FSM Controller:** Orchestrates data flow, computation, and completion signaling.
- **Parameterization:** Width of operands and number of MACs defined via parameters.

### Data Flow

1. Input matrices (or FIR coefficients and data) are loaded serially or in parallel depending on configuration.
2. MAC units perform multiplication and accumulation.
3. Result is stored in internal registers or output buffers.
4. Done flag is raised when computation completes.

---

## Getting Started

### Prerequisites

- Verilog/SystemVerilog RTL files.
- Simulation tools: **ModelSim**, **Vivado**, or **Icarus Verilog**.
- OpenFrame harness for integration.

### Running Simulations

1. Clone the repository:
   ```bash
   git clone https://github.com/PuthalapattuPallavi/Configurable-Accelerator-IP
   cd Configurable-Accelerator-IP


