# 🧮 Scientific Calculator (Compiler Design Project)

![Language](https://img.shields.io/badge/Language-C-blue.svg)
![Build](https://img.shields.io/badge/Build-Flex%20%7C%20Bison-success.svg)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-lightgrey.svg)
![Course](https://img.shields.io/badge/Course-CSE314%20Compiler%20Design-orange.svg)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)

A high-performance command-line scientific calculator developed in **C** using **Flex (Lexical Analyzer)** and **Bison (Parser Generator)**.

Developed as a major project for the **Compiler Design (CSE314)** course at **Daffodil International University (DIU)**, this application demonstrates practical compiler construction principles including **lexical analysis, syntax parsing, semantic evaluation, precedence parsing, and robust error handling**.

---

## 📋 Table of Contents
- [🚀 Features](#-features)
- [🛠️ Technologies Used](#️-technologies-used)
- [📂 Project Structure](#-project-structure)
- [⚙️ Installation & Build Guide](#️-installation--build-guide)
- [🖥️ Example Inputs & Outputs](#️-example-inputs--outputs)
- [📊 Performance Highlights](#-performance-highlights)
- [📌 Future Improvements](#-future-improvements)
- [👨‍💻 Contributors](#-contributors)
- [🎓 Academic Acknowledgment](#-academic-acknowledgment)

---

## 🚀 Features
- **Basic Arithmetic Operations:** Addition (`+`), Subtraction (`-`), Multiplication (`*`), Division (`/`), Modulus (`%`).
- **Advanced Scientific Functions:**
  - **Trigonometric:** `sin(x)`, `cos(x)`, `tan(x)`
  - **Logarithmic:** `log(x)` (Natural Logarithm)
  - **Exponential:** `exp(x)`
  - **Power Function:** `x ^ y`
  - **Square Root:** `sqrt(x)`
- **Operator Precedence & Associativity:** Accurately parsed using Bison grammar definitions.
- **Robust Error Handling:** Detects syntax errors, division by zero, and invalid expressions.
- **Fast CLI Execution:** Ultra-lightweight command-line interface with instantaneous mathematical evaluations.

---

## 🛠️ Technologies Used
- **C Language** – Core evaluation engine & mathematical computation (`math.h`)
- **Flex** – Fast lexical analyzer generator (tokenization)
- **Bison** – LALR(1) parser generator (syntax tree and grammar analysis)
- **GCC / MinGW** – Compiler toolchain

---

## 📂 Project Structure
```bash
Compiler-Design-Scientific-Calculator/
├── calculator_with_conversion.l   # Flex lexical specification (tokens & patterns)
├── calculator_with_conversion.y   # Bison parser grammar rules & execution logic
├── Screenshot/                    # Project execution output screenshots
│   └── Screenshot.png
├── Project Report.pdf             # Comprehensive academic project documentation
├── text.yaml                      # Build reference commands
└── README.md                      # Project documentation
```

---

## ⚙️ Installation & Build Guide

### Prerequisites
Make sure **GCC**, **Flex**, and **Bison** are installed and added to your system `PATH`.

### Build & Run Commands

You can compile the project using the terminal / command prompt:

```bash
# 1. Generate parser C code and header file
bison -d calculator_with_conversion.y

# 2. Generate lexical analyzer C code
flex calculator_with_conversion.l

# 3. Compile generated source files with GCC
gcc -o app calculator_with_conversion.tab.c lex.yy.c -mconsole

# 4. Run the executable
./app.exe
```

---

## 🖥️ Execution Preview & Output

<div align="center">
  <img src="Screenshot/Screenshot.png" alt="Scientific Calculator Execution Screenshot" width="700"/>
</div>

### Sample Test Cases
```bash
> 5 + 3 * 2
= 11

> sqrt(49)
= 7

> sin(3.14159 / 2)
= 1.000000

> 2 ^ 8
= 256.000000

> log(10)
= 2.302585
```

---

## 📊 Performance Highlights
- Zero GUI overhead resulting in minimal RAM usage (< 5 MB).
- Native execution speed powered by C compiled binaries.
- Safe arithmetic bounds checking with clear runtime error messages.

---

## 📌 Future Improvements
- [ ] Add support for complex numbers and matrix computations.
- [ ] Implement variables assignment (`x = 10; y = x * 2;`).
- [ ] Session-based history logging.
- [ ] Lightweight cross-platform GUI frontend.

---

## 👨‍💻 Contributors

* **Shahriar Ahammed Ripon** (ID: 0242310005101019) — [@Shariar-Always](https://github.com/Shariar-Always) | [Portfolio](https://www.shariarahamed.com)
* **Omar Faruk Piash** (ID: 1659)
* **Md Faysal Ahamed** (ID: 1376)
* **Injamum Ul Hoque** (ID: 1645)
* **Md Sorowar Jahan Ishan** (ID: 1559)

---

## 🎓 Academic Acknowledgment

* **Course:** CSE314 – Compiler Design Lab
* **Department:** Computer Science and Engineering (CSE)
* **Institution:** Daffodil International University (DIU), Dhaka, Bangladesh
* **Project Period:** *August 2025*
