Bere Metal Applications
=======================

A bare metal application is a program that runs directly on the hardware without the use of a kernel or operating system to provide services. It will access the hardware directly and is most applicable for embedded systems and firmware generally with time-critical latency requirements.

To create bare metal software requires the use of a text edit ad an assembler / cross compiler. A GNU Cross Compiler for RISC-V can be found at: https://github.com/riscv/riscv-gcc

Often with bare metal programs you needed to implement drivers to devices such as UARTs so that you can monitor program output etc. A simulator can provide 'semihosting' of certain functions so that the simulator takes care of I/O like read/write/open etc.



