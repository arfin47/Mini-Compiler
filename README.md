# MiniLang Compiler

A simple educational compiler for **MiniLang**, built using **Flex**, **Bison**, and **C**. The project demonstrates the complete compilation pipeline, from lexical analysis to pseudo-assembly code generation.

## Features

* Lexical analysis using **Flex**
* Syntax analysis using **Bison**
* Abstract Syntax Tree (AST) construction
* Symbol table implementation
* Semantic analysis
* Three-Address Code (TAC) generation
* Basic code optimization
* Pseudo-assembly code generation
* Compiler error detection and reporting

---

## Technologies Used

* C
* Flex
* Bison
* GCC
* Make

---

## Project Structure

```text
MiniCompiler/
├── lexer.l              # Lexical analyzer
├── parser.y             # Parser grammar
├── ast.c
├── ast.h
├── semantic.c
├── semantic.h
├── symbol_table.c
├── symbol_table.h
├── codegen.c
├── codegen.h
├── Makefile
├── demo.sh
├── testcases/
└── README.md
```

---

## Prerequisites

Install the following packages on Linux (or WSL):

```bash
sudo apt update
sudo apt install -y flex bison gcc make
```

---

## Build

Compile the project using:

```bash
make
```

---

## Run

Execute the compiler on a sample program:

```bash
./minicompiler testcases/sample.ml
```

To run the demonstration script:

```bash
bash demo.sh
```

---

## Example MiniLang Program

```c
int x;
int y;
bool flag;

x = 10;
y = 20;
flag = true;

if (flag) {
    print(x + y);
}

while (x > 0) {
    x = x - 1;
}
```

---

## Compiler Pipeline

The compiler performs the following stages:

1. Lexical Analysis
2. Syntax Analysis
3. AST Construction
4. Semantic Analysis
5. Intermediate Code (TAC) Generation
6. Code Optimization
7. Pseudo-Assembly Generation

---

## Optimizations

The compiler implements several basic optimizations, including:

* Constant Folding
* Algebraic Simplification
* Copy Propagation
* Dead Code Elimination

Examples:

```text
2 + 3  → 5
x + 0  → x
x * 1  → x
```

---

## Error Handling

The compiler detects and reports:

* Lexical errors
* Syntax errors
* Duplicate variable declarations
* Undeclared variables
* Type mismatches
* Invalid conditional expressions

Example:

```text
[Lexical Error] Unknown character '@'
```

---

## Output

After successful compilation, the compiler generates:

* Abstract Syntax Tree (AST)
* Three-Address Code (TAC)
* Optimized Intermediate Code
* Pseudo-Assembly Code

Generated TAC and assembly output are written to:

```text
output.tac
```

---

## Clean Build

To rebuild the project from scratch:

```bash
make clean
make
```

---

## Learning Objectives

This project demonstrates the fundamental concepts of compiler construction, including:

* Lexical analysis
* Parsing
* Abstract Syntax Trees
* Semantic analysis
* Symbol tables
* Intermediate code generation
* Code optimization
* Target code generation

---

## Author

Developed as an educational compiler project using **Flex**, **Bison**, and **C**.
