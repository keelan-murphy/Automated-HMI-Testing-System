# Solenoid

Solentec SD0630 12 V, RS 905-9931 [1], [2]. The coil is 12 V at about 0.25 A (3 W / 12 V). Two flying leads, no polarity, so either lead can go to 12 V+.

# MOSFET

Infineon IRLZ44NPbF, TO-220 [3]. Writing facing you, legs down: pin 1 gate, pin 2 drain, pin 3 source. The metal tab is the drain.

Source to GND. Drain to the solenoid lead that is not on 12 V+. Gate to the Nucleo pin. 12 V does not connect to the gate.
















# References
[1] Solentec Ltd., "SD0630 D-frame solenoid," datasheet, Jan. 2016. [Online]. Available: https://media.distrelec.com/Web/Downloads/_t/ds/Solentec_9059931_eng_tds.pdf

[2] RS Components, "SD0630 12V linear solenoid, RS stock no. 905-9931." [Online]. Available: https://uk.rs-online.com/web/p/linear-solenoids/9059931

[3] Infineon Technologies, "IRLZ44NPbF, 55 V single N-channel power MOSFET," datasheet, rev. 2.1, Aug. 2026. [Online]. Available: https://www.infineon.com/assets/row/public/documents/24/49/infineon-irlz44npbf-datasheet-en.pdf

