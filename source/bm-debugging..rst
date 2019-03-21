Using GDB Debugger with riscvOVPsim
===================================

The simulator install includes a copy of the GNU GDB debugger - making it very easy for you to debug your own programs.

If you have downloaded riscvOVPsim and ran dhrystones, you will have noticed one of the scripts being: DEBUG_GDB_RV32_dhrystone.sh (.bat).

This runs the simulator with the -gdbconsole command line argument. This launches a GDB in a new command window and connects it to the RSP port of the simulator.

When the GDB console window opens, you can type your normal GDB commands: eg step, continue etc.
Don't forget a 'quit' followed by 'y' to cleanly finish.



