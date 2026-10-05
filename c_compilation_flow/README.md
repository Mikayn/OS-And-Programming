# C Compilation Flow

## [-] Introduction

This task explores the four main stages of compiling a C program using GCC: **preprocessing, compilation, assembly, and linking**. Each stage transforms the source code into a progressively lower-level representation until a final executable is produced.

## [-] Objectives

- Understand the four stages of the GCC compilation process.
- Generate and inspect preprocessed C code.
- Convert C source code into assembly and object code.
- Understand how object files are linked into an executable.

## [-] One-Shot Compilation

GCC normally performs all four stages automatically:

```bash
gcc name.c -o name
```

Doing so abstracts the user from the stages of compiling the C program. Each step can be compiled separately to better understand the Compilation Flow. 

## [-] Commands
### 1. Preprocessing

```bash
gcc -E name.c -o name.i
```
Generates the preprocessed C source file, expanding headers and macros.

### 2. Compilation

```bash
gcc -S name.i -o name.s
```
Converts the preprocessed C code into assembly code.

### 3. Assembly

```bash
gcc -c name.s -o name.o
```
Converts the assembly code into an object file containing machine code.

### 4. Linking

```bash
gcc name.o -o name
```
Links the object file with required libraries and produces the final executable.


The resulting executable can be run with:
```bash
./name
```
