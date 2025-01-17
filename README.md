# Unhandled Memory Access in Assembly

This repository demonstrates a common error in assembly programming: accessing memory without proper bounds checking.  The code attempts to access memory at an address calculated dynamically, which may lead to segmentation faults if the calculated address falls outside the allowed memory space.

The `bug.asm` file contains the erroneous code.  The solution, presented in `bugSolution.asm`, adds necessary checks to prevent memory access violations.  This is crucial for writing robust and secure assembly programs.

## How to Reproduce

1. Assemble the code in `bug.asm` (using NASM or a similar assembler).
2. Link the resulting object file (e.g., `bug.o`) to create an executable.
3. Run the executable.  If the memory access is invalid, you'll likely encounter a segmentation fault or similar error.

## Solution

The `bugSolution.asm` file shows the corrected version. The solution involves checking that the calculated memory address is within the program's allocated memory region before attempting to access it. This prevents segmentation faults by handling the out-of-bounds conditions gracefully.