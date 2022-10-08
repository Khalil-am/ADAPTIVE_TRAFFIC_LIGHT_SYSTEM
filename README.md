# ADAPTIVE_TRAFFIC_LIGHT_SYSTEM
This system was built on a PIC16F877A Microcontroller

Adaptive traffic light, which will act like a smart traffic light which can determined the traffic crisis in each route by a sensor and give the priority for the congested route by give this route the longest opening time. In other word it will give each route opening time that suitable for the number of car in this road.

System description 
Now I will describe the system in deep details. There are two mode of work:
    1) Regular. 
    2) Emergency. 
The regular mode consist of two sub-mode of work:
1.	Single : one open road at the time 
2.	Double : two opposite roads open at the time 
I have a pushbutton to move between regular and emergency mode, this Pushbutton connect to RB0 to rise an interrupt, the interrupt subroutine flip the first bit in MODE (define by me) register which use to indicate the state of work. 

In emergency case the system will turn on green led and turn off red led for a period of time then it will flip the situation (red and green lights on all ways are flashed). I chose the flashing time to be 1second.   

The regular mode has two mode of operation as we mention earlier, and I have a switch use to move between single and double mode, if the switch is closed, then the system will be in double mode, and if it is opened ,then the system will be in single mode. In single mode the system permit one road to be open at the time and the time it will be open depend on  number of car in road (proportional) and in double mode two opposite roads can be open for a period of time depend on more crisis  road between it.

 Now I will explain essential information which must be clear:
 
•	Minimum time assigned to any road will be 1 second.
•	The sum of all road time must not exceed 10 second (maximum time for a round).
•	I chose time in emergency for flashing to be 1 second.
•	In double mode the time for opposite roads to be open equal to the longest time between them.
•	will replace the sensor by a potentiometer.
•	will make the time that assigned for any road between 1s to 8s

