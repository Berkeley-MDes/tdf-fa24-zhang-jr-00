# Week 7: Report 7 #
## Week of 10/10-10/17
### 1. Reflections

This week, I concentrated on developing facial expression animations for a robotic display using the Photon 2. The process involved creating a smooth transition of expressions using the OLED display, focusing on movements like blinking and adjusting expressions such as smiling, cring, feeling curious, and being angry. Through this, I enhanced my understanding of animation techniques, such as transitioning shapes smoothly with simple trigonometric functions. Additionally, I explored the practical aspects of using an ultrasonic sensor for distance measurement and parameter testing. This helped me understand how to use sensor data to adjust animation parameters in real-time, ensuring the animations respond effectively to external stimuli. Overall, my progress this week has been substantial in both animation design and sensor integration, which has deepened my skills in programming and real-time debugging with the Photon 2.

#### 1.1 Designing the Facial Expression
First, I designed the logic behind the robot's facial expressions. After careful consideration, and based on the functions our robot needs to perform, I decided on four dynamic facial expressions: curiosity, happiness, anger, and sadness.<br><br>
The two diagrams below illustrate the Facial Expression Design Process. They explain the development of the robot's four emotional expressions (curiosity, happiness, anger, and sadness) and how each expression is triggered by different system states, such as the bin’s fullness level or stability. I created unique appearances for each expression and selected the best designs. Each expression was then carefully programmed and fine-tuned to reflect the robot's status, making it more interactive and engaging for users.
<img width="1000" alt="Learning Rhino" src="assets/Week7/Week7 diagram.png">
<img width="1000" alt="Learning Rhino" src="assets/Week7/Week7 expression design.jpg"><br><br>

Here are some reference images of facial expressions created with Midjourney. The image on the left serves as a reference for anger, while the one on the right represents sadness.
<div align="center">
<img width="500" alt="Learning Rhino" src="assets/Week7/Expression Design.png">
<img width="500" alt="Learning Rhino" src="assets/Week7/Expression Design (2).png">
</div><br><br>

#### 1.2 Programming and Fine Tuning
<img width="1000" alt="Learning Rhino" src="assets/Week7/Week7 algo.png">
<img width="1000" alt="Learning Rhino" src="assets/Week7/Week7 eye code.png">

<img width="1000" alt="Learning Rhino" src="assets/Week7/Week7 angry eye.png">
<img width="1000" alt="Learning Rhino" src="assets/Week7/Week7 sad eye.png">
<img width="1000" alt="Learning Rhino" src="assets/Week7/Week7 curious eye.jpg">
<img width="1000" alt="Learning Rhino" src="assets/Week7/Week7 smiling eye.jpg">

### 2. Speculations

Looking ahead, I plan to refine the responsiveness of the facial expressions based on the data from the ultrasonic sensor. A future goal is to have the animations change dynamically based on detected distances, such as a surprised expression when an object is detected at a close range. Additionally, I aim to explore more complex animation patterns, such as multi-stage eye movements and detailed expressions. Integrating these features with the Photon 2's capabilities could lead to a more interactive and engaging robotic interface. The industry is increasingly focusing on human-like interactions in robotics, as highlighted in recent articles on adaptive user interfaces. Incorporating real-time data from sensors into responsive animations can position this project in line with these trends, improving user experience and functionality.
