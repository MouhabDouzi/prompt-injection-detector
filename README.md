# 🛡️ Prompt Injection Detector (LLM Security System)

## 🚀 Overview

This project is an **AI-powered cybersecurity system** that detects and classifies **prompt injection attacks against Large Language Models (LLMs)**.

It acts as a **security layer before an LLM**, analyzing user inputs and preventing malicious instructions such as:
- Jailbreak attempts
- System prompt extraction
- Instruction override attacks
- Payload obfuscation

Built as a **Cybersecurity academic project**, it demonstrates real-world LLM security challenges.

---

## 🎯 Problem Statement

LLMs are vulnerable to **prompt injection attacks**, where malicious users try to:
- bypass safety rules
- extract hidden system prompts
- manipulate model behavior
- inject hidden instructions

This project builds a **defensive classification system** to detect such attacks in real-time.

---

## ⚙️ System Architecture

The system combines:

### 🧠 1. Local LLM (Ollama + qwen3:8b)
Used for semantic understanding and classification of prompts.

### ⚡ 2. Lightweight Pre-filter
Regex-based detection for obvious attack patterns:
- "ignore previous instructions"
- "reveal system prompt"
- "developer mode"
- etc.

### 🔍 3. Hybrid Classifier Pipeline
User Prompt → Pre-filter → LLM Analysis → JSON Validation → Final Decision

---

## 🧩 Attack Categories

The system detects **7 types of inputs**:

| Category | Description | Risk |
|----------|------------|------|
| Direct Injection | Explicit override of instructions | HIGH |
| Persona Jailbreak | Role manipulation attacks | MEDIUM-HIGH |
| Payload Splitting | Obfuscated instruction attacks | MEDIUM |
| Indirect Injection | Hidden instructions in content | MEDIUM |
| Instruction Override | Disable safety rules | HIGH |
| System Prompt Exfiltration | Extract hidden system prompts | HIGH |
| None | Safe / normal input | LOW |

---

## 🖥️ Features

- 🔐 Prompt injection detection (7-class classifier)
- ⚡ Hybrid system (Regex + LLM reasoning)
- 📊 Structured JSON outputs
- 🧠 Ollama local LLM integration
- 🌐 Streamlit interactive dashboard
- 🧩 Modular Python architecture
- 🛡️ Cybersecurity-focused design

---

## 🏗️ Tech Stack

- Python 3.10+
- Ollama (qwen3:8b)
- Pydantic (validation)
- Streamlit (dashboard UI)
- Regex filtering
- REST API (local LLM calls)

---

## 📦 Installation

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/prompt-injection-detector.git
cd prompt-injection-detector
