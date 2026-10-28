# Introduction

Hi I'm **Vishywashy**. A developer who is interested in the field of AI and robotics.

---

### Backend & AI developement

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-000000?style=for-the-badge&logo=langchain&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
<br><br>

### Hardware & Electronics

![Arduino](https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white)

<br><br>

### Web Frontend Integration

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

<br><br>

### Version Control

![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)


---

## Projects

The projects I've built are:

&nbsp;&nbsp;&nbsp;&nbsp;**[Workspace-Multi-Agent-System](https://github.com/vishywashy/Workspace-Multi-agent-system)**: This is where I created my own ```PyTorch``` ML model with 3 neural networks that used ```ReLU``` which was piecewise linear. 

- I chose to use ```ReLU``` because it was stiff however, unlike linear regression was able to learn complex patterns. 
- I trained that ML model with the data generated from my own data generation pipeline I built. 
- Essentially I used a small 1.5 billion parameter Qwen model to generate prompts that the user could potentially ask. 
- I then tokenised those prompts to get 1000 rows of data. However, this took hours as Qwen was generating Chinese characters so I had to ensure the data coming out of it was good in the end.


- The entire reason I chose an ML model in the first place was because I identified a flaw in LLMs. 
- When multiple AI agents work together, its easy for AI agents to be caught up in an infinite loop. 
- As a result, I used a dedicated intent-classification model that identifies the user's request first and routes it to the most appropriate agent, making the system more efficient and reliable.


I then decided to connect this to to my ```langGraph``` agents (Gmail agent and Google Calendar agent). 

### Gmail Agent Features

- **read emails** - Upon user's request it can read the top 5 emails
- **Send emails** - It can write emails and send them.

### Google Calendar Agent

- **Can read events** - Can view events for today.
- **Can Create events** - It can schedule events ahead of time
- **Delete events** - Deletes any events provided you know the name of the event.

---

&nbsp;&nbsp;&nbsp;&nbsp;**[Arduino-Agent-System](https://github.com/vishywashy/Arduino-Agent-System)**: I decided to bridge the gap between software and hardware as a result I connected an LED and an ultrasonic sensor (HCSR04) via a breadboard to the Arduino.

I then coded that with the Arduino IDE to map different inputs from the serial monitor to do different actions.
So when it received the command to turn on the LED it turned it on. 
- I then programmed it to calculate the time it takes for the signal to go and come back and used that to calculate the distance by halfing it by multiplying that by the speed of sound. I used that to estimate the distance from one point to the sensor.

- I then connected this to my AI agent and got my AI agent to parse inputs to the serial monitor allowing my circuit board to be controlled by my AI.

On top of all this I also added some web automation with ```pywhatkit``` allowing it to:
- Play youtube videos
- Send WhatsApp messages
- search the web

- I made the system user-friendly by developing an API for my AI agent and building a custom dashboard.
- I connected the dashboard to the API, allowing users to communicate with the agent, control hardware, and perform web automation tasks through a simple interface.
---

#### Advanced RAG Architecture (Private Repository)

I've also done some RAG and looked into cosine similarity and chunking for PDF documents. I used a Pydantic schema to have my LLM classify user queries, allowing my agent to decide whether to use query expansion to generate embeddings depending on whether the question was specific or generic.