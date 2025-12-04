# ADL — Agent Definition Language

ADL (Agent Definition Language) is a vendor-neutral, declarative standard for defining AI agents, their tools, RAG inputs, LLM settings, permissions, and dependencies. It is designed for enterprise-grade governance, interoperability, and democratized agent development across verticals.

## Badges

<p align="center">
  <img src="https://img.shields.io/badge/license-Apache%202.0-blue" alt="Apache 2.0 License"/>
  <img src="https://img.shields.io/badge/schema-validated-brightgreen" alt="Schema Validated"/>
  <img src="https://img.shields.io/github/last-commit/nextmoca/adl" alt="Last Commit"/>
  <img src="https://img.shields.io/github/contributors/nextmoca/adl" alt="Contributors"/>
  <img src="https://img.shields.io/github/repo-size/nextmoca/adl" alt="Repo Size"/>
</p>

---

## Overview

ADL exists to solve fragmentation in how AI agents are defined. Today, every vendor and framework defines “agents” differently. ADL provides a unified, human-readable, machine-validated specification for what an agent *is* — its role, tools, parameters, LLLM configuration, permissions, dependencies, and RAG inputs.

If OpenAPI defines APIs and Terraform defines infrastructure, ADL defines **AI agents**.

---

## Key Features

- **Declarative JSON Schema** for agent definition  
- **Cross-vendor interoperability**  
- **Clear tool and capability specification**  
- **Sandbox + permission semantics**  
- **RAG index definitions**  
- **LLM configuration standardization**  
- **Governance & auditability**  
- **Extensible structure for future versions**

---

## Why Apache 2.0 License?

ADL uses **Apache License 2.0** because it is the best license for:  
- Enterprise adoption  
- Vendor-neutral governance  
- Patent protection  
- Long-term standardization  
- Ecosystem trust  

All major open standards (Kubernetes, Kafka, Arrow, OpenTelemetry) use Apache 2.0.

---

## Repository Structure

```
adl/
  README.md
  LICENSE
  schema/
    agent-definition.schema.json
  examples/
    creative_producer_agent.json
    minimal_agent.json
  docs/
    index.md
    governance.md
    roadmap.md
    whitepaper.md
  tools/
    validate.py
    validate.js
  CONTRIBUTING.md
```

---

## Getting Started

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
