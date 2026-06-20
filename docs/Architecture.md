# MentorMind AI – Full-Stack Architecture Document

## System Overview

MentorMind AI is a memory-driven educational companion that delivers personalized tutoring by combining multi-agent orchestration, contextual retrieval, adaptive learning, and AI safety mechanisms.

---

# Agent Workflows

### Student Cognitive Profiler

Maintains student preferences, learning style, and proficiency level.

### Adaptive Pedagogy Engine

Generates explanations tailored to the student's understanding and learning behavior.

### Knowledge Gap Inference Engine

Identifies misconceptions and tracks weak concepts.

### Quiz Synthesis Engine

Creates personalized quizzes and flashcards.

### Spaced-Repetition Scheduler

Resurfaces weak concepts using forgetting-curve principles.

### Safety Alignment Agent

Ensures safe and trustworthy responses through Enkrypt AI.

---

# Mastra Orchestration

Student Query

↓

Mastra Orchestrator

↓

Multi-Agent Swarm

↓

Qdrant Memory Retrieval

↓

LLM Processing

↓

Enkrypt AI Validation

↓

Personalized Response

---

# Qdrant Memory and Retrieval

Collections:

* student_profiles
* conversation_memory
* knowledge_gaps
* learning_materials
* quiz_history

Capabilities:

* Semantic search
* Long-term memory
* Context retrieval
* Personalized learning history

---

# Enkrypt AI Evaluation Layer

### Input Protection

* Prompt injection detection
* Toxicity filtering

### Output Protection

* Hallucination detection
* Educational safety checks
* Age-appropriate responses
* Safe content moderation

---

# Frontend

Technology Stack:

* Next.js
* Tailwind CSS

Modules:

* Chat Interface
* Learning Dashboard
* Quiz Module
* Progress Tracking

---

# Backend

Technology Stack:

* Python
* FastAPI

Responsibilities:

* Agent orchestration
* API management
* Memory handling
* Communication with Qdrant and external AI services

---

# APIs and Integrations

### AI Models

* OpenAI GPT-4o
* Google Gemini 2.5 Flash

### Frameworks and Services

* Mastra
* Qdrant
* Enkrypt AI

---

# Databases

### Qdrant Vector Database

Stores:

* Embeddings
* Memory collections
* Learning resources
* Conversation history

### PostgreSQL

Stores:

* User metadata
* Analytics
* Session information

---

# Deployment Architecture

Frontend

(Vercel)

↓

Backend

(Render + Docker)

↓

Mastra Agent Layer

↓

Qdrant Vector Database

↓

External AI Services

(OpenAI / Gemini + Enkrypt AI)

---

# Expected Outcome

MentorMind AI provides a personalized and safe learning experience by combining adaptive tutoring, memory-driven retrieval, proactive revision, and multi-agent orchestration, enabling students to learn more effectively over time.
