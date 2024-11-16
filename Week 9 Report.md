# Week 9: Report 9 #
## Week of 10/25-10/31
### 1. Reflections

#### 1.1 What I’ve Learned
This week, I deepened my understanding of integrating multiple engineering disciplines by working on the smart trash-eating robot. Specifically, I learned about sensor calibration, real-time data processing, and cross-device communication. Calibrating the ultrasonic and IMU sensors to detect the robot's state (e.g., waste levels, fallen condition) presented challenges, but testing and refining threshold values allowed me to achieve accurate readings for various bin conditions. I also expanded my knowledge of cloud-based data transfer and device communication by successfully setting up alerts that notify users when the robot is full or has fallen over. This cross-device connectivity improved my ability to design and troubleshoot a cloud-based IoT system, which is critical for achieving real-time user feedback.

#### 1.2 Current State of the Project
The project is now in an advanced prototype stage, where the core functions are fully integrated and tested. The robot effectively responds to waste placement, activates emotional feedback, and sends real-time status updates to the cloud. These updates are communicated to a user-end Photon device, which triggers a blinking LED as a visual alert. Additionally, I developed a web-end interface where users can view animations that reflect the robot’s current state, such as “Eating” or “WASTED” when the bin is full. The robot's mechanical functionality is also optimized; it smoothly opens its lid when waste is detected and closes it upon completion, with emotional responses displayed based on the robot’s internal state (e.g., happy, angry, sad). Overall, the system demonstrates a user-friendly and engaging approach to waste management, encouraging users to dispose of trash responsibly.

#### 1.3 Demonstrations and Outcomes
Waste Collection Mode: When the robot detects waste, it will open its lid in response to waste detection, showing active engagement and response to user interaction.<br>
<div align="center">
<img width="500" alt="Learning Rhino" src="assets/W9 1.png">
<img width="500" alt="Learning Rhino" src="assets/W9 2.png">
</div>
<div align="center">The robot detect the waste and then eat it</div><br><br>

Fallen Mode - "Ask for Help!": When tipped over, the IMU sensor detects this state, and the robot displays a sad expression, sending a notification to the user-end device to alert the user.<br>
<img width="500" alt="Learning Rhino" src="assets/W9 3.png">
Help Received - "Smiling!": The robot expresses happiness when helped upright, showcasing its emotional response to user actions.<br>
<img width="500" alt="Learning Rhino" src="assets/W9 4.png">


Angry Mode: The robot looks visibly angry when overfilled with trash, encouraging users to empty it promptly.
Robot Full State - "WASTED": When full, the robot collapses on the web-end display with “WASTED” overlaid, clearly indicating it needs emptying.
Robot Eating Interaction (Web-end): On the web-end interface, the robot is shown in an “eating” state with “Eating = 2” displayed at the top, and a banana peel in its mouth, symbolizing its waste collection action. This animation visually represents the robot’s engagement with waste placed in its compartment.
Robot Full State - "WASTED": When the robot reaches full capacity, it collapses with “WASTED” overlaying the image on the web-end interface, signaling to users that it cannot accept more waste and needs to be emptied.
Cloud and Cross-Device Communication: I developed and tested the cloud component to enable real-time status updates for efficient bin capacity monitoring. This includes animations on the web interface and alerts like “robot is full” or “robot has fallen,” which are transmitted to a user-end Photon device. An LED indicator provides visual feedback on the robot’s status. Using PuTTY, a serial communication tool, I identified and connected another Photon device to integrate these real-time updates effectively.


### 2. Speculations
#### 2.1 For the Tools
Future advancements in sensor technology, microcontrollers, and cloud connectivity could significantly enhance the functionality and responsiveness of systems like this smart trash-eating robot. More advanced sensors with built-in AI could allow the robot to distinguish different types of waste or detect finer details about its environment, improving both interaction and functionality. For example, integrating sensors with higher precision and better noise filtering could reduce false positives and improve overall reliability, particularly in complex environments. On the microcontroller side, devices with greater processing power and memory capacity could handle more complex algorithms and faster data processing, enabling smoother interactions and more responsive behavior in real-time. Additionally, advancements in cloud connectivity could support predictive maintenance, where the robot anticipates potential issues based on usage patterns and alerts users before problems arise, enhancing overall reliability.

#### 2.2 For the Work
Future work in this area could explore more sophisticated user interactions, such as voice recognition, gesture detection, and dynamic emotional responses. For example, incorporating natural language processing could enable the robot to understand spoken commands, enhancing its interactivity and educational value. In public or commercial settings, the robot could engage users more actively, promoting waste disposal with encouraging messages or fun animations that make the experience more enjoyable. Additionally, more nuanced emotional expressions, possibly powered by machine learning, could allow the robot to adapt its responses based on user behavior, becoming “happier” when waste is disposed of correctly or showing “frustration” if left unattended. These developments could help foster a stronger connection between users and the robot, aligning with growing expectations that technology should be interactive, intuitive, and emotionally responsive.



<img width="1000" alt="Learning Rhino" src="assets/W8 mechanical design.png">
<div align="center">Mechanical Design</div><br><br>







I also find a relevant industry example in this field: Recently, Bin-e(https://bine.world/), a Polish startup, developed a smart waste bin that uses AI for waste sorting and categorization, automatically identifying different types of waste for optimized disposal. Bin-e's technology combines sensors and AI processing to improve waste management efficiency, demonstrating how enhanced sensor integration and real-time data processing can transform waste disposal solutions. This development suggests a promising direction for similar projects, where smart bins not only categorize waste but also interact with users to improve waste disposal behavior. 
<div align="center"><img width="400" alt="Learning Rhino" src="assets/W8 bin-e.jpg"></div>
<div align="center">Bin-e</div><br><br>
