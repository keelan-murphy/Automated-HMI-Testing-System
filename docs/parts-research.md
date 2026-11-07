Here I will talk about why I picked my parts and why I did not pick other parts.

STM32 NUCLEO-L476RG
The NUCLEO-L476RG is a Nucleo-64 development board based on the STM32L476RG microcontroller. ST-LINK is built onto the board, so a separate debug probe is not required. The board can be powered from the ST-LINK USB connection. Arduino Uno V3 and ST morpho headers are provided for extra I/O, STM32CubeIDE is a supported toolchain, and there is one user LED [1].

The chip is in the same STM32L4 family as the STM32L475 used in class, so CubeIDE and the HAL still apply, but the Nucleo can stay with the project instead of a lab board. The user LED has already been blinked from CubeIDE, which confirms the board, cable and toolchain.

An ESP32 and a Raspberry Pi were considered as well. STM32 is the better fit for this rig: it matches the course and is better suited to switching a coil for a short, timed press. The ESP32’s Wi-Fi is not needed. A Pi is a Linux computer rather than a microcontroller, so it is a poor place to drive 12 V solenoids. The Nucleo will press the buttons. The laptop will run Python and the camera.
