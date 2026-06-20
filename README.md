# Asynchronous FIFO in Verilog

## Overview
This project implements an Asynchronous FIFO using Verilog.

The design supports data transfer between two different clock domains using:

- Binary read/write pointers
- Gray code conversion
- Two-stage synchronizers
- Full and empty flag generation
- Dual-port memory architecture

## Features

- Parameterized data width
- Parameterized FIFO depth
- Independent write and read clocks
- Clock Domain Crossing (CDC) handling
- Gray code pointer synchronization
- Full and Empty status flags

## Parameters

| Parameter  |     Description    |
|------------|--------------------|
| DATA_WIDTH | Width of FIFO data |
| ADDR_WIDTH | FIFO address width |

FIFO Depth:

```text
Depth = 2^ADDR_WIDTH
```

## Files

```text
rtl/async_fifo.v      -> FIFO Design
tb/async_fifo_tb.v    -> Testbench
```

## Verification

The testbench verifies:

- FIFO reset operation
- Data write operation
- Data read operation
- Full flag generation
- Empty flag generation
- Asynchronous clock operation

## Concepts Used

- Clock Domain Crossing (CDC)
- Gray Code Counters
- Two Flip-Flop Synchronizers
- Asynchronous FIFO Architecture
- RTL Design and Verification