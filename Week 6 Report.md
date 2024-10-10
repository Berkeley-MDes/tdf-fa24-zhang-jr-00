# Week 6: Report 6 #
## Week of 10/3-10/10
### 1. Reflections

It was my first experience working with the Photon 2 and Stemma QT. I didn’t just follow the provided instructions—I took extra steps to enhance both the hardware and software components. Here is a detailed breakdown of my contributions and improvements:

#### 1.1 Realize the Basic Funtion
This week, I tried to use the Stemma QT in my system. I first weld the related circuit, and then realized the basic funtion of the two Stemma QT sensors: APDS and IMU. The feedback on serial monitor shows the software and hardware both being set well and worked well.
<img width="1000" alt="Learning Rhino" src="assets/Week6/W6 weld.jpg">
<img width="1000" alt="Learning Rhino" src="assets/Week6/W6 apds.png">
<img width="1000" alt="Learning Rhino" src="assets/Week6/W6 apds2.jpg">

##### Debugging
One problem that confused me for a long time was that I failed to compile, even though I had already installed the related library. I tried both manually placing the library folder in the program and installing it with `pip install`, but both methods failed. So, I tried another approach: I used the relative path to include the library, like `#include "../lib/MPU6050/src//MPU6050.h"`. This is shown in the following picture.

<img width="1000" alt="Learning Rhino" src="assets/Week6/W6 lib.png">





#### 1.2 How I Improved and Tried New Functions

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

Below are the pictures showing the improved feedback on the Serial Monitor and how the light becomes brighter when the absolute value of ay is high (when the IMU is almost vertical) and dimmer when the absolute value of ay is low (when the IMU is almost horizontal). **You can press [here](https://youtu.be/rguRLTTPiGs) to watch the full video.**
   
   <img width="1000" alt="Learning Rhino" src="assets/Week6/W6 IMU(improved).png">
   <img width="1000" alt="Learning Rhino" src="assets/Week6/W6 IMU light low.jpg">
   <img width="1000" alt="Learning Rhino" src="assets/Week6/W6 IMU light high.jpg">


#### short summary

The system effectively controls the brightness of an LED based on the absolute value of the ay (Y-axis acceleration) from the MPU6050 sensor. As the IMU tilts vertically, the LED brightness increases smoothly, reaching its maximum when ay is high. Conversely, as the IMU moves closer to a horizontal position, the LED dims, with the brightness decreasing proportionally to the ay value. This setup allows for real-time and smooth adjustment of LED brightness based on the sensor's orientation.




### 2. Speculations

Building on the success of controlling the LED brightness based on acceleration data, future expansions of this system could include integrating additional sensor data to enhance interaction. For instance, the MPU6050 also provides gyroscope data, which could be used to create more complex lighting patterns or even gesture-based controls, enabling the user to manipulate lights or other outputs simply by moving the device in specific ways.

Additionally, this setup could be further enhanced by connecting it to external systems via Wi-Fi. The Photon 2's cloud connectivity could allow for remote monitoring of sensor data or control of the lights from a smartphone or web interface. This opens up possibilities for smart home applications, where the IMU could control room lighting based on movement or orientation of objects.

In terms of smoothing sensor data, advanced filtering algorithms, such as a Kalman filter, could be implemented to provide more precise control and reduce noise further, leading to a more stable output. Exploring different techniques to reduce the noise would also allow the system to be more reliable in real-world applications where environmental factors introduce variability.

A bonus opportunity would be adding RGB LED strips to this setup, allowing full-color lighting control based on the combination of the MPU6050's acceleration and gyroscope data. This could lead to artistic installations or dynamic lighting environments in interactive spaces.
