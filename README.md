# mbed-os-example-platform-utils #

Platform Utilities usage example for mbed OS

This is a example showing how to use mbed-OS Debug and MemoryStats utility functions

The program retrieves stack and heap usage and also demonstrates the usage of Debug APIs.

### Suggested hardware for running this example ###

* [K64F](https://os.mbed.com/platforms/FRDM-K64F/)

##  Getting started

1. Import the example

   ```
   mbed import mbed-os-example-platform-utils
   cd mbed-os-example-platform-utils
   ```
2. Compile and generate binary

   For example, for `ARMCC`:

   ```
   mbed compile -t arm -m k64f -DMBED_STACK_STATS_ENABLED -DMBED_HEAP_STATS_ENABLED -DMBED_MEM_TRACING_ENABLED
   ```
   
   NOTE: Make sure you define the following variables:
   MBED_STACK_STATS_ENABLED 
   MBED_HEAP_STATS_ENABLED 
   MBED_MEM_TRACING_ENABLED
   
 5. Open a serial console session with the target platform using the following parameters:
    * **Baud rate:** 9600
    * **Data bits:** 8
    * **Stop bits:** 1
    * **Parity:** None
 
 6. Copy or drag the application `mbed-os-example-platform-utils.bin` in the folder `mbed-os-example-platform-utils/BUILD/<TARGET NAME>/<PLATFORM NAME>` onto the target board.
 
 7. The serial console should display a similar output to below:
 ```
This message is from debug function
This message is from debug_if
MemoryStats:
        Bytes allocated currently: 80
        Max bytes allocated at a given time: 80
        Cumulative sum of bytes ever allocated: 80
        Current number of bytes allocated for the heap: 186884
        Current number of allocations: 2
        Number of failed allocations: 0
Cumulative Stack Info:
        Maximum number of bytes used on the stack: 560
        Current number of bytes allocated for the stack: 5376
        Number of stacks stats accumulated in the structure: 3
Thread Stack Info:
        Thread: 0
                Thread Id: 0x20001EE8
                Thread Name: "main_thread"
                Maximum number of bytes used on the stack: 384
                Current number of bytes allocated for the stack: 4096
                Number of stacks stats accumulated in the structure: 1
        Thread: 1
                Thread Id: 0x20000394
                Thread Name: ""
                Maximum number of bytes used on the stack: 64
                Current number of bytes allocated for the stack: 512
                Number of stacks stats accumulated in the structure: 1
        Thread: 2
                Thread Id: 0x200003DC
                Thread Name: ""
                Maximum number of bytes used on the stack: 112
                Current number of bytes allocated for the stack: 768
                Number of stacks stats accumulated in the structure: 1
Done...

 ```

## Documentation ##

More information on the MemoryStats and Debug API can be found in the [mbed handbook]().
