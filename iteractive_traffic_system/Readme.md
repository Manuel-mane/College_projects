# Interactive Traffic System

### Abstract

Interactively changing the street rails according to the traffic demand is a resource that some cities are already implementing to improve their traffic flow. This project consists
in building a traffic system that allows streets, roads, and rails intersections signaling to adjust to real-time traffic conditions. An embedded system with Wi-Fi interface can
be used to build a system capable of reading the traffic needs, adapting the rails lane accordingly. In addition, this system interacts with the city first responder units such 
as the NYFD who would have the capabilities to manipulate traffic signals and streets lines. These will allow them to create the condition for a better circulation and to improve 
arrival time.

A train crossroad system is be proposed as well to provide an emergency system for vehicles stuck in the line when trains approach. 

### Objectives

•	To develop a traffic and street rail system that will be able to read real-time traffic conditions and makes the necessary adjustments to alleviate congestions and improve the
traffic flow. 

•	To develop an interface for first-responders that will allow them to communicate with the system and to override street-way directions and traffic signaling conditions.

•	To develop a train-crossroad system that will includes an emergency module. This safety mechanism will trigger in the event a vehicle or object blocks the crossroad as a train 
approaches. 

Introduction

Understanding the volume of vehicles in the road will be possible by the utilization of sensors located in both sides of the street (e.g. North and South). The sensors reading
will generate a count. This data will be periodically analyzed and compared. If a threshold is cross, the system will decide if a lane needs to be taken from the side of the 
road with the least traffic-volume and to re-assign it to the busy side of the road. The extra lane will help to ease traffic flow and reduce congestion.

A web server/client interface will be developed between the lane sensors and the rail controls to display their performances. Emergency vehicles will have access to this control
interface to modify the lanes as they need

A second interface will be developed for the crossroad system. It will provide a safety mechanism in the event a car or any other object stalls in the crossroad as the train 
approaches. The system will communicate with the crossroad-sensor to ensure there are not vehicles or objects stalled in the way. If the cross road is blocked, an alert will 
be sent to the train engineer which will pop on the web interface. This will allow the conductor to stop the train in time to avoid a collision.  The system will proceed to r
eturn to service once the emergency and the road is cleared. 

A major challenge in the system design is the development of a bi-directional notification interface between the system, the drivers on the road, and other public agencies. 
Additional considerations will be taking into account when implement changes in street rails and other traffic signs. These changes have to proceed smoothly to avoid confusions 
that could provoke accidents. When it comes to the web interface, this needs to be user-friendly and functional.

### Methodology and Design 

 The project consists on two modules: 
 
•	Street Rail Module

•	Cross Road Module

Figure 1 shows the representation of both modules and their basic design:

[!](/documentation/images.docs/lines_drawn)

**Street Rails Module**

The Street Rails Module consists of four rails (Figure 1). The directions of the rail direction are identified as North or South. Their configuration, depending of the 
automatic traffic reading, and the manual web interface (Figure 2) can take the following structures:

1.	SOUTH – SOUTH – NORTH – NORTH

2.	SOUTH – NORTH – NORTH – NORTH

3.	SOUTH – SOUTH – SOUTH – NORTH

4.	SOUTH – CLOSED - NORTH – NORTH

5.	SOUTH – SOUTH – CLOSED – NORTH

6.	SOUTH – CLOSED – CLOSED – NORTH

The equipment used for the design of this module consists of:

![images](documentation/images.doc/lines drawn.jpg)

•	Arduino platforms such as MKR1000 and ESP32

•	IR sensors

•	LCD screens

•	LEDs

The web server interface (Figure 2) provides the possibility of manually control the rail’s directions. Besides, it will a “close for emergency” feature that will allow the 
shut of rails because of emergency vehicles approaching. 



