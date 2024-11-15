# Week 8: Report 8 #
## Week of 10/18-10/24
### 1. Reflections

This week, I made significant progress in understanding the complexities of integrating hardware and software to create an interactive and autonomous system. What I learned included the intricate interactions required between various sensors, microcontrollers, and cloud services to create a responsive trash bin. I deepened my knowledge of system architecture design, cloud communication, and sensor calibration. Specifically, I learned how to use ultrasonic and IMU sensors effectively to monitor both the trash level and the stability of the bin, which are crucial for triggering accurate system responses.<br>

How I learned these skills involved a combination of hands-on testing, iterative adjustments, and extensive reference to technical documentation. For example, testing different sensor placements and threshold settings helped me understand the real-time responsiveness of the system. I also consulted the Photon 2 reference guide to troubleshoot servo connectivity issues, which allowed me to ensure that the bin's mechanical movements were both smooth and reliable. This iterative process of learning through doing and refining based on results was essential in optimizing the bin’s responses.<br>

Assessment of the current state of the work shows that the project is on a solid path toward achieving its objectives. The system architecture is fully designed and tested, and all primary components—sensor integration, cloud connectivity, and mechanical functionality—are functioning as expected. While there are still opportunities for further refinement, such as enhancing the bin’s emotional feedback for user engagement, the core functionalities are stable and reliable. This week’s progress has established a strong foundation, setting up the next stages of fine-tuning and expanding the bin's interactive features to create a more engaging and efficient waste management solution.<br><br>



#### 1.1 Diagram Analysis
The System Architecture Diagram presents a high-level overview of the digital ecosystem that powers the smart trash bin. It identifies key components, including sensors, microcontrollers, cloud communication, and user interfaces, and represents the flow of information with directional arrows. For instance, data from the ultrasonic sensors (used for trash level detection) and the IMU sensor (used for posture monitoring) flows to the microcontroller, which triggers system responses based on the bin’s status (e.g., full, fallen). This data is then sent to the cloud, enabling real-time user notifications on both the web and user ends (through another Photon 2 and LED).
<img width="1000" alt="Learning Rhino" src="assets/W8 system architecture.png">
<div align="center">System Architecture Diagram</div><br><br>


Process Diagram
The Process Diagram captures the flow of information through each stage of the project’s operation, from data collection to user interaction. It outlines key touchpoints such as trash detection, status monitoring, cloud data transmission, and user notifications. Each stage is labeled to highlight the sequence and logic of the system’s operation, illustrating how sensor inputs translate into outputs, such as robot facial expressions, movements, and user notifications on the web and user ends.

Whole System Architecture
The Whole System Architecture Diagram provides a more detailed look at the system, including cloud communication and data flow details that emphasize the feedback loop for system monitoring. It shows how data flows seamlessly from the robot to the cloud and back to the user, ensuring smooth and reliable alerts when the bin is full or tipped over. This closed-loop system enhances both functionality and usability, supporting real-time data transmission and responsive actions.


### 2. Speculations

Looking ahead, I plan to refine the responsiveness of the facial expressions based on the data from the ultrasonic sensor. A future goal is to have the animations change dynamically based on detected distances, such as a surprised expression when an object is detected at a close range. Additionally, I aim to explore more complex animation patterns, such as multi-stage eye movements and detailed expressions. Integrating these features with the Photon 2's capabilities could lead to a more interactive and engaging robotic interface. The industry is increasingly focusing on human-like interactions in robotics, as highlighted in recent articles on adaptive user interfaces. Incorporating real-time data from sensors into responsive animations can position this project in line with these trends, improving user experience and functionality.
