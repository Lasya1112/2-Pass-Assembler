# 🛠️ Two-Pass Assembler for SIMPLE Architecture

This project is a fully functional **two-pass assembler** written in C++, designed to process a custom instruction set similar to the **SIMPLE** architecture. It converts `.asm` files into machine-readable object code (`.o`), while also generating a listing file (`.l`) and a log file (`.log`) containing warnings or errors.

---

## 📁 Files Generated

| File Type        | Extension | Description                                  |
|------------------|-----------|----------------------------------------------|
| **Input**        | `.asm`    | Assembly source code                         |
| **Object**       | `.o`      | Binary machine code (used by simulators)     |
| **Listing**      | `.l`      | Human-readable PC + hex + original line      |
| **Log**          | `.log`    | Errors and warnings during assembly          |

---

## 🧠 Features

- ✅ Two-pass design (label resolution, forward referencing)
- ✅ Supports decimal, octal, and hexadecimal operands
- ✅ Detects invalid labels, mnemonics, and operand types
- ✅ Logs unused or undefined labels
- ✅ Instruction encoding: 24-bit operand + 8-bit opcode
- ✅ Customizable instruction set (`mnemonic` mapping)

---

## 🔧 Compilation

Use a C++ compiler like `g++`:

```bash
g++ asm.cpp -o asmexe
./asmexe file_name.asm
