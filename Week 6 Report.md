# Week 6: Report 6 #
## Week of 10/3-10/10
### 1. Reflections

It was my first experience working with the Photon 2 and Stemma QT. I didn’t just follow the provided instructions—I took extra steps to enhance both the hardware and software components. Here is a detailed breakdown of my contributions and improvements:

#### Realize the Basic Funtion
<img width="1000" alt="Learning Rhino" src="assets/Week6/W6 IMU code1.png">

#### How I Improved and Tried New Functions

The main idea is controlling the brightness of an LED connected to **A5** based on the absolute value of the **ay** (acceleration on the Y-axis) from the MPU6050 sensor. To achieve this, I conducted the following steps for the software part:

- Limited the **ay** values to a range (-15000 to 15000) using `constrain()`.
- Mapped the absolute value of **ay** to a range suitable for PWM control (0 to 255). Since the `analogWrite()` function expects values between 0 (LED off) and 255 (maximum brightness), I mapped the constrained **ay** values to this range.
- Smoothed out the sensor values using a simple rolling average or a moving average to reduce noise.
- Controlled the brightness of the LED on **A5** using `analogWrite()` based on the mapped value from the sensor.
- Added feedback with the Serial Monitor to observe the **Smoothed ay** and **PWM** values.

Here is a diagram to show the main design:
<img width="1000" alt="Learning Rhino" src="assets/Week6/W6 Diagram of System.png">

And the following two pictures present the changed code.
<img width="1000" alt="Learning Rhino" src="assets/Week6/W6 IMU code1.png">
<img width="1000" alt="Learning Rhino" src="assets/Week6/W6 IMU code2.png">

For the physical circuit part, I:

- Placed the Photon 2 on a breadboard for circuit connections.
- Connected the LED positive to **A5**, with a resistor to protect the circuit.
- Connected the LED negative to **GND** through the breadboard.

Below are the pictures showing the improved feedback on the Serial Monitor and how the light becomes brighter when the absolute value of ay is high (when the IMU is almost vertical) and dimmer when the absolute value of ay is low (when the IMU is almost horizontal). **You can press [here](https://youtube.com/shorts/PtWXePgDtTs?feature=share) to watch the full video.**
   
   <img width="1000" alt="Learning Rhino" src="assets/Week6/W6 IMU(improved).png">
   <img width="1000" alt="Learning Rhino" src="assets/Week6/W6 IMU light low.jpg">
   <img width="1000" alt="Learning Rhino" src="assets/Week6/W6 IMU light high.jpg">


#### short summary

The system effectively controls the brightness of an LED based on the absolute value of the ay (Y-axis acceleration) from the MPU6050 sensor. As the IMU tilts vertically, the LED brightness increases smoothly, reaching its maximum when ay is high. Conversely, as the IMU moves closer to a horizontal position, the LED dims, with the brightness decreasing proportionally to the ay value. This setup allows for real-time and smooth adjustment of LED brightness based on the sensor's orientation.


### 2. Speculations
Looking ahead, I plan to further enhance my understanding of the Photon 2 IoT system by exploring more advanced features such as sensor integration and cloud-based data logging. One direction I foresee for future projects is leveraging real-time data analytics from the sensors connected to the system, which could be crucial for expanding into more complex IoT applications. Additionally, I would like to explore more efficient ways to configure the Photon 2 board and streamline the setup process to save time for myself and others. For instance, automating the network connection steps could reduce the effort required for IoT deployment. Another area of interest involves delving deeper into version management within VS Code and ensuring compatibility with the Photon 2 system. I also see value in creating tutorials or reference guides to help classmates and other learners overcome common challenges, such as configuration and debugging, which I experienced firsthand. 
