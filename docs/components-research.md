Here I will talk about why I picked my parts and why I did not pick other parts.

Microcontroller — STM32 NUCLEO-L476RG
The NUCLEO-L476RG is a Nucleo-64 development board based on the STM32L476RG microcontroller. ST-LINK is built onto the board, so a separate debug probe is not required. The board can be powered from the ST-LINK USB connection. Arduino Uno V3 and ST morpho headers are provided for extra I/O, STM32CubeIDE is a supported toolchain, and there is one user LED [1].

The chip is in the same STM32L4 family as the STM32L475 used in class, so CubeIDE and the HAL still apply, but the Nucleo can stay with the project instead of a lab board. The user LED has already been blinked from CubeIDE, which confirms the board, cable and toolchain.

An ESP32 and a Raspberry Pi were considered as well. STM32 is the better fit for this rig: it matches the course and is better suited to switching a coil for a short, timed press. The ESP32’s Wi-Fi is not needed. A Pi is a Linux computer rather than a microcontroller, so it is a poor place to drive 12 V solenoids. The Nucleo will press the buttons. The laptop will run Python and the camera.

Actuator — SD0630 12 V solenoid

Keys on a membrane panel only move about a millimetre. A 12 V linear solenoid is enough to press them. Servos with a cam would drift. A linear actuator is slower and more expensive than this project needs.

The part ordered is the Solentec SD0630, 12 V dc, pull type, 10 mm maximum stroke, listed on RS as 905-9931 [4]. Continuous rating is 3 W [4]. Ten millimetres is more travel than a membrane key, so a mechanical hard stop and a soft tip are required so the overlay is not damaged. Two solenoids were bought so two keys can be pressed without moving the fixture. A 12 V dc supply of at least a couple of amps is used, from college

Switch — IRLZ44N MOSFET and flyback diode

The solenoid is an inductive load. It is not switched with a resistor. Each coil is switched by an N-channel MOSFET, with a flyback diode across the coil.

The MOSFET is the Infineon IRLZ44NPBF, RS 919-4814. It is a 55 V, 47 A device in a TO-220 package, with 22 mΩ on-resistance [5], [6]. 12 V on the drain is well inside the 55 V rating. Four devices were ordered. Diodes and resistors come from college.

Camera

Two extra LED methods were looked at and not bought. A Raspberry Pi Camera Module needs a Raspberry Pi [7]. Colour-sensor chips such as the TCS34725 are sold as bare parts, not a module that can be wired on a breadboard in week one. The laptop already has a camera, so that is used for now. A proper camera can be added later once one automated press works.

Device under test

The original plan was a medical keypad from a company. That unit has not arrived. A cheap membrane keypad will be used as a stand-in. The rig is a button-and-LED tester. It does not have to be limited to medical devices. Medical devices is the end goal as it is more attractive.

References
[1] STMicroelectronics, “NUCLEO-L476RG,” STMicroelectronics. [Online]. Available: https://www.st.com/en/evaluation-tools/nucleo-l476rg.html. [Accessed: Nov. 7, 2026].

[2] Espressif Systems, “ESP32,” Espressif. [Online]. Available: https://www.espressif.com/en/products/socs/esp32. [Accessed: Nov. 7, 2026].

[3] Raspberry Pi Ltd, “Raspberry Pi documentation,” Raspberry Pi. [Online]. Available: www.raspberrypi.com/documentation/computers/raspberry-pi.html. [Accessed: Nov. 7, 2026].

[4] RS, “Solentec Limited SD0630 Linear Solenoid, 12V dc,” RS Ireland, stock no. 905-9931. [Online]. Available: https://ie.rs-online.com/web/p/linear-solenoids/9059931. [Accessed: Nov. 7, 2026].

[5] Infineon Technologies, “IRLZ44NPbF HEXFET Power MOSFET,” datasheet. [Online]. Available: www.infineon.com/assets/row/public/docu…irlz44n-datasheet-en.pdf. [Accessed: Nov. 7, 2026].

[6] RS, “Infineon IRLZ44NPBF N-Channel MOSFET,” RS Ireland, stock no. 919-4814. [Online]. Available: https://ie.rs-online.com/web/p/mosfets/9194814. [Accessed: Nov. 7, 2026].

[7] Raspberry Pi Ltd, “Camera,” Raspberry Pi documentation. [Online]. Available: www.raspberrypi.com/documentation/accessories/camera.html. [Accessed: Nov. 7, 2026].
