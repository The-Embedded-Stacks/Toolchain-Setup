# Toolchain-Setup

**The text below contains necessary tools for starting with bare-metal programming (currently for Windows - tools for other OS need to be added).**

- GCC-ARM - refers to a specific GNU compiler toolchain tailored for ARM-based CPUs. This collection of programming tools, which includes a compiler, linker, and assembler, among others, is critical for creating, debugging, and optimizing applications for ARM architectures.A specific GNU compiler toolchain for ARM based CPUs
	- https://developer.arm.com/downloads/-/arm-gnu-toolchain-downloads

- Flash Software - OpenOCD is an open-source tool that facilitates debugging on numerous ARM devices using GDB, compatible with a wide variety of JTAG programmers.
    - https://openocd.org/pages/about.html
	- https://gnutoolchains.com/arm-eabi/openocd/

- Make (Windows) - is an essential tool that assists in the automatic building of applications. This package includes both binary files and dependencies, enabling the efficient management and execution of build processes on Windows platforms
	- https://gnuwin32.sourceforge.net/packages/make.htm

**After downloading the .zip files mentioned above, you need to map the binaries to environment variables and verify their recognition:**

    make --version
    openocd --version
    arm--none-eabi--gcc --version

# Overview of the translation of a program:
The source code undergoes several transformation stages to become an executable program:

Preprocessor (generates *.i files):
    - Processes the source code according to preprocessor directives and performs macro substitutions.

Compiler (generates *.s files):
    - Translates high-level programming language into assembly language.

Assembler (generates *.o files):
    - Converts assembly language into object code, which is a binary representation of the program.

Linker (generates a relocatable file):
    -Links the input object files into a single executable file and resolves symbol references.
Locator:
    -Maps all addresses and data to the processor's memory space, preparing the program to be loaded and run.

Loader:
    - Loads the program into memory and initiates its execution.

The process above ensures the program is appropriately transformed and placed into memory for execution.


