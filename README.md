<p align="center">
  <img src="https://img.shields.io/badge/License-Apache_2.0-blue.svg" alt="License"/>
  <a href="https://github.com/nextmoca/adl">
    <img src="https://img.shields.io/badge/ADL-GitHub-black?logo=github" alt="GitHub Repo"/>
  </a>
  <img src="https://img.shields.io/badge/Schema-Validated-brightgreen" alt="Schema Status"/>
</p>

<h1 align="center">ADL — Agent Definition Language</h1>
<p align="center"><strong>A vendor-neutral, open standard for defining AI agents.</strong></p>

---

## 🚀 Overview

For questions or contributions, visit: https://github.com/nextmoca/adl/issues

## Getting Started
**ADL (Agent Definition Language)** is an open, declarative, vendor-neutral specification for defining AI agents in a consistent, auditable, and interoperable way.  
It provides a shared language for describing:

- an agent’s identity and purpose  
- its tools and capabilities  
- its LLM configuration  
- its access to knowledge (RAG)  
- its permissions and sandbox  
- its dependencies  
- its governance metadata  

If **OpenAPI defines APIs**, **ADL defines agents**.

---

## 🧠 Why ADL Exists

Enterprises adopting AI agents face several systemic challenges:

- Each vendor defines “agents” differently  
- Tool contracts are inconsistent  
- RAG pipelines are wired differently across apps  
- Permissions are rarely explicit  
- Governance teams have no centralized visibility  
- Agents are not portable across platforms  
- Vendor lock-in slows enterprise adoption  
- Compliance and auditability are fragile or impossible  

**ADL solves these problems** by introducing a single, declarative, versioned artifact that describes what an agent *is* and what it is *allowed* to do.

---

## 🧩 What ADL *Is*

ADL defines:

- **Identity** — name, description, role, owner, version  
- **LLM Settings** — provider, model, temperature, max tokens  
- **Tools & Actions** — typed parameters, descriptions, return schemas  
- **RAG Inputs** — indices, types, metadata, paths  
- **Permissions** — file I/O, network, env vars  
- **Dependencies** — Python packages with optional version pins  
- **Governance** — created_by, approved_by, timestamps, version notes  

This makes agents:

- portable  
- predictable  
- auditable  
- reproducible  
- interoperable across vendors  

---

## 🚫 What ADL *Is Not*

To avoid confusion, ADL explicitly does **not** define:

- ❌ A2A (agent-to-agent) communication protocols  
- ❌ runtime tool invocation semantics (e.g., MCP)  
- ❌ prompt templating or formatting  
- ❌ workflow orchestration (Airflow, Temporal, Dagster)  
- ❌ API schemas (OpenAPI already solves that)  
- ❌ message transport (HTTP, gRPC, JSON-RPC)  

**ADL is laser-focused on definition — not execution.**

---

## 🔍 ADL vs AI App Definition  
**ADL is an Agent Definition Language - not a general AI App definition format.**

AI apps are broad and may include UI, API layers, deployments, data stores, or business logic.

Agents are specific:

- they reason  
- they call tools  
- they retrieve knowledge  
- they act autonomously  
- they require permission boundaries  

ADL models **agent competencies**, not app-level infrastructure.

This is a key strategic distinction.

---

## 🔄 Comparing ADL to Other Standards

### **ADL vs A2A**
- **A2A**: defines how agents communicate  
- **ADL**: defines *what* an agent is  

### **ADL vs MCP**
- **MCP**: runtime tool protocol  
- **ADL**: declarative definition of tools and capabilities  

### **ADL vs OpenAPI**
- **OpenAPI**: describes HTTP services  
- **ADL**: describes agent behavior, boundaries, and capabilities  

### **ADL vs Workflow Engines**
- Workflows = *when & how tasks execute*  
- ADL = *which agent executes them*  

---

## 🌐 Why Next Moca Open Sourced ADL

Next Moca open-sourced ADL under **Apache 2.0** to enable:

### ✔ Ecosystem-wide interoperability  
### ✔ Enterprise trust and transparency  
### ✔ Neutral governance  
### ✔ Community-driven evolution  
### ✔ Vendor adoption without lock-in  
### ✔ Safe, compliant, standards-based agent deployment  

Open sourcing ensures ADL becomes a **true standard**, not a proprietary configuration format.

---

## 📘 Documentation

- 📄 ADL Spec (JSON Schema) — `/schema/adl.schema.json`  
- 📚 Examples — `/examples/`  
- 📐 Roadmap — `/ROADMAP.md`  
- 🏛 Governance — `/GOVERNANCE.md`  
- 🤝 Contributing — `/CONTRIBUTING.md`  

---

## 🛠 Getting Started

```bash
git clone https://github.com/nextmoca/adl.git
cd adl
```

### Validate an ADL Agent File

```bash
pip install jsonschema
python tools/validate.py examples/minimal_agent.json
```

Or using Node:

```bash
npm install ajv
node tools/validate.js examples/minimal_agent.json
```

---

## Minimal Example

```json
{
  "name": "campaign_image_generator",
  "description": "Generate a 1024x1024 marketing image from a creative brief.",
  "role": "Creative Producer",
  "llm": "openai",
  "llm_settings": {
    "temperature": 0,
    "max_tokens": 4096
  },
  "tools": [
    {
      "name": "generate_campaign_image",
      "description": "Generate a high-quality image from a prompt.",
      "parameters": [
        {
          "name": "prompt",
          "type": "string",
          "description": "Image prompt",
          "required": true
        }
      ],
      "invocation": { "type": "python_function" }
    }
  ],
  "rag": []
}
```

---

## Contributing

We welcome contributions!  
Please see **CONTRIBUTING.md** for guidelines on RFCs, schema updates, and tooling improvements.

---

## License

Licensed under the **Apache License, Version 2.0**.

---

## About Next Moca

Next Moca is the enterprise platform for multi-agent workflows, agent orchestration, RAG pipelines, governance, and AI system observability. ADL is the foundation for how agents are defined consistently across the ecosystem.
