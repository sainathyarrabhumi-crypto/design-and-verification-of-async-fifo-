# Asynchronous FIFO (16x8) Design and Verification

This repository contains the **RTL design** and **SystemVerilog-based verification** of an **Asynchronous FIFO**.  
The FIFO supports independent read/write clocks and is suitable for CDC (Clock Domain Crossing) applications.  

---

## 🚀 Features
- Data Width: **8 bits**  
- Depth: **16 entries**  
- Dual Clock Domain with Gray-code pointer synchronization  
- Status Flags: Full, Empty  

---

## 📂 Repository Structure
async-fifo/
├── rtl/
│ └── dut.sv # FIFO DUT (RTL design)
├── tb/
│ ├── wrdri.sv # Write driver
│ ├── rdri.sv # Read driver
│ ├── gen.sv # Stimulus generator
│ ├── wrmon.sv # Write monitor
│ ├── rdmon.sv # Read monitor
│ ├── ref_model.sv # Reference model
│ ├── scoreboard.sv # Scoreboard for data checking
│ └── async_fifo_tb.sv # Top-level testbench
├── docs/

---

## 🧩 Verification
- **Random stimulus** generated for read/write operations (`gen.sv`)  
- **Drivers** (`wrdri.sv`, `rdri.sv`) for applying transactions  
- **Monitors** (`wrmon.sv`, `rdmon.sv`) for capturing DUT activity  
- **Reference Model** used for golden comparison  
- **Scoreboard** to validate data integrity against reference model  
- Verified with **QuestaSim** (functional correctness only)  

---

## 📊 Results
- ✅ Verified FIFO operation with asynchronous clocks  
- ✅ Correct behavior of **Full** and **Empty** flags  
- ✅ Scoreboard ensured end-to-end data integrity  

---

## 📌 Run Instructions
```bash
git clone https://github.com/sainathyarrabhumi-crypto/async-fifo.git
cd async-fifo
make run    # or use sim/run.do for QuestaSim
👨‍💻 Author

Y. Sainath Reddy

RTL Design & Verification (SystemVerilog)

Practice Project for learning CDC concepts


