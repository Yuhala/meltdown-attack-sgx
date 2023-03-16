------------------------
Demo of SGX protection against Meltdown (rogue memory access)
------------------------


How to Build/Execute the demo
------------------------------------
Build libkdump:  
1. Run  
 	```$ git submodule init```  
    ```$ git submodule update```  
 	```$ cd meltdown/libkdump```  
    ```$ make && sudo make install```  

Build the demo:  
1. Install Intel(R) SGX SDK for Linux* OS  
2. Build the project with the prepared Makefile:  
    2a. Hardware Mode, Debug build:  
        ```$ make```  
    2b. Hardware Mode, Pre-release build:  
        ```$ make SGX_PRERELEASE=1 SGX_DEBUG=0```  
    2c. Hardware Mode, Release build:  
        ```$ make SGX_DEBUG=0```  
    2d. Simulation Mode, Debug build:  
        ```$ make SGX_MODE=SIM```  
    2e. Simulation Mode, Pre-release build:  
        ```$ make SGX_MODE=SIM SGX_PRERELEASE=1 SGX_DEBUG=0```  
    2f. Simulation Mode, Release build:  
        ```$ make SGX_MODE=SIM SGX_DEBUG=0```  
3. Execute the binary directly:  
    ```$ ./app```  
4. Remember to "make clean" before switching build mode
