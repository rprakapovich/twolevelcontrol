We will use the Mobile Robot with the Two-Tier Control System to cover three topics:
1. To program a Raspberry Pi with Simulink.
2. To program Arduino Mega with Simulink.
3. To make Raspberry Pi and Arduino communicate with each other.

By the end of this description you will see a Mobile Robot programmed to detect and
follow a linear perspective point using Simulink Support Packages for Raspberry Pi and Arduino
Hardware.
1. Мodel HighLevel_RaspberryPi simulate the vision system that allows a mobile robot to
travel along straight road sections and corridors on the basis of linear perspective point detect.
Camera Board or web camera must have connected to Raspberry Pi.
2. Model LowLevel_Arduino simulate a simple closed-loop control algorithm which use the
difference between two encoder outputs to calculate the power that should be applied to each
wheel individually.
3. In this project Raspberry Pi and Arduino Mega communicate with each other through the
serial interface. However, despite the fact that the Raspberry Pi has the hardware parallel
interface (UART), but it is not among the Simulink’s blocks as that of Arduino. To solve this
problem for Raspberry Pi was developed the block of software parallel interface. But there is still
a problem: UART port Arduino powered by 5 V, and Raspberry - from 3.3 V. For this Raspberry Rx
pin was connected to the Arduino Tx pin through two resistors as shown in the pict.

For camera resolution at 320x240 pixels and UART port settings at 600-2400 baud rate was
obtained maximum of 4-8 frames per second.

The project includes the following files:

- **HighLevel_RaspberryPi.slx**;
- **LowLevel_Arduino.slx**.