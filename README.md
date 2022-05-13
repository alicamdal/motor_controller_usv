# Motor Controller Scripts for USV
This repo contains motor controller scripts of the USV that is mentioned [here](https://github.com/alicamdal/yolov5_object_detection). BLDC motors are connected to Arduino Nano board. ESC class for the control can be found under folder called "motorController".
## Installing Libraries
Control device is Xbox One Controller. This gamepad's data can be readable with input library.
```
pip3 install input
```
## Motor Controller Code
BLDC Motors are connected to Arduino Nano. Related code is written on Arduino IDE. Code can initialize motors as left and right. "move" method can be called with parameters of region and angle.
For example; if joystick is in region one and angle is 60 degree, that means left motor will be ran with given throttle percentage and right motor will be mapped with related angle.
Also region three and four make device tank turn to left and right respectively.
## Data Sender
Data that obtained from Xbox One Controller, used to control the USV. Data is sent to Web Server using POST method. Region, angle, and thruster percentage can be changed.
