# CCS20 Template
This repository is based on the blinky demo with some changes to make the naming more generic. It contains the minimum possible setup for compiling and running code for the Tiva-C Launchpad with CCS20.

## Prerequisites
CCS20 by default does not ship with the compiler used on CCS12.8 for the Launchpad. The new, clang-based compiler is not compatible and does not allow for debugging of the TM4C devices. To fix this, you must install the arm cgt (https://www.ti.com/tool/ARM-CGT) to your standard ti install path and [update the ccs20 search path](https://e2e.ti.com/support/processors-group/processors/f/processors-forum/1485933/ccstudio-ccs-theia-does-not-contain-ti-arm-compiler-for-arm-cortex-tiva-c?tisearch=e2e-sitesearch&keymatch=CCSTUDIO%25252525252520ek-tm4c#) to use the correct compiler. After that, this should build, flash, and debug without issue.

This also assumes you have TivaWare installed at ${TI_PRODUCTS_DIR__TIREX}/TivaWare_C_Series-2.2.0.295 which on Windows is under C:\ti and on mac is under /home/<youruser>/ti. If you don't, you can go to the Resource Explorer in either CCS version, type in the name of our board (EK-TM4C123GXL), and then add the TivaWare install under Arm-based microcontrollers-->EmbeddedSoftware in the folder view on the left.
