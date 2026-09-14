# Video 7: Types of Instructions in a General Purpose Computer

## Why this matters

Every program you write eventually becomes a sequence of instructions that the CPU executes. Understanding the three types of instructions tells you everything a CPU can actually do. Every single instruction, no matter how complex the program, falls into one of these three categories.

## Core Concept: What is an Instruction?

An **instruction** is a command given to the processor telling it what operation to perform and how to execute it.

All instructions in a general purpose computer (x86, AMD, Intel, ARM) fall into three categories:

```mermaid
flowchart TD
    A[All CPU Instructions] --> B[Data Transfer]
    A --> C[Data Manipulation]
    A --> D[Program Control]
    
    B --> B1[Move data between\nregisters, memory, I/O]
    
    C --> C1[Arithmetic\nADD, SUB, MUL, DIV]
    C --> C2[Logical\nAND, OR, XOR]
    C --> C3[Shift/Rotate\nLeft, Right]
    
    D --> D1[Branch / Jump]
    D --> D2[Call / Return]
    D --> D3[Skip]
```

## The Three Instruction Types

### A. Data Transfer Instructions

**What they do**: Copy or move data from one place to another without changing the data itself.

Data can move between:
- Register to register
- Register to memory
- Memory to register
- CPU to I/O device
- I/O device to CPU

**Key commands**: `LOAD`, `STORE`, `MOV`, `XCHG`, `PUSH`, `POP`, `IN`, `OUT`

```mermaid
flowchart LR
    MEM[Memory] <-->|"LOAD / STORE"| REG[Registers]
    REG <-->|"IN / OUT"| IO[I/O Devices]
    REG <-->|"MOV / XCHG"| REG2[Other Registers]
    REG <-->|"PUSH / POP"| STK[Stack]
```

### B. Data Manipulation Instructions

**What they do**: Change, process, or transform data. This is where actual computation happens.

Three sub-categories:

| Sub-category | What it does | Examples |
|-------------|-------------|---------|
| Arithmetic | Math operations on numbers | ADD, SUB, MUL, DIV, INC, DEC |
| Logical | Bitwise operations | AND, OR, XOR, Complement, Clear |
| Shift/Rotate | Move bits left or right within a register | Logical Shift, Arithmetic Shift, Rotate |

### C. Program Control Instructions

**What they do**: Change the order of execution. Without these, a program would only run top to bottom with no decisions or loops.

**Key commands**: `BRANCH`, `JUMP`, `SKIP`, `CALL`, `RETURN`

These are what make `if`, `for`, `while`, and function calls possible at the hardware level.

```mermaid
flowchart TD
    A[Normal execution\nline by line] --> B{Program Control\nInstruction?}
    B -->|JUMP/BRANCH| C[Go to a different\naddress in memory]
    B -->|CALL| D[Jump to a subroutine\nand save return address]
    B -->|SKIP| E[Skip the next\ninstruction]
    B -->|No| F[Continue to\nnext instruction]
    D --> G[RETURN\nGo back to saved address]
```

## How They Work Together

A real program uses all three types. Here is a simple example:

```mermaid
flowchart TD
    A["LOAD A\n(Data Transfer)"] --> B["ADD B\n(Data Manipulation)"]
    B --> C{"Is result > 100?\n(Program Control)"}
    C -->|Yes| D["STORE result\n(Data Transfer)"]
    C -->|No| E["JUMP back to start\n(Program Control)"]
```

## Key Terms

| Term | Meaning | Example |
|------|---------|---------|
| Data Transfer | Move data without changing it | LOAD, STORE, MOV |
| Data Manipulation | Change or process data | ADD, AND, Shift Left |
| Program Control | Change execution order | JUMP, CALL, RETURN |
| Arithmetic instruction | Math on numbers | ADD, SUB, MUL, DIV |
| Logical instruction | Bitwise operations | AND, OR, XOR |
| Shift instruction | Move bits within a register | Shift Left, Rotate Right |
| Branch/Jump | Go to a different instruction address | JUMP 200, BRANCH IF ZERO |
| Subroutine | A reusable block of instructions | CALL function, RETURN |

## Summary

- Every CPU instruction falls into one of three types: data transfer, data manipulation, or program control
- Data transfer moves data between registers, memory, and I/O without changing it
- Data manipulation includes arithmetic (ADD, SUB), logical (AND, OR), and shift operations
- Program control changes the execution flow with jumps, branches, calls, and returns
- Real programs combine all three types to do useful work

## Quick Revision

- Data Transfer = LOAD, STORE, MOV, PUSH, POP, IN, OUT (moves data, does not change it)
- Data Manipulation = Arithmetic + Logical + Shift (changes data)
- Program Control = JUMP, BRANCH, CALL, RETURN, SKIP (changes execution order)
- Without program control, there are no loops or if-else decisions
- All three types work together in every real program
