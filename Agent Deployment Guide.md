# Agent Deployment Guide

## 1. Create Project & Install Dependencies

`mkdir deepseek_agent
cd deepseek_agent`

### Create a Virtual Environment

`python -m venv venv venv\Scripts\activate`

After activation, you should see:

`(venv)`

### Install Dependencies

`pip install requests python-dotenv`

---

## 2. Coding

### Project Structure

`deepseek_agent/ │ ├─ venv/ ├─ .env ├─ agent.py └─ tools.py`

### (1) Create `.env` File

`DEEPSEEK_API_KEY=your_deepseek_api_key`

### (2) Add Code Files

- Put the AI coding tool  into `tools.py`

- Put the agent main logic into `agent.py`

---

## 3. Run the Agent

`python agent.py`
