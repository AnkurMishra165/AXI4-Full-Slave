AXI4 Full Slave Design with SystemVerilog Verification
Project Summary

This project implements a fully AXI4-compliant slave supporting read and write transactions with FIXED, INCR, and WRAP burst modes.
The design follows the AXI4 protocol specification with decoupled channels, valid–ready handshaking, and ID-based transaction handling.

The RTL is verified using a class-based SystemVerilog verification environment, demonstrating both digital design and verification methodology skills.
The project was designed and simulated using Xilinx Vivado.

Technical Scope
AXI4 Features Implemented

Full AXI4 read and write channel support (AW, W, B, AR, R)

Burst types: FIXED, INCR, WRAP

Configurable burst length and transfer size

Transaction ID propagation across channels

Proper RLAST and response signaling

Byte-level write support using WSTRB

Design Architecture

Independent FSMs for:

Write Address Channel

Write Data Channel

Write Response Channel

Read Address Channel

Read Data Channel

Byte-addressable internal memory model

Wrap boundary calculation based on burst length and transfer size

Clean separation of control and data paths

Verification Methodology

The design is verified using a SystemVerilog class-based testbench, structured to reflect industry verification practices.

Verification Components

Transaction class with constrained random fields

Generator for randomized AXI read/write bursts

Driver to apply protocol-accurate stimulus

Monitor to observe and collect bus activity

Scoreboard for self-checking data integrity

Mailboxes and events for synchronization

Verification Capabilities

Randomized burst modes and lengths

End-to-end data checking

Protocol-aware stimulus generation

Waveform-driven debug in Vivado

Folder Structure
AXI4-Full-Slave/
│
├── rtl/
│   ├── axi_if.sv          # AXI interface definition
│   └── axi_slave.sv       # AXI4 slave RTL
│
├── tb/
│   ├── transaction.sv     # Transaction modeling
│   ├── generator.sv       # Stimulus generation
│   ├── driver.sv          # Bus driving logic
│   ├── monitor.sv         # Protocol monitoring
│   ├── scoreboard.sv      # Data checking
│   └── tb_top.sv          # Testbench top
│
├── README.md
└── .gitignore

Tools & Technologies

Verilog / SystemVerilog

Xilinx Vivado

GTKWave

Git & GitHub

Skills Demonstrated

AXI4 protocol understanding

FSM-based RTL design

Burst transaction handling

SystemVerilog class-based verification

Debugging using waveforms and self-checking testbenches

Professional project structuring and version control

Author

Ankur Mishra
B.Tech Electronics & Communication Engineering
National Institute of Technology Goa
