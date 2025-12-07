# Agent Definition Language (ADL)

A vendor-neutral JSON-based specification for defining AI agents, their tools, and RAG indices.

This repo contains:

- `schema/agent-definition.schema.json` — the canonical JSON Schema
- `examples/` — real-world agent definitions that validate against the schema
- `tools/` — simple validation utilities (Python and Node.js)
- `docs/` — human-readable documentation
- `CONTRIBUTING.md` — contribution and versioning guidelines

For questions or contributions, visit: https://github.com/nextmoca/adl/issues

## Getting Started

### Clone

```bash
git clone https://github.com/<your-org-or-user>/agent-definition-language.git
cd agent-definition-language
```

### Validate an agent JSON (Python)

```bash
pip install jsonschema
python tools/validate.py examples/creative_producer_agent.json
```

### Validate an agent JSON (Node.js)

```bash
npm install
node tools/validate.js examples/creative_producer_agent.json
```

## Versioning

The schema is versioned in two ways:

1. **Repository tags / releases** using semantic versioning (semver), e.g. `v0.1.0`, `v1.0.0`.
2. **Agent documents** use their own `version` field (an integer) to represent the version of a specific agent definition.

See `CONTRIBUTING.md` and `docs/schema-reference.md` for details.
