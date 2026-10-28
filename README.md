# apb-protocol-uvm
UVM-based APB 3.0 Slave Design and Protocol Verification using uvm

# APB 3.0 Slave — UVM-Based Protocol Verification

## 📌 Project Overview
This project focuses on the design and functional verification of a 32-bit APB Slave based on the AMBA APB protocol specifications using Verilog HDL, SystemVerilog, and UVM.

A UVM-based verification environment was developed to generate, drive, monitor, and check APB transactions. The project verifies normal read/write operations, protocol timing, wait states, and error responses.

## 🎯 Project Objectives
- Implement a 32-bit APB Slave.
- Develop a reusable UVM-based verification environment.
- Verify APB setup and access phases.
- Check read/write transactions and wait-state behavior.
- Verify `PREADY` and `PSLVERR` responses.
- Compare expected and actual responses using a scoreboard.

## 🛠️ Technologies and Tools
- HDL: Verilog HDL, SystemVerilog
- Verification Methodology: UVM
- Simulation: Synopsys VCS
- Waveform Debugging: Synopsys Verdi
- Protocol: AMBA APB 3.0

## 🏗️ Verification Environment
The UVM testbench is organized around the following components:
- Sequence Item: Defines APB transaction fields.
- Sequence: Generates APB read/write transactions.
- Sequencer: Sends transactions to the driver.
- Driver: Drives APB signals to the DUT.
- Monitor: Observes APB bus activity.
- Agent: Groups the driver, monitor, and sequencer.
- Environment: Integrates the verification components.
- Scoreboard: Compares expected and actual transaction responses.

## 🔌 APB Interface Signals
| Signal | Description |
|---|---|
| `PCLK` | APB clock |
| `PRESETn` | Active-low reset |
| `PADDR` | Address bus |
| `PSEL` | Selects the peripheral |
| `PENABLE` | Indicates the access phase |
| `PWRITE` | Selects read or write |
| `PWDATA` | Write data bus |
| `PRDATA` | Read data bus |
| `PREADY` | Indicates completion of a transfer |
| `PSLVERR` | Indicates a transfer error |

## 🧪 Verification Scenarios
1. APB setup and access phases.
2. Read transactions.
3. Write transactions.
4. Wait-state handling using `PREADY`.
5. Error-response handling using `PSLVERR`.
6. Scoreboard-based expected-versus-actual response checking.

## 🔍 Simulation and Debugging
Simulation and waveform debugging were performed using Synopsys VCS and Verdi to examine protocol behavior and transaction responses.

## 📁 Suggested Repository Structure
apb-protocol-uvm/
├── rtl/
│   └── apb_slave.sv
├── tb/
│   ├── apb_if.sv
│   ├── apb_pkg.sv
│   ├── apb_sequence_item.sv
│   ├── apb_sequence.sv
│   ├── apb_sequencer.sv
│   ├── apb_driver.sv
│   ├── apb_monitor.sv
│   ├── apb_agent.sv
│   ├── apb_scoreboard.sv
│   ├── apb_env.sv
│   └── apb_test.sv
├── sim/
├── screenshots/
└── README.md

## 👨‍💻 Author
Sarif Ahmad
M.Tech — Electronic Circuits & Systems Design  
Aligarh Muslim University (AMU)

- LinkedIn: https://www.linkedin.com/in/ahmad-a-68b500138/
- GitHub: https://github.com/sarif-ahmad-vlsi
