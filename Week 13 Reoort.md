# Final Week: Report 13 #
## Week of 12/02-12/05
### 1. Reflections

This week, I concentrated on refining the 'MINI ME' agent by integrating all previous enhancements with a real-time internet search capability. This final experiment allowed the agent to access both personal knowledge and current public information, resulting in a fully adaptive, context-aware digital representation. By balancing internal knowledge with external data sources, I achieved a comprehensive system capable of responding accurately and relevantly. This milestone marks the completion of MINI ME's transformation into a digital twin that provides personalized, timely insights in response to complex queries.<br><br>

<div align=center><img width="500" alt="Learning Rhino" src="assets/Week11 system architecture.png"></div>
This diagram illustrates the overall architecture of the "MINI ME" LLM system. It showcases the primary components and their interactions within the system. The architecture is designed to enable seamless question answering by leveraging both a personalized knowledge base and external public sources, such as research papers, websites, and documents. Two distinct LLMs are integrated into this setup. The first LLM processes user inquiries, formatting them and determining if they require external data from public sources or if they can be answered solely within the personal knowledge base. The second LLM acts as the core of the system, executing the response generation based on the selected data sources. This architecture allows for a flexible, robust, and intelligent question-answering experience.<br><br>


<div align=center><img width="500" alt="Learning Rhino" src="assets/Week11 system process.png"></div>
This diagram illustrates the flow of how my "MINI ME" agent processes incoming queries. When a user submits a question, the Input Processing LLM first analyzes and categorizes the query. It then determines if the response requires external information (public sources) or if it can be handled internally using the personal knowledge base. This step ensures efficiency by directing queries appropriately, either to the knowledge base or to an internet search module. Through this flow, the system dynamically decides the best data sources to use for each query, ensuring relevant and comprehensive responses.<br><br>


<div align=center><img width="1000" alt="Learning Rhino" src="assets/Week11 detailed system flow.png"></div>
This diagram shows the detailed system flow. The process starts with user input, where project details such as project number, URL, or year are provided. The input is then modified for structured processing, specifying conditions for the LLM’s response based on project parameters. The agent first queries a knowledge base to retrieve specific data points, using adjustable similarity and chunk parameters controlled by sliders. If relevant knowledge is not found internally, it performs an internet search. These results are then formatted and processed by a Core LLM, with prompts designed to ensure the response is framed professionally and contextually, referencing Jingru Zhang's work as appropriate. Finally, the output is generated and displayed in a designated output node, completing the information retrieval flow. This design leverages both internal and external data sources, ensuring comprehensive and accurate responses.
<br><br>

To achieve a sophisticated and well-functioning "MINI ME" agent, I conducted a series of experiments to test and refine specific elements of its design and functionality. Each experiment was essential in advancing the model toward its final, high-performing version.


#### 1.1 RAG Experiment
The first experiment focused on implementing Retrieval Augmented Generation (RAG) within the knowledge base. By experimenting with various data chunking and organization techniques, I was able to improve the agent's efficiency and accuracy in retrieving relevant information. This experiment highlighted the need for structured data flow, ensuring that the agent could generate coherent responses by accessing the most appropriate segments of knowledge.
<div align=center><img width="1000" alt="Learning Rhino" src="assets/Week11 rag experiment.png"></div>
<div align=center><img width="1000" alt="Learning Rhino" src="assets/Week11 rag experiment2.png"></div>
These two screenshots show the knowledge base configuration experiment and monitoring interface. In the first image, various chunking and overlap settings were tested to find an optimal structure, ultimately selecting a setup of 200 tokens per chunk with 200 tokens of overlap. This configuration enhances contextual understanding by allowing MINI ME to maintain coherence across segments while balancing retrieval efficiency, enabling quick access to relevant information without losing context. In the second image, the monitoring interface demonstrates the agent’s success in retrieving key information from the personalized database, accurately locating and presenting relevant details from Jingru’s curated content to support precise, contextually relevant responses.<br><br>


#### 1.2 External Source Search Experiment
This experiment explored the integration of external search capabilities through Google. This feature allowed the agent to access real-time public information, supplementing the internal knowledge base with up-to-date data from the internet. By incorporating Google search, the agent could provide richer and more comprehensive responses, especially for questions requiring broader context beyond its static data. This experiment illustrated the agent’s adaptability in balancing internal knowledge with relevant external sources, enhancing its responses to be both informed and current.<br>
<div align=center><img width="1000" alt="Learning Rhino" src="assets/Week11 google search.png"></div>
This image shows the agent’s monitoring process during an external Google search. The agent successfully locates a relevant website and provides a coherent description of its content, demonstrating its ability to not only retrieve information from public sources but also interpret and present it in a meaningful way. This capability highlights the agent's understanding and synthesis of external information to complement its personalized knowledge base.<br><br>

#### 1.3 Project Outcome
The "MINI ME" Project demonstrates a balanced use of personalized knowledge and external data, achieving a level of interaction that feels genuinely responsive and comprehensive. This project highlights my dedication to exceeding requirements, as I designed an agent that mirrors my own expertise and insights while remaining adaptable to broader information contexts. By combining RAG, variables, real-time search, and context-aware variables, I successfully created a digital representation of myself that is capable of delivering rich, personalized, and current information. This approach not only fulfills all the listed requirements but also reflects my growth in knowledge management, innovative LLM design, and the ability to create an AI agent that feels meaningfully personalized.
<div align=center><img width="1000" alt="Learning Rhino" src="assets/Week11 Final Agent1.png"></div>
This picture shows the result of interacting with the 'MINI ME' agent. When asked about my experience with embedded systems and related information, it successfully provides details from both my private knowledge base and public sources (via Google search), including the correct URL to the Photon 2 documentation.
<br><br>

### 2. Speculations

#### 2.1 Speculation on Human-Like AI Interactions

As AI systems like "MINI ME" develop, they could transform how users perceive and relate to technology, building connections that feel more human. With features like memory and adaptable responses, AI can simulate empathy, creating experiences where users feel understood and supported. This shift could lead people to rely on AI not just for information but also for advice that feels genuinely personal. For example, we can imagine an AI assistant that remembers a user’s past preferences and offers encouragement when facing a challenge. This capability could turn AI into a companion-like presence, bridging the gap between information provider and empathetic supporter.<br><br>
For the future Work to enhance "MINI ME," I could integrate sentiment analysis to detect user emotions, allowing it to respond more sensitively in different situations, making interactions feel even more personalized and supportive.<br><br>

#### 2.2 Speculation on AI in Engineering

Integrating AI into engineering workflows could allow AI to handle initial design tasks, freeing engineers to focus on refining and approving designs. For example, an AI could generate multiple layout options based on specified criteria, while engineers review and make adjustments as needed. This speeds up the design process and enables more rapid prototyping. For example, an AI-driven design tool could quickly produce several product models based on project goals, with engineers choosing the best fit and refining it, allowing for more exploration in less time.<br><br>
In the future, for this project, I can expand it to support design brainstorming and refinement could turn it into a valuable tool in engineering, assisting with rapid prototyping and collaborative creation.<br><br>

#### 2.3 Speculation on AI Self-Improvement

In the future, AIs like "MINI ME" could autonomously monitor and enhance other AI systems, optimizing performance and adapting algorithms without human input. This self-sustaining ecosystem would allow AIs to learn from each other, evolving continuously through feedback loops. An AI could analyze a chatbot’s responses, adjusting its natural language processing to improve user interactions. This setup could create a dynamic cycle where one AI's improvements inform another’s development.<br><br>
For future work, I can build monitoring capabilities into "MINI ME" to allow it to refine its own responses based on user feedback, making it a self-improving assistant capable of adapting to evolving needs.<br>
