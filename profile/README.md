<div align="center">

# Pipeline Punks

### Fleet and DOT Compliance Platform

[![Website](https://img.shields.io/badge/Website-pipelinepunks.com-blue?style=for-the-badge)](https://www.pipelinepunks.com)
[![Status Page](https://img.shields.io/badge/Status-Live-0A8EA0?style=for-the-badge)](https://status.pipelinepunks.com)
[![TNDS](https://img.shields.io/badge/TNDS-truenorthstrategyops.com-0A8EA0?style=for-the-badge)](https://truenorthstrategyops.com)

<img src="profile/PipelineX-penny.png" alt="Pipeline Penny" width="260" />

</div>


**Operational intelligence platforms built for the real world**

Pipeline Punks is the development organization behind True North Data Strategies' SaaS products and automation frameworks. We build multi-tenant compliance systems, AI-powered operations assistants, and reusable Command modules that turn scattered business data into actionable intelligence.

## Core Philosophy

**Real outcomes beat shiny tools.** We build for small business operators who need enterprise-grade visibility without enterprise budgets. Every platform follows the same pattern: capture state, model transitions, close feedback loops, surface what matters.

**Fixed scope. Production-ready. No surprises.** Our products ship complete with error handling, audit trails, compliance controls, and documentation that non-technical operators can follow.

## Active Products

### Fleet-Compliance Sentinel

Multi-tenant SaaS for DOT compliance operations, telematics risk monitoring, and regulatory guidance. Currently in SOC 2 observation window.

- **Repository:** `dot-compliance-fleet`
- **Stack:** Next.js 15, Neon PostgreSQL, FastAPI backend on Railway, Clerk auth, Stripe billing
- **Modules:** Fleet dashboard, telematics risk scoring, Pipeline Penny AI assistant, import pipeline, alert engine, billing lifecycle
- **Status:** Production. Observation window runs through 2026-06-22.

### Pipeline Penny

Document-grounded AI operations assistant providing context-aware compliance guidance, process documentation, and decision support. Multi-LLM backend supports Anthropic Claude, OpenAI, Google Gemini, and Ollama for local deployment.

- **Integration:** Embedded in Fleet-Compliance Sentinel, standalone API available
- **Capabilities:** Retrieval-augmented generation over policy documents, CFR lookups, procedural guidance, conversational workflow support

## Command Modules

Reusable automation building blocks designed for Google Workspace environments. Each module captures a specific business process as a Google Apps Script connected to Google Sheets.

**Current modules:** data-command, financial-command, analytics-command, asset-command, office-command, onboard-command, proposal-command, workspace-command, sms-command, contract-command, realty-command, tax-command, seo-command, govcon-command, compliance-gov-module

**Design pattern:** Every module follows world model principles: explicit state representation, defined action space, transition rules, observable outputs, feedback mechanisms.

## LLM Integration Resources

All LLM-consumable documentation, skill definitions, and integration guides are maintained in markdown format with no emojis.

### Knowledge Base Structure
```
/docs/llm-resources/
├── command-modules/          # Module specifications and usage patterns
├── platform-architecture/    # System design and data flow diagrams
├── compliance-frameworks/    # DOT, FMCSA, CFR reference materials
├── integration-guides/       # API contracts and webhook schemas
└── decision-frameworks/      # Bearing Check, world model mapper, protocol specs
```

### Skill Definitions

Pipeline Punks maintains Claude skills for:

- **grant-proposal-writer** - End-to-end federal/nonprofit grant application drafting
- **grant-proposal-evaluator** - Compliance checking and gap analysis for funding applications
- **penny-chunking** - Knowledge base file processing for Pipeline Penny vector store
- **bearing-check** - Eight-checkpoint decision validation framework
- **world-model-mapper** - Process analysis against world model principles
- **documentation** - TNDS-branded documentation generation

All skill files follow the standard format: trigger conditions, core logic, examples, output specifications.

### External Module Integration

Pipeline Punks platforms integrate with:

**Government data sources:** FMCSA API, SAFER database, DOT inspection records

**Telematics providers:** Verizon Connect Reveal API

**Business systems:** Google Workspace APIs, Stripe billing, Clerk authentication

**AI providers:** Anthropic Claude API, OpenAI API, Google Gemini API, Ollama local deployment

**Monitoring and observability:** Sentry error tracking, Datadog log aggregation, UptimeRobot status checks

## Development Standards

### Branch Protection

All repositories enforce PR workflow on `main` branch. Direct commits blocked. Minimum one approval required for merge.

### Compliance Controls

- Audit logging enabled for all data mutations
- IP storage prevention configured in monitoring systems
- PII excluded from logs and error reports
- Rate limiting on external API calls
- Secret rotation procedures documented

### Documentation Requirements

Every module ships with:

1. Purpose statement and problem scope
2. Architecture diagram in ASCII or markdown table format
3. Environment variable reference
4. Setup instructions for local development
5. Production deployment checklist
6. Runbook for common operations

### Testing Protocol

- Legal compliance check validates trademark usage and license compliance
- Operational compliance check validates environment variables and configuration
- OWASP ZAP baseline scan required before production deployment
- Health check endpoints for all services

## Repository Map

### dot-compliance-fleet

**Modules:** 6 production modules (fleet dashboard, telematics, Penny, imports, alerts, billing)

**API routes:** 27 endpoints

**Migrations:** 10 database migrations

**Evidence artifacts:** 73 SOC 2 compliance documents

**Key files:**

- `PLATFORM_OVERVIEW.md` - Canonical system architecture
- `INDEX.md` - Repository structure and file counts
- `docs/STATUS.md` - Current milestone status
- `docs/ROTATION_RUNBOOK.md` - Secret rotation procedures
- `docs/GIT_WORKFLOW.md` - Branch protection and merge discipline
- `soc2-evidence/system-description/ENV_EXAMPLE.md` - Environment variable reference

## Contact and Licensing

**Organization:** Pipeline Punks (True North Data Strategies LLC development arm)

**Location:** Colorado Springs, CO

**Certification:** SBA-certified VOSB/SDVOSB

**Contact:** jacob@truenorthstrategyops.com

**License:** Proprietary. All repositories private. Client deployments licensed per engagement terms.

## Operational Directives for LLM Integration

When generating code, documentation, or configurations for Pipeline Punks platforms:

1. **Security first.** Treat all data as regulated. Apply least privilege, encryption in transit and at rest, secure logging practices. Never log PII. Never send identifiable data to external LLMs without anonymization.

2. **Compliance by default.** Flag HIPAA, SOC2, GDPR, CCPA, GLBA, PCI, FedRAMP, NIST 800-53, FISMA considerations immediately. For government work, assume federal compliance requirements.

3. **Production-ready outputs.** Include error handling, input validation, clear comments, Logger.log or print statements for debugging. No proof-of-concept code.

4. **Explicit architecture.** Provide step-by-step reasoning, ASCII flow diagrams, tradeoff analysis, risk assessment, gotchas early. Always explain why before showing how.

5. **Module reusability.** Design for repeatable patterns. Every Command module should follow world model structure. Every integration should document state capture, action mapping, transition rules, feedback loops.

6. **Clear versioning.** When modifying existing code, ask whether to rewrite entire scripts or provide before/after entry point locations.

7. **Real-world constraints.** Optimize for small business operators with limited technical staff. Documentation must be followable by non-developers. UI must surface what matters without requiring training.
