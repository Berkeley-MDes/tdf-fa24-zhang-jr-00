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

The Process Diagram captures the flow of information through each stage of the project’s operation, from data collection to user interaction. It outlines key touchpoints such as trash detection, status monitoring, cloud data transmission, and user notifications. Each stage is labeled to highlight the sequence and logic of the system’s operation, illustrating how sensor inputs translate into outputs, such as robot facial expressions, movements, and user notifications on the web and user ends.
<img width="1000" alt="Learning Rhino" src="assets/W8 Process Diagram.png">
<div align="center">Process Diagram</div><br><br>


The Whole System Architecture Diagram provides a more detailed look at the system, including cloud communication and data flow details that emphasize the feedback loop for system monitoring. It shows how data flows seamlessly from the robot to the cloud and back to the user, ensuring smooth and reliable alerts when the bin is full or tipped over. This closed-loop system enhances both functionality and usability, supporting real-time data transmission and responsive actions.
<img width="1000" alt="Learning Rhino" src="assets/W8 detailed system architecture.png">
<div align="center">Detailed System Architecture</div><br><br>

#### 1.2 Mechanical Design
The mechanical system includes a linkage mechanism with two pivot points, two connection points, and three rigid links, enabling the robot to perform complex movements, such as opening its mouth and simulating “eating” with a single servo motor. The design emphasizes the testing, calibration, and refinement required to achieve precise and smooth movements, highlighting the mechanical sophistication of the smart trash bin.
<img width="1000" alt="Learning Rhino" src="assets/W8 mechanical design.png">
<div align="center">Mechanical Design</div><br><br>

#### 1.3 Ultrasonic and IMU Sensor Testing
To ensure accurate distance measurement and effective posture monitoring, I carefully evaluated the placement of the ultrasonic and IMU sensors and calibrated specific threshold values for optimal functionality. This testing was essential for reliable trash detection, internal waste capacity assessment, and monitoring the robot’s posture. By running continuous tests, I determined reasonable parameter values that allow the robot to execute specific actions when the ultrasonic sensor detects trash within a certain range.<br>
In particular, when the ultrasonic sensor detects waste within this defined range, the robot's code triggers the servo motor to perform coordinated movements, such as rotating the mechanical arm and opening the mouth. This process was refined through repeated testing (通过不断测试得出的合理数值), ensuring that the robot executes these movements smoothly and accurately whenever waste is detected. The screenshot displays the final parameter settings used for controlling the servo, demonstrating the fine-tuning necessary to achieve consistent and precise reactions during the trash collection process.
<img width="1000" alt="Learning Rhino" src="assets/W8 servo code.png">
<div align="center">Ultrasonic Parameter Settings to Control The Servo</div><br><br>

#### 1.4 Servo Functionality Testing
I experimented with various servo settings, ultimately setting optimal angles between 10-70 degrees to ensure smooth and responsive lid movements, enabling the robot to “eat” trash effectively. Additionally, I worked on connecting and controlling the servo with the Photon 2 board, as not all pins are compatible with servo control. The attached screenshot, referencing the Particle Photon guide, shows the steps I followed to attach the servo to a compatible pin and control its movement accurately, thus enhancing the mechanical functionality of the robot.
<img width="1000" alt="Learning Rhino" src="assets/W8 photon2 document.png">
<div align="center">Photon2 Document</div><br><br>

### 2. Speculations

For the tools, future advancements could focus on enhancing the sensor accuracy, microcontroller capabilities, and cloud communication systems used in smart trash bin applications. Given the importance of reliable sensor data (as seen in my ultrasonic and IMU sensor testing in sections 1.3 and 1.4), next-generation sensors might incorporate built-in AI processing for better noise reduction and precision, especially in complex or variable environments. More powerful microcontrollers, capable of managing multiple high-resolution sensors and processing real-time feedback with minimal latency, would also improve system responsiveness. Additionally, cloud-based tools could evolve to support seamless integration with IoT devices, allowing for more complex data processing and predictive maintenance features that prevent system errors before they occur.

For the work, future efforts might focus on expanding the smart bin’s ability to interact with users based on environmental data, such as user proximity, object recognition, and even verbal commands. For instance, integrating natural language processing could allow the bin to respond to spoken instructions or give feedback, enhancing user engagement. In customer service and public environments, emotionally responsive and interactive bins might become part of a larger smart infrastructure, encouraging waste disposal and promoting environmental awareness through interaction. Another potential area of focus could be developing more expressive and adaptive facial animations, drawing from my work on creating dynamic facial expressions that reflect the bin's status. These animations could become more nuanced, with the robot showing additional emotions like encouragement or surprise, depending on user actions and sensor input.

I also find a relevant industry example in this field: Recently, Bin-e(https://bine.world/), a Polish startup, developed a smart waste bin that uses AI for waste sorting and categorization, automatically identifying different types of waste for optimized disposal. Bin-e's technology combines sensors and AI processing to improve waste management efficiency, demonstrating how enhanced sensor integration and real-time data processing can transform waste disposal solutions. This development suggests a promising direction for similar projects, where smart bins not only categorize waste but also interact with users to improve waste disposal behavior. 
<div align="center"><img width="400" alt="Learning Rhino" src="assets/W8 bin-e.jpg"></div>
<div align="center">Bin-e</div><br><br>
