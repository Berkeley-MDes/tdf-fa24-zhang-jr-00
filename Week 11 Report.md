# Week 11: Report 11 #
## Week of 11/7-11/14
### 1. Reflections

This week, I concentrated on refining the 'MINI ME' agent by integrating all previous enhancements with a real-time internet search capability. This final experiment allowed the agent to access both personal knowledge and current public information, resulting in a fully adaptive, context-aware digital representation. By balancing internal knowledge with external data sources, I achieved a comprehensive system capable of responding accurately and relevantly. This milestone marks the completion of MINI ME's transformation into a digital twin that provides personalized, timely insights in response to complex queries.

<img width="1000" alt="Learning Rhino" src="assets/Week11 system architecture.png">
This diagram illustrates the overall architecture of the "MINI ME" LLM system. It showcases the primary components and their interactions within the system. The architecture is designed to enable seamless question answering by leveraging both a personalized knowledge base and external public sources, such as research papers, websites, and documents. Two distinct LLMs are integrated into this setup. The first LLM processes user inquiries, formatting them and determining if they require external data from public sources or if they can be answered solely within the personal knowledge base. The second LLM acts as the core of the system, executing the response generation based on the selected data sources. This architecture allows for a flexible, robust, and intelligent question-answering experience.


<img width="1000" alt="Learning Rhino" src="assets/Week11 system process.png">
This diagram illustrates the flow of how my "MINI ME" agent processes incoming queries. When a user submits a question, the Input Processing LLM first analyzes and categorizes the query. It then determines if the response requires external information (public sources) or if it can be handled internally using the personal knowledge base. This step ensures efficiency by directing queries appropriately, either to the knowledge base or to an internet search module. Through this flow, the system dynamically decides the best data sources to use for each query, ensuring relevant and comprehensive responses.


<img width="1000" alt="Learning Rhino" src="assets/Week11 detailed system flow.png">
This diagram shows the detailed system flow. The process starts with user input, where project details such as project number, URL, or year are provided. The input is then modified for structured processing, specifying conditions for the LLM’s response based on project parameters. The agent first queries a knowledge base to retrieve specific data points, using adjustable similarity and chunk parameters controlled by sliders. If relevant knowledge is not found internally, it performs an internet search. These results are then formatted and processed by a Core LLM, with prompts designed to ensure the response is framed professionally and contextually, referencing Jingru Zhang's work as appropriate. Finally, the output is generated and displayed in a designated output node, completing the information retrieval flow. This design leverages both internal and external data sources, ensuring comprehensive and accurate responses.


To achieve a sophisticated and well-functioning "MINI ME" agent, I conducted a series of experiments to test and refine specific elements of its design and functionality. Each experiment was essential in advancing the model toward its final, high-performing version.


#### 1.1 RAG Experiment
The first experiment focused on implementing Retrieval Augmented Generation (RAG) within the knowledge base. By experimenting with various data chunking and organization techniques, I was able to improve the agent's efficiency and accuracy in retrieving relevant information. This experiment highlighted the need for structured data flow, ensuring that the agent could generate coherent responses by accessing the most appropriate segments of knowledge.


#### 1.2 Achieving a Personalized Digital Twin with Comprehensive Insights
Through this configuration, MINI ME now acts as a true “digital twin,” capable of delivering nuanced responses that combine my personal data with relevant, up-to-date insights from the internet. When asked about suitable future projects, the agent suggested an interactive HCI installation, integrating my technical skills and ongoing research interests. This demonstrated the model’s ability to reflect my aspirations accurately and provide insightful suggestions.

3. Balancing Internal and External Knowledge Sources
The final experiment confirmed the utility of balancing personal and external knowledge sources. By using Retrieval Augmented Generation (RAG) and Google search, the agent can retrieve personal information while staying informed of recent trends and developments in my field. This balance is crucial for creating responses that are both accurate and contextually relevant, as MINI ME now addresses questions with a well-rounded perspective.
<img width="1000" alt="Learning Rhino" src="assets/Week7/Week7 diagram.png">
<img width="1000" alt="Learning Rhino" src="assets/Week7/Expression Design.png">
<img width="1000" alt="Learning Rhino" src="assets/Week7/Expression Design (2).png">


### 2. Speculations

Looking ahead, I plan to refine the responsiveness of the facial expressions based on the data from the ultrasonic sensor. A future goal is to have the animations change dynamically based on detected distances, such as a surprised expression when an object is detected at a close range. Additionally, I aim to explore more complex animation patterns, such as multi-stage eye movements and detailed expressions. Integrating these features with the Photon 2's capabilities could lead to a more interactive and engaging robotic interface. The industry is increasingly focusing on human-like interactions in robotics, as highlighted in recent articles on adaptive user interfaces. Incorporating real-time data from sensors into responsive animations can position this project in line with these trends, improving user experience and functionality.
