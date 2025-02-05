# VHDL Race Condition Example

This repository demonstrates a potential race condition in VHDL code.  The provided code appears correct at first glance, but under certain conditions, `data_out` might not reflect the intended value of `data_in`. The problem stems from the concurrent assignments of `internal_data` and `data_out` within a single clock cycle. If the value of `data_in` changes between these assignments, `data_out` will output the old or incorrect value.   A fix is provided in `bugSolution.vhdl` that uses a single assignment to prevent the race condition. 

## Setup

This example should be compatible with most VHDL simulators.

## Solution

The solution is provided in `bugSolution.vhdl` file, which demonstrate a simple way to fix the race condition using sequential signal assignment inside the process.