# ADL – Frequently Asked Questions (FAQ)

For questions or contributions, visit: https://github.com/nextmoca/adl/issues

## What is ADL?
ADL (Agent Definition Language) is an open, declarative standard for defining AI agents in a structured, portable, and framework-independent way. It describes an agent’s role, capabilities, tools, workflows, inputs, outputs, context needs, governance rules, and metadata.

## Is ADL just a JSON schema?
No. While ADL can be expressed in JSON or YAML, it is a full specification for agent behavior, capabilities, tool permissions, workflows, metadata, and constraints. Like OpenAPI or Terraform, the value is in the declarative standard, not the file format.

## How is ADL different from Instructor?
| Feature | ADL | Instructor |
|--------|-----|------------|
| Purpose | Define entire agents declaratively | Structured LLM output enforcement |
| Scope | Capabilities, tools, workflows, governance | JSON schemas for model outputs |
| Layer | Definition layer | Runtime/inference |
| Portability | Framework-agnostic | Python-specific |
| Governance | Yes | No |

Instructor standardizes *outputs*; ADL standardizes *agents*.

## Why not define agents in Python?
Python is ideal for execution, but poor for:
- Governance and auditing  
- Static inspection  
- Versioning and collaboration  
- Multi-runtime portability  
- Auto-generation of UIs, docs, SDKs  

Declarative specs enable interoperability and governance, similar to OpenAPI or Terraform.

## What practical problems does ADL solve?
### 1. Governance & Compliance
Clear, static definitions of tool permissions, safety rules, and capabilities.

### 2. Team Collaboration
Non-engineers can read, review, and propose changes.

### 3. Portability & Interoperability
Agents can run across multiple frameworks without rewrites.

### 4. Multi-agent Systems
ADL defines workflows, interfaces, and contracts between agents.

### 5. Auto-generation
ADL can generate UIs, SDKs, documentation, and CLIs.

## What does an ADL workflow look like?
1. Write ADL spec  
2. Validate governance  
3. Load into runtime  
4. Execute with defined tools  
5. Monitor and version changes  

## Is ADL tied to Next Moca?
No. ADL is open source and vendor-neutral. Next Moca is a contributor, not an owner.

## Where can I ask questions or propose improvements?
GitHub Issues: https://github.com/nextmoca/adl/issues
