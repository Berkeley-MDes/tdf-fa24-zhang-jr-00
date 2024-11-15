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
I designed four distinct facial expressions for the robot, each requiring separate tasks assigned to the left and right eyes, which are displayed using OLED screens. By connecting the AD0 pins to ground and 3.3V, I was able to set unique addresses for each screen, allowing me to control each eye independently with specific commands.
To enhance the expressions and make them more charming, I carefully designed animation effects. This involved calculating and fine-tuning parameters in my code and iteratively adjusting them to achieve the desired look and smoothness.<br><br>
The following images and screenshots illustrate part of this process. For example, I calculated parameters to shape the 'angry' eyes as a rectangular trapezoid. For the 'curious' expression, I experimented with different eye positions to create a lively and endearing appearance.
<img width="1000" alt="Learning Rhino" src="assets/Week7/Week7 algorithm.png">
<div align="center">calculating parameters to shape the angry eyes</div><br><br>

<img width="1000" alt="Learning Rhino" src="assets/Week7/Week7 eye code.png">
<div align="center">fine tuning codes' parameters to realize the best animation effect</div><br><br>

The following pictures show the final result of the facial expressions. I used a Photon 2 to control two OLED screens, which serve as the robot's eyes. It has four dynamic facial expressions.
<img width="1000" alt="Learning Rhino" src="assets/Week7/Week7 angry eye.png">
<div align="center">angry eye</div><br><br>
<img width="1000" alt="Learning Rhino" src="assets/Week7/Week7 sad eye.png">
<div align="center">sad eye</div><br><br>
<img width="1000" alt="Learning Rhino" src="assets/Week7/Week7 curious eye.jpg">
<div align="center">curious eye</div><br><br>
<img width="1000" alt="Learning Rhino" src="assets/Week7/Week7 smiling eye.jpg">
<div align="center">smiling eye</div><br><br>

### 2. Speculations

In the near future, developments in robot facial expression technology are likely to focus on enhancing emotional depth and responsiveness.

For the tools, advancements in OLED displays and sensor integration will enable more sophisticated hardware for creating expressive robots. Higher-resolution displays and more compact, precise actuators will allow robots to exhibit realistic and flexible facial movements. Additionally, the use of advanced machine learning algorithms will empower robots to dynamically adapt their facial expressions based on user interactions, allowing them to convey complex emotions, such as empathy or surprise, in response to specific stimuli.

For the work, future efforts will likely concentrate on integrating real-time data processing to enhance robots' responsiveness to environmental cues, such as voice tone or body language, making interactions more personalized and lifelike. This approach could be especially valuable in fields like customer service and elder care, where emotionally intelligent robots might improve user experience, ease social isolation, or assist with daily tasks. Additionally, expressive robots may be increasingly applied in educational and therapeutic contexts, supporting children’s social development or providing companionship to individuals in need.

Here is a relevant news/industry item: a recent development in this field is the work of Ex-Robots, a company based in Dalian, China, which has been creating humanoid robots with advanced facial expressions. By using custom software and AI algorithms, Ex-Robots has enabled its robots to mimic human facial movements accurately, enhancing expressiveness and interactivity. Currently displayed in museums, these robots are expected to find applications in healthcare and education, such as psychological counseling and services for children. Here is a link for the news: https://www.reuters.com/technology/chinas-ex-robots-develops-humanoids-with-enhanced-facial-movement-2024-06-11/?utm_source=chatgpt.com

<img width="1000" alt="Learning Rhino" src="assets/Week7/W7 news image.jpg">
<div align="center">A humanoid robot stands at the office of developer Ex-Robots in Dalian, Liaoning province, China June 6, 2024</div><br><br>

In summary, the future of expressive robotics seems promising, with potential applications across various industries. As tools for designing and animating robot faces become more advanced and widely accessible, robots will likely become more intuitive and empathetic, bridging the gap between machine functionality and human emotion in a variety of professional and social settings.
