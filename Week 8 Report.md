# Week 8: Report 8 #
## Week of 10/18-10/24
### 1. Reflections

This week, I focused on several aspects of the smart trash bin project, including system architecture design, sensor testing, mechanical component optimization, and servo functionality. Through these tasks, I enhanced my skills in both hardware design and software integration, achieving a functional and interactive system that effectively manages waste and provides real-time feedback to users. I learned how to optimize communication between sensors, microcontrollers, and the cloud, and I developed efficient code to handle the bin’s status updates based on input from ultrasonic and IMU sensors. This experience deepened my understanding of real-time data processing and practical aspects of sensor calibration and feedback systems.

#### Designing the Logic
This week, I tried to use the Stemma QT in my system. I first weld the related circuit, and then realized the basic funtion of the two Stemma QT sensors: APDS and IMU. The feedback on serial monitor shows the software and hardware both being set well and worked well.
<img width="1000" alt="Learning Rhino" src="assets/Week7/Week7 diagram.png">
<img width="1000" alt="Learning Rhino" src="assets/Week7/Expression Design.png">
<img width="1000" alt="Learning Rhino" src="assets/Week7/Expression Design (2).png">


### 2. Speculations

Looking ahead, I plan to refine the responsiveness of the facial expressions based on the data from the ultrasonic sensor. A future goal is to have the animations change dynamically based on detected distances, such as a surprised expression when an object is detected at a close range. Additionally, I aim to explore more complex animation patterns, such as multi-stage eye movements and detailed expressions. Integrating these features with the Photon 2's capabilities could lead to a more interactive and engaging robotic interface. The industry is increasingly focusing on human-like interactions in robotics, as highlighted in recent articles on adaptive user interfaces. Incorporating real-time data from sensors into responsive animations can position this project in line with these trends, improving user experience and functionality.
