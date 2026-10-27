# Introduction

Hi I'm **Vishywashy**. A developer who is interested in the field of AI and robotics.

---

## Projects

The projects I've built are:
- **Workspace-Multi-Agent-System**: This is where I created my own ```pytorch``` ML model with 3 neural networks that used ```ReLU``` which was piecewise linear. I chose to use ```ReLU``` because it was stiff however, unlike linear regression was able to learn complex patterns. I trained that ML model with the data generated from my own data generation pipeline I built. Esssentially I used a small 1.5 billion parameter Qwen model to generate prompts that the user could potentially ask. I then tokenised those prompts to get 1000 rows of data. However, this took hours as Qwen was generating Chinese characters so I had to ensure the data coming out of it was good in the end.


The entire reason I chose an ML model in the first place was because I identified a flaw in LLMs. When a system of AI agents becomes complicated. LLM's tend to hallucinate as a result infinitely loop over tools. An ML model identifies intent and routes to it without causing any loops making them incredibly efficient.


I then decided to connect this to to my ```langgraph``` agents (Gmail agent and Google Calendar agent). 

### Gmail Agent Features

- **read emails** - Upon user's request it can read the top 5 emails
- **Send emails** - It can write emails and send them.

### Google Calendar Agent

- **Can read events** - Can view events for today.
- **Can Create events** - It can schedule events ahead of time
- **Delete events** - Deletes any events provided you know the name of the event.


- **Arduino-Agent-System**: I decided to bridge the gap between software and hardware as a result I connected an LED and an ultrasonic sensor (HCSR04) via a breadboard to the arduino.

I then coded that with the arduino IDE to map different inputs from the serial monitor to do different actions.
So when it received to turn on the LED it turned it on. I then programmed it to calculate the time it takes for the signal to go and come back and used that to calculate the distance halfing it by multiplying that by the speed of sound. I used that to estimate the distance from one point to the sensor.

I then connected this to my AI agent and got my AI agent to parse inputs to the serial monitor allowing my circuit board to be controlled by my AI.

On top of all this I also added some web automation with ```pywhatkit``` allowing it to:
- Play youtube videos
- Send whatsapp messages
- search the web

---

#### Advanced RAG Architecture (Private Repository)

I've also done some RAG and looked into cosine similarity and chunking for PDF documents. I used a Pydantic schema to have my LLM classify user queries, allowing my agent to decide whether to use query expansion to generate embeddings depending on whether the question was specific or generic.