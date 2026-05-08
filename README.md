Ollama Hybrid Coder
A local hybrid AI coding‑agent powered by a structured kernel, verifier‑layer, multi‑step task engine, and strict output control.
Runs fully on your machine using Ollama as the LLM backend.

This project is the lightweight open‑source edition of the NovaSpire Hybrid AI system.

Overview
Ollama Hybrid Coder provides:

Hybrid pipeline combining deterministic logic with LLM generation

Verifier layer (critic, auto‑repair, policy enforcement)

Multi‑step task engine for feature‑level execution

RAG project context for accurate code generation

State persistence for long‑running tasks

Local execution with zero cloud dependencies

This version is ideal for developers who want a private, offline, zero‑cost coding assistant.

Installation
1. Install Ollama
Download from:
https://ollama.com/download

Verify installation:

Kode
ollama run llama3
2. Clone and install backend
Kode
git clone https://github.com/<your-repo>/ollama-hybrid-coder
cd ollama-hybrid-coder
pip install -r requirements.txt
Start backend:

Kode
python -m hybrid_backend
Default backend URL:

Kode
http://localhost:5005
3. Install VS Code Extension
Open VS Code

Go to Extensions

Search for: Ollama Hybrid Coder

Install

Configure backend URL in settings.json:

json
"hybridCoder.backendUrl": "http://localhost:5005"
Usage
Analyze a file
Command Palette →
Hybrid Coder: Analyze File

Implement a feature
Command Palette →
Hybrid Coder: Implement Feature

Multi‑step execution
The agent automatically performs:

PLAN

EXECUTE

VERIFY

REFLECT

Each step is validated through the verifier layer.

Architecture
Kode
src/
├── kernel/
│   ├── hybrid_loop.py
│   ├── state.py
│   ├── multi_step_tasks.py
│   ├── safety_gates.py
│   ├── rag_pipeline.py
│   └── verifier/
│       ├── critic.py
│       ├── auto_repair.py
│       └── policy_enforcer.py
└── backend/
    ├── server.py
    └── api.py
Core components:

Hybrid Loop

Safety Gates

RAG Context Engine

Verifier Layer

Task Engine

Privacy
No cloud calls

No external API keys

No telemetry

All code stays on your machine

Developer Program
We help you — in return we hope you help us.

This project is free and open‑source.
If you find it useful, we appreciate:

Starring the repository

Linking to the project

Sharing it with other developers

Writing about it

Contributing improvements

This is voluntary — not required.

Status
Version: v1.0
Stability: Tier 5+
Requirements: Python 3.11+, Ollama installed

License
MIT License (or your chosen license).

Contact
For issues, feature requests, or contributions:
Open an issue or pull request in the repository.
