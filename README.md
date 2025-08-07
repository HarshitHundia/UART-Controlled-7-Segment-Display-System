# UART-Controlled-7-Segment-Display-System
Here’s a complete and clean `README.md` file for your GitHub repository:
**“UART-Controlled 7-Segment Display System”**

You can paste this into a file named `README.md` in your project folder.

---

```markdown
# UART-Controlled 7-Segment Display System

This project implements a UART-driven, command-controlled 4-digit 7-segment display system using Verilog HDL. It is designed as part of an FPGA prototyping lab assignment and demonstrates UART communication, finite state machine (FSM) control, and time-multiplexed display logic.

---

## 📌 Project Overview

- **Input Interface:** UART @ 9600 baud, 8 data bits, no parity, 1 stop bit (8N1)
- **Commands:** 
  - `S1234` → Start displaying digits 1, 2, 3, 4
  - `C` → Clear the display
  - `E` → Enable display (future use)
- **Output:** 4-digit multiplexed 7-segment display

---

## 🧠 Key Modules

| Module      | Description |
|-------------|-------------|
| `uart_rx`   | UART Receiver (8N1 protocol) |
| `fsm`       | Finite State Machine to decode and store incoming UART digits |
| `seg7_mux`  | Multiplexer to cycle through all 4 digits on a 7-segment display |
| `uart_fsm_7seg` | Top module connecting all submodules |
| `tb_*`      | Testbenches for each module |

---

## ✅ Features

- Receives serial ASCII commands and converts them to digit display
- FSM handles command decoding (`S`, `C`, `E`)
- Converts ASCII to binary (`"1"` → `4'b0001`)
- Cycles each digit using a refresh counter
- Verified using simulation testbenches (no physical FPGA required)

---

## 📷 Simulation Waveforms

Simulation results demonstrate:

- UART byte reception (`rx`, `rx_data`, `rx_done`)
- FSM transitions and digit storage
- 7-segment display digit cycling
- Edge cases like incorrect or partial inputs

All waveforms are included in `/sim/` and explained in the project report.

---

## 📘 Report

Detailed report with:

- Block diagram  
- Verilog architecture  
- Waveform analysis  
- Challenges faced & solutions  
- Output explanation

📄 Available in `/report/UART_7Segment_Project_Report.docx`

---

## 🚀 How to Simulate

1. Open in Vivado or ModelSim
2. Compile the source files in `/src/`
3. Run testbenches from `/tb/`
4. View waveform results and verify outputs

---

## 🛠 Tools Used

- **Vivado Design Suite** (Xilinx)
- **Git & GitHub**
- **GTKWave** / Vivado's simulation tool
- **Markdown** for documentation

---

## 📌 Author

**Harshit Hundia**  
2025 | FPGA Prototyping & Verilog Project  
`UART-Controlled 7-Segment Display System`

---

## 📜 License

This project is for educational purposes. Free to use with credit.

```

---

Let me know if you'd like:

* The above content saved as a `.md` file
* A `.gitignore` to exclude simulation folders or Vivado files
* A preview to help you format it nicely on GitHub

Once added, your GitHub repo will look great and professional!
