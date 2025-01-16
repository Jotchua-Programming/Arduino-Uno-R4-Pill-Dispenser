# Arduino-Uno-R4-Pill-Dispenser
This repository contains code for an Arduino Uno R4 WiFi and provides functionality to a time based pill dispenser using a stepper motor and an accompanying LCD screen.
The code uses the suggested configuration (see image attached) with 15 slots for pills with a front facing empty slot at all times, however the steps taken can be modified accordingly (1 slot = 137 steps, in our case)

Once power is supplied, an internal timer begins and counts until the defined time has been met. Once met, the motor will spin, a ping will be sent to the web server and the LCD will decrement the internal amount of pills held. This time can also be modified.

This example only allows for web functionality to turn off the LCD and LED as well as restart the countdown timer. I suggest you look into instead sending this info to the web server, with how long it took for a button, for example, to be pressed on the dispenser.
Then, you can use this data to generate analytics on how the user interacts with the product, providing tailored healthcare for users who struggle to remember their medication.

This code makes use of LiquidCrystal I2C libraries for the screen functionality.

Additional products include a 28BYJ-48 ULN2003 5V Stepper Motor utilising ULN2003 Driver Board to power the motor, as well as a FREENOVE I2C IIC LCD 1602 Module.

![image](https://github.com/user-attachments/assets/a99b89ac-50dd-4aa8-9aee-aed66149ba7d)
