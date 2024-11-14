# Week 10: Report 10 #
## Week of 10/31-11/7
### 1. Reflections

This week, I focused on conducting a series of initial experiments with the 'MINI ME' agent to build a foundation for its personalization capabilities. Starting from a basic GPT model setup, I gradually enhanced it by adding instructional prompts, a personalized knowledge base, and dynamic variables. Each experiment allowed me to understand how different configurations impact the agent’s response quality, personalization, and adaptability. These foundational steps set the stage for creating a digital twin that reflects my unique professional and academic background.

<img width="1000" alt="Learning Rhino" src="assets/Week10 Function Diagram.png">

#### Understanding Basic LLM Capabilities
The first experiment involved testing a simple GPT model without any special configurations such as instructional prompts, retrieval augmentation, or variable adjustments. This provided a baseline understanding of the model’s inherent capabilities. Without additional guidance, the model produced generic responses, highlighting the need for further customization to align the agent's behavior with my personal and professional context.

<img width="1000" alt="Learning Rhino" src="assets/Week10 Agent1.png">

#### Impact of Instructional Prompts on Personalization
In Experiment 2, I introduced instructional prompts to shape the model’s responses by giving it context about representing me, Jingru Zhang, as a creative technologist, HCI researcher, and artist. This experiment demonstrated how instructional prompts could make the responses more aligned with my identity and expertise, reflecting my background in human-computer interaction. The model now provided answers that felt more personalized, showing how setting a defined role can influence the quality of LLM responses.

<img width="1000" alt="Learning Rhino" src="assets/Week10 Agent2.png">

#### Leveraging a Personalized Knowledge Base with Retrieval Augmented Generation (RAG)

Experiment 3 integrated a custom knowledge base using RAG, where the model accessed specific personal documents like my CV and project reports. This enhancement allowed the agent to retrieve details directly relevant to my work, making its responses both accurate and uniquely tailored to my personal experiences. For instance, when asked about my background, the model could pull precise information on my studies at Tsinghua University and UC Berkeley, significantly improving its response quality and relevance.

<img width="1000" alt="Learning Rhino" src="assets/Week10 Agent3-1.png">
<img width="1000" alt="Learning Rhino" src="assets/Week10 Agent3-2.png">

#### Incorporating Context-Specific Variables

In the fourth experiment, I added dynamic variables, such as location and year, enabling the model to adjust responses based on these factors. This configuration made the agent more adaptable and time-specific, accurately answering questions like my current academic status in 2024 or my involvement in Berkeley. This flexibility allows the agent to be even more precise, which could be valuable in scenarios requiring responses that consider both place and time.
<img width="1000" alt="Learning Rhino" src="assets/Week10 Agent4.png">




### 2. Speculations

One future direction is to improve the model’s adaptability further by refining the use of variables and knowledge retrieval. For example, enabling the agent to recognize changes in my research focus or new professional achievements over time could make it a continuously evolving digital twin. This would be especially useful in professional settings where maintaining up-to-date personal data is crucial for networking and collaboration.

Suppose in the future I transition into a new research area such as neuroinformatics. With an adaptive knowledge base, the model could update its responses based on this new focus area, allowing it to accurately reflect changes in my career trajectory.



Experiment 1: Basic GPT response without instructions, showing generic answers.
Experiment 2: Response using instructional prompts to represent me as Jingru Zhang.
Experiment 3: Example response that utilizes the personalized knowledge base.
Experiment 4: Context-specific answer using dynamic variables (e.g., confirming my current studies at Berkeley in 2024).
Sketches, Drawings, and Diagrams:
Use the System Architecture Diagram to explain how different components interact to process questions. Additionally, add the System Process Diagram to illustrate the decision-making flow within the MINI ME agent. These diagrams provide a visual representation of the system’s evolution from a basic LLM to a context-sensitive agent.
