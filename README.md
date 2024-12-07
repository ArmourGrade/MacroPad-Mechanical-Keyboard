# MacroPad-Mechanical-Keyboard
This is a mechanical keyboard macro pad project featuring the schematic and firmware


![MacroPad](https://github.com/ArmourGrade/MacroPad-Mechanical-Keyboard/blob/main/Images%20Keyboard/P1140373.JPG?raw=true)

>#### Overview
> - The firmware is for **QMK Enviroment** and should be placed in the **keyboards** folder after installing the QMK Enviroment,
>   for example C:\Users\PC_NAME\qmk_firmware\keyboards.
>
> - The controller board used in the project is a Sparkfun RP2040 pro micro Qwiic board
>   but the project is compatible with the other PRO MICRO Boards like the Atmega32u4 based ones.

> - Depending on the Voltage of the GPIO pins of the controller board either the 0 Ohm resistor should be populated if the GPIO Voltage is 5V
>   or the level shifter IC if its 3V3(then the 0 Ohm resistor shouldnt be populated).
>   This is because the RBG LEDs require at least 0.7*Vcc for the logic input and the VCC is 5V.
>
> - The diodes connected in series to the switches are **TS4148**.