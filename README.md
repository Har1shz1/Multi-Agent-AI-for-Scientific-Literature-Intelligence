# 🧠 Autonomous Agentic AI System for Scientific Literature Intelligence & Research Gap Discovery

> A research-grade multi-agent AI system that simulates how researchers explore literature, analyze methodologies, synthesize trends, and identify open research problems.

---

## 🚀 Introduction

Conducting a high-quality literature review is a time-consuming and cognitively demanding process involving:
- Discovering relevant papers
- Comparing methodologies
- Identifying emerging trends
- Finding under-explored research gaps

This project introduces an **autonomous agent-based AI system** that models the **academic research workflow** using multiple collaborating AI agents.  
Instead of a single chatbot, the system decomposes research into **specialized reasoning stages**, closely mirroring how real research groups operate.

---

## ✨ Key Features

- 🤖 Multi-agent architecture using CrewAI  
- 📚 Automated literature discovery via Serper (Google Search API) and arXiv  
- 🧩 Role-specific reasoning agents  
- 🔗 Task chaining and prompt-driven orchestration  
- 🔍 Research gap identification and experiment suggestions  
- ⚡ Fast LLM inference using Groq-hosted LLaMA 3.1 models  

---

## 🧠 System Architecture

### Overall Architecture

```mermaid
flowchart TD
    U[User Research Topic] --> LM[Literature Miner Agent]
    LM --> MA[Methodology Analyzer Agent]
    MA --> TS[Trend Synthesizer Agent]
    TS --> RG[Research Gap Agent]

    LM -->|Search Queries| S[Serper API]
    LM -->|Scholarly Metadata| A[arXiv]

    S --> LM
    A --> LM

    RG --> O[Final Research Intelligence Output]

### Overall Architecture
graph LR
    subgraph Agentic_AI_System
        LM[Literature Miner]
        MA[Methodology Analyzer]
        TS[Trend Synthesizer]
        RG[Research Gap Agent]
    end

    LM --> MA --> TS --> RG
