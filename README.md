# UART Serial Communication Interface using Verilog

This repository contains the RTL design and verification of a UART (Universal Asynchronous Receiver Transmitter) serial communication interface developed using Verilog. The project focuses on implementing a reliable and easy-to-understand UART design that can be used in FPGA-based digital systems.

## Overview
UART is a widely used asynchronous serial communication protocol that allows data transfer between two digital systems without a shared clock. In this project, separate transmitter (TX) and receiver (RX) modules are designed to handle serial data transmission and reception based on standard UART communication principles.

This implementation emphasizes clarity and correctness, helping in understanding UART timing, framing, and data flow at the RTL level. The design can serve as a practical reference for basic serial communication in digital hardware designs.
<img width="692" height="327" alt="image" src="https://github.com/user-attachments/assets/d7ba0363-bbbb-4d14-b0ec-f25822891aaf" />
<img width="1130" height="730" alt="image" src="https://github.com/user-attachments/assets/adf640e4-8cf5-49e3-ae0b-b7f733be86d4" />


## Design Implementation
The UART design is implemented using FSM-based control logic to manage the transmission and reception processes. A baud rate generator is used to derive the required timing for serial communication from the system clock.

The transmitter converts parallel data into serial format, while the receiver reconstructs serial data back into parallel form by sampling incoming bits at the correct time. The design is modular, making individual blocks easy to understand, test, and reuse.

The design supports:
- Start bit detection and generation
- Data framing with multiple data bits
- Stop bit handling for proper frame completion
- Modular RTL structure for easy integration and reuse
- <img width="965" height="547" alt="image" src="https://github.com/user-attachments/assets/17ba47be-e7ce-4ca5-8680-e705a79d5b95" />


## Verification
Functional verification is performed using Verilog testbenches to ensure correct operation of the UART design. Simulation waveforms are analyzed to verify proper timing, data transfer, and synchronization between the transmitter and receiver.

Test scenarios include basic transmission and reception, validation of start and stop bits, and checking correct data recovery at the receiver. Both transmit and receive paths are validated to confirm reliable serial communication under different operating conditions.

## Tools and Technologies
- **HDL:** Verilog  
- **Simulation & Synthesis:** Xilinx Vivado
