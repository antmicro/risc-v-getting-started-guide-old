Semihosting I/O calls in riscvOVPsim
====================================

The riscvOVPsim simulator includes semihosting of Newlib (https://en.wikipedia.org/wiki/Newlib) system calls, such as read, write, open...

A simple program, such as a Fibonacci sequence generator (as provided in examples/fibonacci) uses semihosting and looks like:

.. code-block:: bash

    #include <stdio.h>
    #include <stdlib.h>

    static int fib(int i) {
        return (i>1) ? fib(i-1) + fib(i-2) : i;
    }

    #define MAX 48
    static unsigned char resultArray[MAX];

    int main(int argc, char **argv[]) {

        unsigned int i;
        int num = (argc >= 2) ? atoi((const char *)argv[1]) : 38;

        printf("starting fib(%d)...\n", num);

        for(i=0; i<num; i++) {
            int result=fib(i);                      // calculate fibonacci for i
            printf("fib(%d) = %d\n", i, result);

            resultArray[i%MAX] = result & 0xff;     // store low byte into result array
        }

        printf("finishing...\n");

        return 0;
    }
