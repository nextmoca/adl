# Contributing to ADL (Agent Definition Language)

Thank you for your interest in contributing to ADL — the Agent Definition Language maintained by Next Moca.  
ADL is designed to be a vendor-neutral, declarative standard for defining AI agents, their tools, RAG inputs, LLM settings, permissions, and dependencies. We welcome contributions that make the specification stronger, clearer, and more useful to the global ecosystem.

---

## 🧭 Guiding Principles

- **Interoperability first** — ADL should work across vendors, frameworks, and runtimes.
- **Clarity over complexity** — definitions must be easy to read, write, and validate.
- **Enterprise-grade governance** — permissioning, security, and auditability matter.
- **Backwards compatibility** — schema changes must be handled with discipline.
- **Ecosystem friendliness** — the community should be able to extend ADL safely.

---

## 🚀 Ways to Contribute

### 1. Improve Documentation
- Fix typos, unclear explanations, or missing examples.
- Enhance schema descriptions and field definitions.
- Add architecture diagrams, best practices, or tutorials.

### 2. Propose Schema Enhancements
- New fields for tools, RAG entries, or LLM configuration.
- Clarifications to existing structures.
- Major improvements via RFCs (see below).

### 3. Add Examples
- Realistic agent definitions for various industries.
- Tool definitions showcasing parameters and invocation types.

### 4. Enhance Validators / Tooling
- Python JSON schema validator improvements.
- Node / AJV validator improvements.
- CI/CD enhancements for schema linting and validation.

### 5. Community Engagement
- Reporting bugs.
- Suggesting enhancements.
- Providing feedback on RFCs.

---

## 📝 Workflow for Contributors

### Step 1: Fork the Repository
Click **Fork** on the GitHub page to create your own copy.

### Step 2: Create a Feature Branch
```bash
git checkout -b feature/your-feature-name
```

### Step 3: Make Your Changes
Ensure your changes include:
- Updated schema (if applicable)
- Updated documentation
- Validation tests
- New examples (if relevant)

### Step 4: Validate All Examples
```bash
python tools/validate.py examples/*.json
```

### Step 5: Commit and Push
```bash
git add .
git commit -m "Add: description of change"
git push origin feature/your-feature-name
```

### Step 6: Submit a Pull Request
Please include:
- Summary of changes  
- Motivation  
- Backwards compatibility notes  
- Links to relevant discussions or issues  

---

## 📘 The ADL RFC Process

Large or structural changes to the ADL schema require an **RFC (Request for Comments)**.

### When to create an RFC:
- Adding new schema sections
- Major restructuring
- Backwards-incompatible changes
- Introducing new ADL components (e.g., workflows, capabilities)

### RFC Workflow:
1. Open a GitHub Issue titled `[RFC] Proposal Name`
2. Create a document under `rfcs/` explaining:
   - Motivation  
   - Proposed changes  
   - Alternatives considered  
   - Impact on ecosystem  
3. Engage in discussion with maintainers and community
4. Receive approval from the Steering Committee
5. Implement changes and submit PR referencing the RFC

---

## 🧪 Local Development Setup

### Python Validator:
```bash
pip install jsonschema
python tools/validate.py examples/minimal_agent.json
```

### Node Validator:
```bash
npm install ajv
node tools/validate.js examples/minimal_agent.json
```

---

## 🔖 Versioning

ADL follows **Semantic Versioning (SemVer)**:
- **MAJOR** — breaking schema changes  
- **MINOR** — new fields or features  
- **PATCH** — fixes, clarifications, documentation  

Schema stability is important: breaking changes must go through RFC review.

---

## 🤝 Contributor Expectations

- Be respectful and constructive.
- Focus on clarity and correctness.
- Provide clear rationales for changes.
- Prioritize compatibility and usability.
- Align with ADL’s long-term vision.

---

## Thank You

By contributing to ADL, you’re helping create the foundation for safe, governed, interoperable enterprise AI.  
We deeply appreciate your time, expertise, and collaboration.

