# Data Processing Based on AutoGen

## Agents

1. **Data Agent**
   
   - Reads data (CSV / JSON)
   
   - Performs basic statistics (max, min, average)

2. **Analysis Agent**
   
   - Plots charts
   
   - Analyzes trends

3. **Report Agent**
   
   - Summarizes results in natural language

---

## Prompt

I want to deploy AutoGen locally and orchestrate multiple agents for a data processing task.

My environment:

- OS: Windows

- IDE: VS Code



1. **Data Agent**
   
   - Read data (CSV / JSON)
   
   - Perform basic statistics

2. **Analysis Agent**
   
   - Analyze trends
   
   - Generate visualizations

3. **Report Agent**
   
   - Summarize results in natural language

Reference tutorial: https://github.com/microsoft/autogen  
Use : `autogen-agentchat`

Please provide a detailed tutorial

---

## Project Structure

```
D:\projects\autogen\
├─ .venv\
├─ .env
├─ main.py
├─ requirements.txt
└─ sales.csv
```

---

## Setup Steps

### 1. Create Virtual Environment

```bash
python -m venv .venv
.venv\Scripts\activate
```

### 2. Configure Environment Variables

- Add your API key to the `.env` file

- Write your main code in `main.py`

### 3. Run the Project

```bash
python main.py
```

---

## Improvements

1. **GraphFlow** — Custom workflow orchestration

2. **AutoStudio** — Web-based interface
