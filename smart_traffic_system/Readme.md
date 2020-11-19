# Smart Traffic Light System

## Abstract

The intended system tries to alleviate these congestions problems by making traffic lights adaptable to real-time traffic conditions. This will allow traffic to flow continuously 
in one direction or other based on the need. This can be achieved using existing technology such as, infrared sensors, Wi-Fi, GPS, cameras, and system controllers. Example, 
infrared sensors can detect traffic on the road and send a command to the traffic light via Wi-Fi to change the duration of the light. In addition, the system can interact with 
the cities first-responders units such as the NYFD whom could take control of the system and override the lights sequence.

## Objectives

The purpose of this project is to develop a traffic light system that could adapt to real-time road conditions. The system will be able to detect traffic congestion and adjust the
timing of the traffic lights. This will allow cars (drivers) to move in one direction or the other preventing possible traffic congestion. First responders will be able to 
communicate with the system wirelessly to overwrite the light sequence, if necessary. This capability will allow emergency personal to take control of the light signals of the 
upcoming intersection and to clear the traffic upon their pass.

## Methodology and Design

The goal is to design and develop a working prototype of a smart traffic light system. The system will be developed using an Arduino Mega 2560 platform, Arduino wireless module, 
IR sensors, and other electronic elements such as LEDs, resistors and LCD screen. Sensors are critical for the design. IR sensor will determine the presence of vehicles on the
road. The 1 or 0 condition will determine the operation of the controller.

In addition to the hardware, the programming of the smart units will be achieved by using Arduino IDE 1.8.8. The code (sketch) and behavior of the traffic light system will 
consist of four different modules: 

1)	Screen Module: In this module presents the behavior of the screen LCD using an Arduino/Genuino MKR1000. 

2)	Traffic Light Module: Using the Arduino Mega 2500, the behavior is the following: When cars approximate any side of the street, and therefore will be sensed by the IR 
sensors, the traffic light will proceed to a state of working, and it will change its light (green) to give pass to the coming vehicles: This module is divided in three 
situations:

a)	Situation A: Vehicles are coming by one of the sides of the intersection: traffic light will proceed to access the pass (green light) to this side meanwhile there are not 
vehicles coming by the other side. If cars approach the other side of the street as well, the traffic lights will proceed to situation B; if vehicles are only coming by one 
side of the street, the traffic light will keep the green on until the situation changes. On the other side, if cars stop coming from both sides of the intersection, the traffic
lights condition will go back to Null Module.

b)	Situation B: Vehicles coming from both sides of the intersection: In this case, the traffic lights will proceed to access pass to both sides of the intersection (normal 
condition) in a timely-equal way. If cars stop coming by one side of the intersection, the traffic lights will proceed to situation A and they will only give pass to one side 
of the intersection until the situation changes. It vehicles stop coming from both sides of the intersection, the traffic lights will go to Null Module.

c)	Situation C: When there are not vehicles coming by any side of the street, the traffic lights will acquire a null state, where both traffic lights will be blinking the 
yellow light with a two seconds timer.

3)	Emergency Module: Through the Arduino Wireless Module (Arduino/Genuino MKR1000), emergency vehicles will send a signal to the traffic light system and the switch (Switch1 
and Switch2) will activate. In this case, the emergency mode will activate, and will overwrite the traffic light systems. The traffic light system will proceed to give access 
to the side of the intersection the emergency vehicle is coming to clean its way through. 

4)	WiFi Module: Using the Arduino/Genuino MKR1000, with a WiFi program, the emergency vehicles will be able to send a signal when they are approaching the intersection. Once 
the signal is sent, this board will communicate with the Arduino Mega 2500 and the Emergency Module (emergency state) will activate overwriting the rest of the traffic light 
system.



