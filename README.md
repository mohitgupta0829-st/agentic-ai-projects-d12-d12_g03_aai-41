# Autonomous Retail Researcher Agent

## Overview

The Autonomous Retail Researcher Agent is an AI-based system designed to automate retail research using a multi-agent architecture. The system combines Agentic AI concepts with Retrieval-Augmented Generation (RAG) to perform intelligent data collection, analysis, and summarization.

It enables users to input queries in natural language and receive structured insights generated from real-time data sources and stored knowledge.

---

## Problem Statement

Retail research involves analyzing large volumes of data such as market trends, product demand, and competitor activity. Traditional approaches are manual, time-consuming, and inefficient.

Existing systems often rely on keyword-based search, which fails to capture the intent behind queries and leads to incomplete or irrelevant results.

This project aims to solve these challenges by building an intelligent system capable of understanding queries, retrieving relevant information, and generating meaningful insights automatically.

---

## Objectives

- Develop an autonomous retail research system
- Implement multi-agent collaboration
- Automate data collection, analysis, and summarization
- Enable natural language interaction
- Store and reuse research outputs
- Improve efficiency and decision-making

---

## Key Features

- Multi-agent architecture for task distribution
- Automated research workflow
- Real-time data processing
- Natural language query interface
- LLM-based summarization
- Retrieval-Augmented Generation (RAG)
- Persistent storage using vector database
- Modular and scalable backend design

---

## System Architecture

The system follows a pipeline-based multi-agent structure:

User Query → Orchestrator → Research Agent → Analysis Agent → Summary Agent → Storage → Output

Each component performs a specific task, ensuring separation of concerns and scalability.

---

## Backend Components

The backend is implemented using Python and consists of the following key modules:

- `main.py`  
  Entry point of the application. Initializes the system and API.

- `agents.py`  
  Defines the multi-agent workflow and coordination logic.

- `rag.py`  
  Implements the Retrieval-Augmented Generation pipeline.

- `memory.py`  
  Handles storage and retrieval of past interactions.

- `database.py`  
  Manages local data storage.

- `tools.py`  
  Contains helper utilities for data processing and external integrations.

- `config.py`  
  Stores configuration and environment settings.

---

## Data & Storage

- Vector storage using FAISS (`faiss_index.faiss`, `faiss_index.meta.pkl`)
- Local database (`retail_researcher.db`)
- Document storage in `backend/data/`

---

## Frontend

The frontend is a lightweight interface built using:

- HTML (`index.html`)
- CSS (`style.css`)
- JavaScript (`script.js`)

It communicates with the backend API to:
- Accept user queries
- Trigger research workflows
- Display structured results

---

## DevOps & Deployment

- Backend Dockerized using `backend/Dockerfile`
- Frontend served via Nginx (`frontend/nginx.conf`)
- Multi-container setup defined in `docker-compose.yml`

---

## Project Structure

```
Agent/
│
├── backend/
│   ├── data/
│   ├── agents.py
│   ├── config.py
│   ├── database.py
│   ├── main.py
│   ├── memory.py
│   ├── rag.py
│   ├── tools.py
│   ├── requirements.txt
│   ├── requirements.docker.txt
│   ├── Dockerfile
│   ├── faiss_index.faiss
│   ├── faiss_index.meta.pkl
│   └── retail_researcher.db
│
├── frontend/
│   ├── index.html
│   ├── script.js
│   ├── style.css
│   ├── nginx.conf
│   └── Dockerfile
│
├── docker-compose.yml
├── README.md
└── .gitignore
```

---

## Installation and Setup

### Clone the repository


git clone <repository-url>
cd Agent


### Create virtual environment


python -m venv venv
venv\Scripts\activate (Windows)
source venv/bin/activate (Linux/Mac)


### Install dependencies


pip install -r backend/requirements.txt


### Run backend


cd backend
python main.py


### Run frontend

Open `frontend/index.html` in browser  
or use Docker setup.

---

## Running with Docker


docker-compose up --build


---

## Output

The system generates structured research outputs including:

- Market trends
- Product insights
- Competitor analysis
- Summary reports

Results are displayed in a clean and readable format on the frontend interface.

---

## Key Outcomes

- Automated retail research pipeline
- Efficient multi-agent coordination
- Integration of RAG with LLMs
- Faster and more accurate insights
- Reduced manual effort

---

## Limitations

- Requires internet connectivity
- Dependent on external data sources
- Limited support for multimedia inputs
- Not optimized for large-scale enterprise deployment

---

## Future Enhancements

- Cloud deployment (AWS, Docker)
- Database upgrades (MongoDB, PostgreSQL)
- Real-time dashboards and analytics
- Voice-based interaction
- Multi-domain expansion
- Improved agent orchestration

---

## Contributors

Aditya Agrawal  
Atharv Shukla  
Mohit Gupta  
Malya Singh  
Nikhil Kumar Verma  

Institution: Medicaps University  
Course: Agentic AI – Datagami Skill Based Course  
Project: AAI-41  
Group: D03G12  

---

## Conclusion

The project demonstrates how Agentic AI and multi-agent systems can be applied to automate complex retail research workflows. By integrating real-time data retrieval, intelligent processing, and structured output generation, the system improves efficiency and decision-making.

The modular design ensures scalability and makes the system adaptable for future enhancements and broader applications
