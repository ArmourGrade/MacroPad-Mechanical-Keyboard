# MacroPad-Mechanical-Keyboard
### OVERVIEW
 - This is a mechanical keyboard macro pad project featuring the schematic and firmware.
 - The Keyboard is designed to work with QMK enviroment.
 - The keyboard consists of two PCBs, one Main PCB and the second PCB with two encoders.
 - The two PCBs are connected with a FPC cable.
 - The keyboard features two programmable encoders/knobs with push-buttons, an OLED screen and 12 Buttons/Swithces.
 - The main PCB requires a PRO MICRO format Controller Board (RP2040 Qwiic is used in this project). 

### YOUTUBE VIDEO CLICK ON PICTURE
[![MacroPad](https://github.com/ArmourGrade/MacroPad-Mechanical-Keyboard/blob/main/Images%20Keyboard/P1140373.JPG?raw=true)](https://www.youtube.com/watch?v=CmnHtQ5szXs)
![MacroPad_Clear](https://github.com/ArmourGrade/MacroPad-Mechanical-Keyboard/blob/main/Images%20Keyboard/Keyboard_ON_DESK.jpg?raw=true) 
### FIRMWARE SETUP

- The non via firmware is setup for my uses currently.
- The OLED shows what each of the buttons does on the layer you are currently on.
- You go through Layers by rotating one of the encoders and by pushing the button on that encoder more information will be displayed on the OLED.
- The 1st layer is a simple app launcher.
- The 2nd layer is for a SPICE simulation tool called MICRO-CAP.
- The 3rd layer is for Altium Designer and some functions are still a work-in progress.
- The 4th layer is for RGB settings, here rotating the second encoder will change the colours and pushing the encoder button will toggle the RGB on/off.
- The 5th layer is for MATHCAD.

- I have also now, as of 3rd January 2025. added the VIA compatible firmware (armourgrade_via), so it can be programmed through the GUI.
- The oled here is just used to show which layer is currently active and has small images displayed.
- The top knob is still used for going through layers, the bottom is used for volume on all layer except layer 4 where it adjust the RGB colours.
- To reprogram the keyboard through VIA, go to the SETTINGS tab in the VIA opened in your browser or App and enable the DESIGN tab.
- Then go to the DESIGN tab and press LOAD in the **Load Draft Definitions** and upload the keyboard.json file that is provided in the armourgrade_via.zip
- After that the keyboard should appear and you can programm it however you like.
>### NOTES 
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
