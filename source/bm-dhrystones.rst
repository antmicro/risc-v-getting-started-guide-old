Running Dhrystones on riscvOVPsim
=================================

After you have downloaded the simulator, go into the examples directory:

.. code-block:: bash

    cd <path_where_riscv-ovpsim_is_cloned>
    cd examples
    cd dhrystone
    
You will see several scripts to execute. If on Linux use the .sh, if on windows the .bat

You should see output similar to: 

.. code-block:: bash

    simond@lnx:~/git/riscv-ovpsim/examples/dhrystone$ RUN_RV32_dhrystone.sh
    Imperas riscvOVPsim

    CpuManagerFixedPlatform (64-Bit) v20181126.0 Open Virtual Platform simulator from www.IMPERAS.com.
    Copyright (c) 2005-2018 Imperas Software Ltd.  Contains Imperas Proprietary Information.
    Licensed Software, All Rights Reserved.
    Visit www.IMPERAS.com for multicore debug, verification and analysis solutions.

    CpuManagerFixedPlatform started: Mon Nov 26 14:52:21 2018

    Info (OR_OF) Target 'riscvOVPsim/cpu' has object file read from 'dhrystone.RISCV32.elf'
    Info (OR_PH) Program Headers:
    Info (OR_PH) Type           Offset     VirtAddr   PhysAddr   FileSiz    MemSiz     Flags Align
    Info (OR_PD) LOAD           0x00000000 0x00010000 0x00010000 0x00010af0 0x00010af0 R-E   1000
    Info (OR_PD) LOAD           0x00010af0 0x00021af0 0x00021af0 0x000009c0 0x00003228 RW-   1000
     
    Dhrystone Benchmark, Version 2.1 (Language: C)
     
    Program compiled without 'register' attribute
     
    Execution starts, 5000000 runs through Dhrystone
    Execution ends
     
    Final values of the variables used in the benchmark:
     
    Int_Glob:            5
            should be:   5
    Bool_Glob:           1
    ...
    ...
     
    Info 
    Info ---------------------------------------------------
    Info CPU 'riscvOVPsim/cpu' STATISTICS
    Info   Type                  : riscv (RV32IMAC)
    Info   Nominal MIPS          : 100
    Info   Final program counter : 0x10098
    Info   Simulated instructions: 6,615,062,845
    Info   Simulated MIPS        : 1662.1
    Info ---------------------------------------------------
    Info 
    Info ---------------------------------------------------
    Info SIMULATION TIME STATISTICS
    Info   Simulated time        : 66.15 seconds
    Info   User time             : 3.98 seconds
    Info   System time           : 0.00 seconds
    Info   Elapsed time          : 3.98 seconds
    Info   Real time ratio       : 16.62x faster
    Info ---------------------------------------------------

    CpuManagerFixedPlatform finished: Mon Nov 26 14:52:25 2018
    CpuManagerFixedPlatform (64-Bit) v20181126.0 Open Virtual Platform simulator from www.IMPERAS.com.
    Visit www.IMPERAS.com for multicore debug, verification and analysis solutions.

And you can see that the simulator ran some 6.6 Billion instructions in under 4 elapsed seconds.

This ran the simulator on one of the .elf files (the cross compiled RISC-V binary) with certain simulator configuration options.

For more information please read the simulator user guide (riscvOVPsim_User_Guide.pdf) in the doc directory.
