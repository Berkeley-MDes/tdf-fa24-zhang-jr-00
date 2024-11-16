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
<div align="center">The robot detected the waste and then ate it</div><br><br>

Fallen Mode - "Ask for Help!": When tipped over, the IMU sensor detects this state, and the robot displays a sad expression, sending a notification to the user-end device to alert the user.<br>
<img width="1000" alt="Learning Rhino" src="assets/W9 3.png"><br>
<div align="center">The robot fell down and displayed a sad expression</div><br><br>

Help Received - "Smiling!": The robot expresses happiness when helped upright, showcasing its emotional response to user actions.<br>
<img width="1000" alt="Learning Rhino" src="assets/W9 4.png"><br>
<div align="center">The robot was helped by human and smiled</div><br><br>

Angry Mode: The robot looks visibly angry when overfilled with trash, encouraging users to empty it promptly.
<img width="1000" alt="Learning Rhino" src="assets/W9 5.png"><br>
<div align="center">Angry Mode</div><br><br>

Robot Eating Interaction (Web-end): I developed and tested the cloud component to enable real-time status updates for efficient bin capacity monitoring. This includes animations on the web interface and alerts like “robot is full” or “robot has fallen,” which are transmitted to a user-end Photon device. On the web-end interface, the robot is shown in an “eating” state with “Eating = 2” displayed at the top, and a banana peel in its mouth, symbolizing its waste collection action. This animation visually represents the robot’s engagement with waste placed in its compartment.
<img width="1000" alt="Learning Rhino" src="assets/W9 7.png"><br>
<div align="center">Robot Eating Interaction (Web-end)</div><br><br>

Robot's Death: When the robot reaches full capacity, it collapses with “WASTED” overlaying the image on the web-end interface, signaling to users that it cannot accept more waste and needs to be emptied.
<img width="1000" alt="Learning Rhino" src="assets/W9 8.png"><br>
<div align="center">Robot's Death</div><br><br>

Cloud and Cross-Device Communication: Phonton 2 Cloud is used to enable information uploading and also the communication of two Phonton 2 board. Using PuTTY, a serial communication tool, I identified and connected another Photon device to integrate these real-time updates effectively.
<img width="1000" alt="Learning Rhino" src="assets/W9 cloud.png"><br>
<div align="center">Using PuTTy to search for the second Phonton 2</div><br><br>


### 2. Speculations
#### 2.1 For the Tools
Future advancements in sensor technology, microcontrollers, and cloud connectivity could significantly enhance the functionality and responsiveness of systems like this smart trash-eating robot. More advanced sensors with built-in AI could allow the robot to distinguish different types of waste or detect finer details about its environment, improving both interaction and functionality. For example, integrating sensors with higher precision and better noise filtering could reduce false positives and improve overall reliability, particularly in complex environments. On the microcontroller side, devices with greater processing power and memory capacity could handle more complex algorithms and faster data processing, enabling smoother interactions and more responsive behavior in real-time. Additionally, advancements in cloud connectivity could support predictive maintenance, where the robot anticipates potential issues based on usage patterns and alerts users before problems arise, enhancing overall reliability.<br><br>

#### 2.2 For the Work
Future work in this area could explore more sophisticated user interactions, such as voice recognition, gesture detection, and dynamic emotional responses. For example, incorporating natural language processing could enable the robot to understand spoken commands, enhancing its interactivity and educational value. In public or commercial settings, the robot could engage users more actively, promoting waste disposal with encouraging messages or fun animations that make the experience more enjoyable. Additionally, more nuanced emotional expressions, possibly powered by machine learning, could allow the robot to adapt its responses based on user behavior, becoming “happier” when waste is disposed of correctly or showing “frustration” if left unattended. These developments could help foster a stronger connection between users and the robot, aligning with growing expectations that technology should be interactive, intuitive, and emotionally responsive.<br><br>

#### 2.3 Related Industry Example
A relevant industry example is Recycle Track Systems (RTS), a company that leverages technology to enhance waste management efficiency. RTS is a good example of how to build a comprehensive system for intelligent trash management, recycling, and reuse. By utilizing artificial intelligence and a proprietary tracking system, RTS provides hauling services for waste, recycling, organics, and bulk removal. Their system tracks materials as they travel to recycling or composting facilities, offering companies detailed reports on the amount of material recycled or composted. This approach highlights how integrated technologies, such as AI and data analytics, can improve waste sorting, tracking, and sustainability while ensuring proper waste diversion. RTS serves as a model for developing smart waste management ecosystems that combine operational efficiency with environmental responsibility.
<div align="center"><img width="1000" alt="Learning Rhino" src="assets/W9 rts.jpg"></div>
<div align="center">Recycle Track Systems (RTS) App</div><br><br>
