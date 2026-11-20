# Sagent Lab — Agent & Voice Integration Experiments

> An experimental toolkit for local AI-agent workflows, provider integration, approval concepts and voice communication. This is a research/prototyping repository, not a production-ready assistant.

**Focus:** AI Agent Tooling · TypeScript · Shell Automation · Provider Abstraction · Voice Integrations

## Why this project exists

Sagent Lab explores how different AI-agent components can be combined into a controllable local developer workflow. The repository contains proof-of-concept implementations, shell-based utilities, integration experiments and technical design documents.

## What's in the repository

- **Provider abstraction:** TypeScript registry, configuration loader and demonstration scripts in `src/providers/` and `src/demo/`
- **Voice experiments:** pipeline, mock provider, Google Live and Twilio provider implementations under `voice/`
- **Agent utilities:** task, status, health-check, notifications and approval-related shell scripts under `scripts/`
- **Documentation:** security concepts, approval workflows, architecture proposals and spike notes under `docs/`
- **Configuration templates:** example provider and voice-call configs under `config/`

These components are experimental. The presence of a script or design document does not mean a fully integrated feature is production-ready.

## Development

Prerequisites: Node.js and npm. Some shell helpers assume a Unix-like environment and a separately configured local agent runtime.

```bash
npm install
npm run typecheck
npm run demo:providers
npm run demo:load-config
```

Additional integration scripts:

```bash
npm run test:google-live
npm run test:twilio
```

Network-backed variants require explicit opt-in and the relevant third-party services. Do not commit actual credentials. Start from the `*.example` configuration files.

## Architecture and documentation

- [Design direction](DESIGN.md)
- [Agent research](docs/FRAMEWORK-SPIKE-MATRIX.md)
- [Approval flow](docs/APPROVAL-FLOW.md)
- [Voice architecture](docs/LIVE-VOICE-ARCHITECTURE.md)
- [Commands](docs/COMMANDS.md)
- [OpenClaw integration notes](docs/OPENCLAW-AS-SAGENT.md)

## Security and limitations

This is a developer experiment, not a sandboxed agent service. Only run scripts after reviewing them and use a trusted local environment. Keep API keys, personal data and external-service credentials out of the repository. Provider availability, external costs and real-time integrations depend on your own configuration.

## Related work

- [Sagent](https://github.com/Santi-v3/sagent) — a separate local-first AI agent project with a FastAPI backend and Next.js interface.

## Author

**Santino Burkhardt** — Business Systems & Automations Specialist | AI & Software Automation
