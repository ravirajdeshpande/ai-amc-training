# AI / AMC Engineering Training

A structured learning repository for my **AI / AMC Engineering Training Program**, covering the evolution of Large Language Models (LLMs), Prompt Engineering, RAG, MCP, Agentic AI, LangGraph, security, observability, LLMOps, and production deployment.

This repository contains my **course exercises, hands-on implementations, experiments, documentation, notes, and capstone project** developed throughout the training.

---

## 🎯 Training Objective

The objective of this training is to build practical, hands-on expertise in designing and developing **enterprise-grade Generative AI and Agentic AI applications**.

The learning journey progresses from:

**LLMs → Prompt Engineering → LangChain → Enterprise RAG → MCP → Agents → Multi-Agent Systems → Security → LLMOps → Production**

---

## 📚 Training Curriculum

| #  | Topic                                  | Status        |
| -- | -------------------------------------- | ------------- |
| 01 | Introduction & Evolution of LLM Models | ⬜ Completed |
| 02 | Prompt Engineering                     | ⬜ Completed |
| 03 | LangChain                              | ⬜ Not Started |
| 04 | Enterprise RAG – Ingestion             | ⬜ Not Started |
| 05 | Enterprise RAG – Hybrid Search         | ⬜ Not Started |
| 06 | RAG Evaluation & A/B Testing           | ⬜ Not Started |
| 07 | MCP Servers                            | ⬜ Not Started |
| 08 | MCP in Production & A2A                | ⬜ Not Started |
| 09 | LangGraph – Stateful Agents            | ⬜ Not Started |
| 10 | LangGraph – Multi-Agent Systems        | ⬜ Not Started |
| 11 | Memory & State                         | ⬜ Not Started |
| 12 | Guardrails & Security                  | ⬜ Not Started |
| 13 | Observability & LLMOps                 | ⬜ Not Started |
| 14 | Deployment & Production                | ⬜ Not Started |
| 15 | Capstone & Career Launch               | ⬜ Not Started |

### Progress Legend

* ⬜ Not Started
* 🟡 In Progress
* 🟢 Completed
* 🔵 Revisiting / Improving

---

## 🧠 Learning Path

```text
                    LLMs
                     │
                     ▼
            Prompt Engineering
                     │
                     ▼
                 LangChain
                     │
                     ▼
              Enterprise RAG
             ┌───────┴────────┐
             ▼                ▼
        Ingestion        Hybrid Search
             │                │
             └───────┬────────┘
                     ▼
             RAG Evaluation
              & A/B Testing
                     │
                     ▼
                MCP Servers
                     │
                     ▼
             MCP + A2A
                     │
                     ▼
              LangGraph
                     │
          ┌──────────┴──────────┐
          ▼                     ▼
    Stateful Agents       Multi-Agent Systems
          │                     │
          └──────────┬──────────┘
                     ▼
               Memory & State
                     │
                     ▼
             Guardrails & Security
                     │
                     ▼
            Observability & LLMOps
                     │
                     ▼
             Deployment & Production
                     │
                     ▼
                 CAPSTONE
                     │
                     ▼
              CAREER LAUNCH
```

---

# 📂 Repository Structure

```text
ai-amc-training/
│
├── README.md
│
├── week-01/
│   ├── exercise-01/
│   ├── exercise-02/
│   └── ...
│
├── week-02/
│   ├── exercise-01/
│   ├── exercise-02/
│   └── ...
│
├── week-03/
│   ├── exercise-01/
│   ├── exercise-02/
│   └── ...
│
├── week-04/
│   ├── exercise-01/
│   ├── exercise-02/
│   └── ...
│
├── projects/
│   ├── mini-projects/
│   └── capstone/
│
├── notes/
│   ├── llm-evolution.md
│   ├── prompt-engineering.md
│   ├── langchain.md
│   ├── rag.md
│   ├── mcp.md
│   ├── langgraph.md
│   ├── agentic-ai.md
│   ├── security.md
│   └── llmops.md
│
├── resources/
│   ├── references.md
│   └── useful-links.md
│
└── templates/
    ├── exercise-template.md
    └── project-template.md
```

---

# 🛠️ Technologies & Concepts

The training will cover a combination of AI frameworks, engineering practices and architectural patterns.

### Generative AI & LLMs

* Large Language Models
* Transformer Architecture
* Tokens & Embeddings
* Attention
* Model Parameters
* LLM APIs
* Foundation Models
* Open / Closed Models

### Prompt Engineering

* Zero-Shot Prompting
* Few-Shot Prompting
* Chain-of-Thought
* ReAct
* Structured Outputs
* Prompt Templates
* Context Engineering
* Prompt Evaluation

### AI Application Development

* Python
* LangChain
* LangGraph
* LLM APIs
* Tool Calling
* Structured Data
* API Integration

### Enterprise RAG

* Document Ingestion
* Document Chunking
* Embeddings
* Vector Databases
* Semantic Search
* Keyword Search
* Hybrid Search
* Retrieval
* Reranking
* RAG Evaluation
* A/B Testing

### Agentic AI

* AI Agents
* Stateful Agents
* ReAct Agents
* Tool-Using Agents
* Planning
* Memory
* State Management
* Multi-Agent Systems
* Agent-to-Agent (A2A) Communication

### MCP

* Model Context Protocol
* MCP Servers
* MCP Clients
* MCP Tools
* MCP Resources
* Production MCP
* MCP Security
* A2A

### Production AI

* Guardrails
* AI Security
* Prompt Injection
* Access Control
* Observability
* LLMOps
* Logging
* Tracing
* Evaluation
* Monitoring
* Deployment
* Production Architecture

---

# 🧪 Exercises

Each training exercise will be maintained as an independent, reproducible piece of work.

Each exercise should ideally contain:

```text
exercise/
│
├── README.md
├── src/
├── tests/
├── prompts/
├── docs/
└── requirements.txt
```

The exercise README should document:

* Objective
* Problem statement
* Approach
* Architecture
* Technologies used
* Implementation
* Results
* Challenges
* Lessons learned
* Possible improvements

---

# 📝 Learning Notes

The `notes/` directory contains my consolidated understanding of important concepts covered during the training.

The objective is not only to complete the exercises but also to build a **personal AI Engineering knowledge base** that can be referenced after the training.

---

# 🚀 Projects

## Mini Projects

Small applications developed during the training to apply individual concepts such as:

* LLM applications
* Prompt Engineering
* RAG
* Hybrid Search
* MCP
* AI Agents
* LangGraph
* Multi-Agent Systems

## Capstone Project

The final project will combine multiple concepts learned during the training into an **enterprise-oriented AI / Agentic AI application**.

### Target Architecture

```text
                 User / Application
                         │
                         ▼
                  AI Application
                         │
             ┌───────────┴───────────┐
             ▼                       ▼
            RAG                    Agents
             │                       │
             ▼                       ▼
      Knowledge Base            LangGraph
             │                       │
             └───────────┬───────────┘
                         ▼
                    MCP / Tools
                         │
                         ▼
                 External Systems
                         │
                         ▼
               Guardrails / Security
                         │
                         ▼
                 Observability
                         │
                         ▼
                  Production
```

---

# 🔬 Engineering Practices

Throughout the training, I will aim to follow professional software engineering practices:

* Git-based version control
* Feature branches
* Pull Requests
* Meaningful commits
* Unit testing
* Integration testing
* Documentation
* Environment management
* Secure secrets management
* Code quality
* Evaluation-driven development
* Observability
* Reproducibility

---

# 📈 Training Progress

My goal is to progress from understanding individual AI concepts to being able to design and implement **production-ready AI and Agentic AI systems**.

```text
LLM Fundamentals
       ↓
AI Application Development
       ↓
RAG Engineering
       ↓
Agent Engineering
       ↓
Multi-Agent Systems
       ↓
AI Security
       ↓
LLMOps
       ↓
Production AI
       ↓
AI / Agentic AI Architecture
```

---

# 🎓 Learning Outcomes

By the end of this training, I aim to be able to:

* Explain the evolution and architecture of modern LLMs
* Engineer effective prompts and structured AI interactions
* Build LLM applications using LangChain
* Build enterprise RAG pipelines
* Implement hybrid search
* Evaluate and benchmark RAG systems
* Build and consume MCP servers
* Understand MCP production architecture and A2A communication
* Build stateful agents using LangGraph
* Design multi-agent systems
* Implement memory and state management
* Apply AI guardrails and security controls
* Implement observability and LLMOps
* Deploy AI applications into production
* Design enterprise-grade Agentic AI architectures

---

# 💡 Key Principle

> **The goal is not simply to learn AI tools. The goal is to learn how to engineer reliable, secure, observable and production-ready AI systems.**

---

## 👨‍💻 Training Repository

**Program:** AI / AMC Engineering Training
**Duration:** 4 Weeks
**Focus:** Generative AI • RAG • MCP • Agentic AI • LLMOps • Production AI

---

*This repository is a continuous learning and experimentation space. Content will evolve throughout the training as new concepts, exercises and projects are completed.*

