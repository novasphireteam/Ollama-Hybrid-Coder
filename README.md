# 🟠 NovaSpire AI Coder

<div align="center">

**Tier 5+ Autonomous Coding Agent with Strict Quality Standards**

[![Coming Soon](https://img.shields.io/badge/status-coming%20soon-orange)](https://github.com/novaspire/novaspire-coder)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Quality: Tier 5+](https://img.shields.io/badge/quality-tier%205%2B-red.svg)](https://github.com/novaspire/novaspire-coder)

</div>

---

## 🚀 Overview

**NovaSpire AI Coder** is an enterprise-grade hybrid autonomous coding agent built with military precision and aerospace-quality standards. It combines Retrieval-Augmented Generation (RAG), strict LLM output control, and deterministic verification to deliver reliable, high-quality code generation.

### Key Features

- 🔍 **Knowledge Pipeline** — Project-aware RAG with .md parsing and vector search
- 🛡️ **Quality Gates** — 6 non-negotiable quality gates (TYPES, COMPLEXITY, SAFETY, STRUCTURE, DOMAIN, TESTING)
- 🔄 **Hybrid Loop** — State machine: PLAN → RETRIEVE → GENERATE → VERIFY → APPLY
- 🤖 **Model Routing** — Intelligent selection between reasoning and coding models
- ✅ **Auto-Repair** — Critic + auto-correction loop for iterative improvement
- 🔒 **Safety Gates** — No changes without verification
- ⚡ **Optimization** — Caching, parallel verification, model ensembling
- 🎯 **Autonomy** — Task decomposition, roadmap understanding, feature-level planning
- 💬 **VSCode Extension** — Chat interface with code actions

---

## 🏗️ Architecture

NovaSpire AI Coder follows a modular architecture with strict separation of concerns:

```
┌─────────────────────────────────────────────────────────────┐
│                     VSCode Extension                        │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐  │
│  │  Chat UI │  │ Code Act │  │File Ctxt │  │ Backend  │  │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘  │
└─────────────────────────────────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                        Hybrid Loop                            │
│  ┌──────────────────────────────────────────────────────┐  │
│  │ PLAN → RETRIEVE → GENERATE → VERIFY → APPLY           │  │
│  └──────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────┘
         │           │           │           │           │
         ▼           ▼           ▼           ▼           ▼
┌─────────┐  ┌─────────┐  ┌─────────┐  ┌─────────┐  ┌─────────┐
│  RAG    │  │  LLM    │  │Verifier │  │Tooling  │  │ Autonomy │
│ Pipeline│  │  Layer  │  │  Layer  │  │  Layer  │  │   Layer  │
└─────────┘  └─────────┘  └─────────┘  └─────────┘  └─────────┘
```

### Components

- **Kernel** — State machine, hybrid loop, safety gates, autonomy
- **RAG** — .md parsing, chunking, embedding, vector search, context builder
- **LLM** — Ollama integration, system prompt, schema validation, model routing
- **Verifier** — Critic, auto-repair, policy enforcement, parallel verification
- **Tooling** — File executor, git integration, test runner, static analysis

---

## 🎯 Quality Standards

NovaSpire AI Coder enforces **Tier 5+ Absolute Override** quality standards:

### 6 Quality Gates (NON-NEGOTIABLE)

1. **TYPES** — 100% type coverage, mypy --strict, no `Any` without justification
2. **COMPLEXITY** — O() notation documented in all docstrings
3. **SAFETY** — No hardcoded secrets, XSS, injection vulnerabilities
4. **STRUCTURE** — frozen=True, slots=True on all dataclasses
5. **DOMAIN** — Domain-specific standards compliance
6. **TESTING** — Edge cases documented and handled

### Critical Violations (AUTO-REJECT)

- Hardcoded credentials/secrets
- Race conditions / memory leaks
- XSS/SQL injection/Path traversal
- O(n²) where O(n log n) is possible
- Untyped functions
- Unhandled exceptions
- Blocking I/O in async context

---

## 🔧 Technology Stack

### Backend
- **Python 3.10+** — Core implementation
- **Ollama** — Local LLM inference (CodeLlama, LLaMA2)
- **sentence-transformers** — Embeddings
- **FAISS/Qdrant** — Vector search
- **httpx** — Async HTTP client
- **GitPython** — Git integration
- **pytest** — Testing
- **mypy** — Type checking
- **pylint** — Linting
- **bandit** — Security analysis

### VSCode Extension
- **TypeScript 5.0+** — Extension implementation
- **VSCode API** — Editor integration
- **Webview API** — Chat interface

---

## 🛠️ Installation (Coming Soon)

### Prerequisites
- Python 3.10 or higher
- Ollama (for local LLM)
- VSCode (for extension)

### Backend Setup
```bash
# Clone repository
git clone https://github.com/novaspire/novaspire-coder.git
cd novaspire-coder

# Install dependencies
pip install -r requirements.txt

# Install Ollama
curl -fsSL https://ollama.com/install.sh | sh

# Pull CodeLlama model
ollama pull codellama

# Start backend server
python -m nova_backend.server
```

### VSCode Extension
```bash
# Navigate to extension directory
cd src/vscode_extension

# Install dependencies
npm install

# Compile TypeScript
npm run compile

# Package extension
vsce package

# Install in VSCode
code --install-extension novaspire-coder-1.0.0.vsix
```

---

## 📖 Usage (Coming Soon)

### VSCode Extension

1. Open NovaSpire AI Chat from the activity bar
2. Ask questions about your code
3. Use code actions (Explain, Generate, Refactor, Analyze)
4. Apply suggested code directly to your files

### Command Line

```python
from nova_coder import NovaSpireCoder

# Initialize agent
agent = NovaSpireCoder()

# Generate code
result = agent.generate("Create a function to sort a list")

# Explain code
explanation = agent.explain(code_string)

# Refactor code
refactored = agent.refactor(code_string)
```

---

## 🤝 Contributing

Contributions are welcome! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes with descriptive messages
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code Standards

All contributions must pass:
- 100% type coverage (mypy --strict)
- All 6 Quality Gates
- No critical violations
- Frozen dataclasses with slots=True

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Ollama for local LLM inference
- sentence-transformers for embeddings
- FAISS for vector search
- VSCode for the extension platform

---

## 📞 Contact

www.novaspire-ai.com
support@novaspire-ai.com

---

<div align="center">

**Built with 🟠 NovaSpire AI — Tier 5+ Absolute Override**

</div>
