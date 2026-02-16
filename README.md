# 🛡️ iSafe: Cognitive Security \& Anti-Fraud AI

[![Status](https://img.shields.io/badge/Status-Production%20Ready-success.svg)]()
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)]()
[![License](https://img.shields.io/badge/License-MIT-green.svg)]()
[![AI Engine](https://img.shields.io/badge/Generative%20AI-LLM-purple)]()
[![Framework](https://img.shields.io/badge/Frontend-Streamlit-red)]()

> **"Decentralizing Cyber-Defense with Large Language Models."**

> *Architected by [Ankit Choubey (Master AK)](https://github.com/ankit-choubey)*

---

## 📖 Executive Summary

**iSafe** is an enterprise-grade cybersecurity utility designed to neutralize social engineering attacks (Smishing, Phishing, and Cognitive Fraud) using **Generative AI**. Unlike deterministic, regex-based legacy filters, iSafe deploys a **Large Language Model (LLM)** to perform semantic analysis on unstructured text, identifying malicious *intent* rather than just keywords.

The system utilizes **Zero-Shot Chain-of-Thought (CoT) reasoning** to deconstruct psychological manipulation vectors—such as artificial urgency, authority impersonation, and scarcity bias—providing users with real-time, explainable threat intelligence.

---

## 🧠 Cognitive Architecture

iSafe operates on a **Neural-Symbolic Logic** pipeline, bridging raw text processing with advanced reasoning capabilities.

### The Inference Pipeline:

1. **Ingestion \& Normalization**: Raw inputs (SMS, Email, DMs) are sanitized and prepared for tokenization.
2. **Prompt Engineering Layer**: The input is encapsulated in a **System Persona** (`Cyber Safety Analyst`) with strict constraints. We utilize **Contextual Few-Shot Learning** principles to enforce a deterministic JSON output schema.
3. **LLM Inference Engine**: The payload is processed by the configured LLM (e.g., Google Gemini Pro / Flash) to extract latent semantic features.
4. **Psychometric Evaluation**: The model scores the text on:
    * **Urgency Heuristics**: Detecting artificially induced time pressure.
    * **Authority Bias**: Identifying impersonation of entities (RBI, IRS, Banks).
    * **Sentiment Volatility**: Measuring aggression or fear-mongering tactics.
5. **Structured Serialization**: The probabilistic output is converted into a strict JSON object for frontend rendering.

---

## 🚀 Key Technical Features

* **⚡ Latency-Optimized Inference**: Real-time threat scoring (<800ms) using lightweight, distilled LLM architectures.
* **📊 Probabilistic Risk Assessment**: Dynamic classification into **Low**, **Medium**, or **High** confidence intervals based on log-probability thresholds.
* **🛡️ Explainable AI (XAI)**: Unlike "black box" classifiers, iSafe provides natural language explanations for *why* a message is flagged, improving user digital literacy.
* **🔌 Vendor-Agnostic Design**: The architecture is decoupled from specific model providers, allowing hot-swapping between Gemini, GPT-4, or local LLaMA models via the `LLM_API_KEY` configuration.
* **🔒 Privacy-First Design**: Stateless execution ensures no user PII (Personally Identifiable Information) is persisted in vector stores or logs.

---

## 🛠️ Tech Stack \& Dependencies

| Layer | Technology | Role |
| :-- | :-- | :-- |
| **Orchestration** | Python 3.x | Async I/O \& API Management |
| **Interface** | Streamlit | Reactive Web UI \& State Management |
| **AI Backend** | Google Generative AI (Gemini) | Semantic Reasoning \& NLP |
| **Security** | `python-dotenv` | Environment Variable Injection |
| **Data Format** | JSON / Markdown | Structured Data Interchange |


---

## ⚙️ Deployment \& Configuration

Follow these steps to deploy the iSafe neural defense layer locally.

### 1. Clone the Repository

```bash
git clone [https://github.com/ankit-choubey/isafe.git](https://github.com/ankit-choubey/isafe.git)
cd isafe
```

### 2. Environment Setup

Isolate dependencies to prevent version conflicts.

**macOS/Linux:**

```bash
python3 -m venv venv
source venv/bin/activate
```

**Windows:**

```bash
python -m venv venv
venv\Scripts\activate
```


### 3. Install Core Dependencies

```bash
pip install -r requirements.txt
```


### 4. API Configuration

Create a `.env` file in the root directory. This project uses a generic variable to support model flexibility.

```ini
# Configuration for the underlying GenAI Model (default: Gemini)
LLM_API_KEY=your_secured_api_key_here
```


### 5. Initialize the Neural Engine

```bash
streamlit run app.py
```


### 📂 Repository Structure

```
isafe/
├── assets/
│   └── architecture_diagram.png # System design visuals
├── .env                         # Secrets (GitIgnored)
├── app.py                       # Main Inference Controller
├── requirements.txt             # Dependency graph
├── PROJECT_DETAILS.md           # Extended technical documentation
├── README.md                    # Documentation (Current)
└── LICENSE                      # MIT Open Source License
```


---

## 🧪 Usage \& Testing

**Dashboard Access**: Navigate to the local Streamlit port (Default: http://localhost:8501).

**Threat Simulation**: Input a sample phishing text (e.g., "SBI Alert: KYC Pending. Update immediately via bit.ly/...").

**Inference**: Execute the analysis. The AI will decompose the message into:

* **Risk Vector**: High/Critical.
* **Manipulation Tactic**: Authority Bias + Urgency.
* **Countermeasures**: Specific tactical steps for containment.

---

## 🔮 Roadmap \& Future Scope

- [ ] **Multimodal Analysis**: Integrating OCR (Optical Character Recognition) to scan screenshots and QR codes.
- [ ] **RAG Integration**: Connecting to a vector database (ChromaDB) of known scam patterns for historical cross-referencing.
- [ ] **Edge Deployment**: Porting the inference engine to ONNX for client-side execution on mobile devices.
- [ ] **Fine-Tuning**: Training a LLaMA-3 adapter specifically on cyber-threat datasets for higher precision.

---

## 🤝 Contribution Guidelines

We welcome pull requests from the security research community.

1. Fork the repo and create your feature branch (`git checkout -b feat/neural-upgrade`).
2. Ensure code adheres to PEP-8 standards.
3. Submit a PR with a detailed description of the architectural changes.

---

## 👨‍💻 Author \& Maintainer

**Ankit Choubey (Master AK)**
AI Enthusiast | Full-Stack AI Architect | 

**GitHub**: [ankit-choubey](https://github.com/ankit-choubey)
**Team**: CodeHashiras
**Affiliation**: SRM University AP
**Focus Areas**: Generative AI, Fintech Security, \& Large Scale Distributed Systems.

*"Engineering the immune system for the digital age."*

```
