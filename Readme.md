This repo describe the two major Capstone projects I developed in my college major of Bachelor of Telecommunications Technology.

## Project 1: Smart Traffic Light
`Spring 2019 (February 2019 - June 2019)`

The purpose of this project is to develop a traffic light system that could adapt to real-time road conditions. The system will be able to detect traffic congestion and adjust 
the timing of the traffic lights. This will allow cars (drivers) to move in one direction or the other preventing possible traffic congestion. First responders will be able to 
communicate with the system wirelessly to overwrite the light sequence, if necessary. This capability will allow emergency personal to take control of the light signals of the 
upcoming intersection and to clear the traffic upon their pass.

Methodology and Design
The goal is to design and develop a working prototype of a smart traffic light system. The system will be developed using an Arduino Mega 2560 platform, Arduino wireless module, 
IR sensors, and other electronic elements such as LEDs, resistors and LCD screen. Sensors are critical for the design. IR sensor will determine the presence of vehicles on the
road. The 1 or 0 condition will determine the operation of the controller.

In addition to the hardware, the programming of the smart units will be achieved by using Arduino IDE 1.8.8. The code (sketch) and behavior of the traffic light system will 
consist
of three different modules: 

### 1)  Screen Module

In this module presents the behavior of the screen LCD using an Arduino/Genuino MKR1000.

### 2) Traffic Light Module

Using the Arduino Mega 2500, the behavior of the traffic light is the following: When cars approximate any side of the street, and therefore will be sensed by the IR sensors, 
the traffic lights will go through different states depending of the outside input of the sensors changing its behavior as well. This module is mainly divided in three states 
or situations:

**State A** “Vehicles coming from one of the sides of the intersection”
In this state, the sensor will alert the system that vehicles are approaching one side of the intersection. The system will proceed to give it pass to them according to the 
sensor information, changing the traffic light to pass state (green light) and it will keep it always than are not vehicles approaching from the other side of the intersection 
as well or vehicles stop approaching.

**State B**: “Vehicles coming from both sides of the intersection”

In this states, the system will manage the traffic lights to behave in a way that both intersections are granted their pass in a timely-equal way. If cars stop coming by one 
side of the intersection, the traffic lights will proceed to State A and they will only give pass to one side of the intersection until the situation changes. It vehicles stop 
coming from both sides of the intersection, the traffic lights will go to State C.

**State C:** “No vehicles”

When there are not vehicles coming by any side of the street, the traffic lights will acquire a null state, where both traffic lights will be blinking the yellow light with a 
two seconds timer.

### 3)Emergency Module

Through the Arduino Wireless Module (Arduino/Genuino MKR1000), using a wifi connection, emergency vehicles will send a signal to the traffic lights system. This signal will 
activate an interruption in the system overwriting the program passing to an emergency state. This state, according to where the emergency signal is coming from (side of the 
intersection) will activate the traffic lights to facilitate the pass of such vehicles, stopping the flow of vehicles for the other side of the intersection and granting the 
pass to the side of the intersection where the emergency vehicle is coming from, clearing its way. Through the Screen Module, the drivers will be alert of an emergency vehicle 
approaching to the intersection as well. 

## Project2: Interactive Traffic System

`Fall 2019 (August 2019 - December 2019)`

### Objectives

•	To develop a traffic and street rail system that will be able to read real-time traffic conditions and makes the necessary adjustments to alleviate congestions and improve the
traffic flow. 

•	To develop an interface for first-responders that will allow them to communicate with the system and to override street-way directions and traffic signaling conditions.

•	To develop a train-crossroad system that will includes an emergency module. This safety mechanism will trigger in the event a vehicle or object blocks the crossroad as a train
approaches. 

### Methodologies

Understanding the volume of vehicles in the road will be possible by the utilization of sensors located in both sides of the street (e.g. North and South). The sensors reading 
will generate a count. This data will be periodically analyzed and compared. If a threshold is cross, the system will decide if a lane needs to be taken from the side of the 
road with the least traffic-volume and to re-assign it to the busy side of the road. The extra lane will help to ease traffic flow and reduce congestion.

A web server/client interface will be developed between the lane sensors and the rail controls to display their performances. Emergency vehicles will have access to this 
control interface to modify the lanes as they need.

A second interface will be developed for the crossroad system. It will provide a safety mechanism in the event a car or any other object stalls in the crossroad as the train 
approaches. The system will communicate with the crossroad-sensor to ensure there are not vehicles or objects stalled in the way. If the cross road is blocked, an alert will be 
sent to the train engineer which will pop on the web interface. This will allow the conductor to stop the train in time to avoid a collision.  The system will proceed to return 
to service once the emergency and the road is cleared. 

A major challenge in the system design is the development of a bi-directional notification interface between the system, the drivers on the road, and other public agencies. 
Additional considerations will be taking into account when implement changes in street rails and other traffic signs. These changes have to proceed smoothly to avoid confusions 
that could provoke accidents. When it comes to the web interface, this needs to be user-friendly and functional.

**The project consists on two modules: **

•	Street Rail Module

•	Cross Road Module

**The equipment used for the design of this module consists of:**

•	Arduino platforms such as MKR1000 and ESP32

•	IR sensors

•	LCD screens

•	LEDs






