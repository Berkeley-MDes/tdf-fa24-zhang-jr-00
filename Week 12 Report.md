# Week 12: Report 12 #
## Week of 11/14-11/21
### 1. Reflections

During the first week of the FaceStory project, our team focused on establishing the foundational components necessary for developing a medical rehabilitation product aimed at patients with facial movement loss due to neurological conditions. A significant portion of our efforts was dedicated to data collection and sensor integration. The following two diagrams show the comprehensive structure and workflow of the our project "FaceStory". The System Architecture Diagram depicts how the neck-mounted wearable device, equipped with flex sensors and the Photon 2 microcontroller, integrates with machine learning models and the Unity-based interactive game interface, including the ChatGPT API for adaptive storytelling. Meanwhile, the Process Diagram outlines the flow of data from sensor input and data cleaning through the CNN model for accurate expression detection, culminating in real-time user feedback via a digital twin in Unity. Together, these diagrams illustrate the seamless interaction between hardware and software components that enable an effective and engaging facial rehabilitation experience.
<div align=center><img width="1000" alt="Learning Rhino" src="assets/Week12-13/Diagram1.png"></div>
<div align=center><img width="1000" alt="Learning Rhino" src="assets/Week12-13/Diagram2.png"></div>

We began by procuring various flex sensors from Amazon, experimenting with different lengths and structures to identify the most effective options for our application. This experimentation included testing multiple sensor placement methods on the neck—both vertically and horizontally—to determine which configuration best captures the subtle muscle movements associated with facial expressions. Using the Photon 2 microcontroller, we successfully integrated these sensors, allowing us to collect extensive datasets that accurately reflect muscle activity during different facial expressions.
<div align=center><img width="500" alt="Learning Rhino" src="assets/Week12-13/sensor1.jpg"></div>
<div align=center><img width="500" alt="Learning Rhino" src="assets/Week12-13/sensor2.jpg"></div>
<div align=center>The two pictures above show the different flex sensors we have tried.</div></br>

<div align=center><img width="1000" alt="Learning Rhino" src="assets/Week12-13/datacollection.jpg"></div>
<div align=center>This picture shows our data collection platform</div></br>

To ensure the reliability of our data, we employed Python for thorough data cleaning, removing any noise and inconsistencies that could impede model accuracy. With the cleaned data, we trained a Convolutional Neural Network (CNN) model, achieving an impressive accuracy rate of 99.14% in detecting and classifying facial expressions. This high level of accuracy validated our sensor setup and data processing pipeline, demonstrating the potential effectiveness of our machine learning approach in real-time expression detection.
<div align=center><img width="1000" alt="Learning Rhino" src="assets/Week12-13/dataprocessing.jpg"></div>
<div align=center>This picture shows the process of discussing about the data colllection and processing</div></br>

<div align=center><img width="1000" alt="Learning Rhino" src="assets/Week12-13/CNN.png"></div>
<div align=center>This picture shows the result of our CNN Model</div></br>

Additionally, we developed a comprehensive system architecture diagram to visualize the interaction between the wearable device, machine learning algorithms, and the Unity-based game interface. This diagram was instrumental in ensuring that all team members had a clear understanding of the project's overall structure and the flow of data within the system.

Assessing our progress, we successfully integrated the flex sensors with the Photon 2 microcontroller, established reliable data collection methods, and developed a highly accurate CNN model. These achievements set a strong foundation for the subsequent phases of the project, ensuring that our wearable device can effectively monitor and interpret facial muscle movements.



### 2. Speculations

Looking ahead, the FaceStory project is poised to significantly advance the field of facial rehabilitation through a combination of cutting-edge technologies. As we refine our Convolutional Neural Network (CNN) model, one of our primary focuses will be on exploring additional data augmentation techniques. This could involve not only traditional methods like rotation, flipping, and scaling, but also more sophisticated approaches such as synthetic data generation using Generative Adversarial Networks (GANs). By expanding the diversity of the data used to train our model, we expect to improve its generalization capabilities, leading to a model that can achieve higher accuracy and perform better across a broader range of real-world scenarios. Additionally, incorporating hybrid machine learning models, which combine the strengths of both CNNs and Recurrent Neural Networks (RNNs) or Attention Mechanisms, may allow us to capture temporal patterns in facial movements, further boosting the system’s effectiveness in real-time applications.

On the hardware side, one promising direction is the optimization of ergonomic sensor placement to improve user comfort. The challenge lies in ensuring that the sensors provide accurate data without causing discomfort or interfering with the user’s daily activities. In this regard, recent advances in flexible sensor technology are particularly relevant. Companies like FlexEnable and StretchSense are developing sensors that are both lightweight and highly conformable, which could be seamlessly integrated into FaceStory’s wearable devices. These sensors could conform to the contours of the face, offering a more comfortable, less intrusive experience, while maintaining the high-quality data required for effective rehabilitation. This type of wearable sensor is a critical component for the success of any rehabilitation device, as it enhances user compliance and engagement, ultimately leading to better outcomes.

Moreover, the data collected during the initial phase of the FaceStory project will be instrumental in shaping the development of the device moving forward. By analyzing how patients interact with the current prototype, we can identify pain points and areas for improvement. This data will guide our decisions regarding future hardware designs, user interface adjustments, and even customization options based on individual needs. Importantly, we plan to integrate continuous feedback loops into the design process, allowing us to iterate quickly and ensure that the device evolves in a way that maximally benefits users.

Ultimately, FaceStory’s success hinges on the combination of robust machine learning algorithms and innovative wearable technologies. We are committed to staying abreast of emerging industry trends, such as the rise of flexible and printed electronics, which will likely drive future iterations of our product. By marrying these advancements with our commitment to user-centered design, we believe FaceStory can transform facial rehabilitation, providing patients with a more comfortable, effective, and engaging treatment experience.

#### Relevant Industry Development:
A notable industry trend aligned with FaceStory's goals is the growth of flexible electronics and sensors in the medical device sector. For example, StretchSense, a leader in the development of flexible, stretchable sensors, has made significant strides in wearable health technologies. Their sensors are being used in applications ranging from motion capture to patient monitoring, enabling more comfortable and accurate tracking of physiological signals.

For more information, visit StretchSense’s recent developments here:https://stretchsense.com/

This development in flexible sensors could have a direct impact on FaceStory’s ability to create a more comfortable and effective facial rehabilitation device, contributing to increased patient engagement and better overall outcomes.
