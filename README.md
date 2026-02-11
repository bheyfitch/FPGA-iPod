# FPGA iPod

FPGA-based audio playback system that streams music directly from flash memory with real-time keyboard-controlled playback.


**Overview**

This project implements an iPod-style audio playback system entirely in RTL on an FPGA. Audio samples are read from external flash memory and streamed to a DAC with precise timing and synchronization.

The system supports:

- Start, stop, rewind, and playback speed adjustment via keyboard input

- Real-time audio streaming to a DAC

- LED display of live audio signal strength


**System Architecture**

The design is modular and built around multiple interacting finite state machines.

Key components include:

- Flash memory interface using the Avalon bus protocol

- Audio streaming logic with timing synchronization

- Keyboard input handler

- Clock division and clock domain synchronization

- PicoBlaze soft processor for real-time audio signal strength computation


**Implementation Details**

- Designed RTL modules in SystemVerilog

- Implemented FSMs to manage memory addressing, timing control, and data flow

- Integrated flash memory and DAC communication over Avalon bus

- Managed clock synchronization between FPGA system clock and DAC clock

- Incrementally integrated and validated modules in hardware using Intel Quartus Prime


**Verification**

- Each module was verified before hardware deployment:

- Developed SystemVerilog testbenches for all major modules

- Verified I/O behavior in ModelSim

- Debugged internal FPGA signals using SignalTap logic analyzer

- Performed iterative hardware validation after synthesis


**Tools & Technologies**

- SystemVerilog

- Intel Quartus Prime

- ModelSim

- PicoBlaze soft processor

- Avalon bus interface

- SignalTap logic analyzer
