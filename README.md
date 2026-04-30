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
