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

 ```

## Documentation ##

More information on the MemoryStats and Debug API can be found in the [mbed handbook]().
