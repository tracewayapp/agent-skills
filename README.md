<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="Traceway%20Logo%20White.png" />
    <source media="(prefers-color-scheme: light)" srcset="Traceway%20Logo.png" />
    <img src="Traceway Logo.png" alt="Traceway Logo" width="200" />
  </picture>
</p>

# Traceway Agent Skills

Skills for coding agents (Grok Build, Claude Code, and others) to set up and operate [Traceway](https://tracewayapp.com), an error tracking and monitoring platform.

## Skills

| Skill | What it does |
|---|---|
| [`traceway`](skills/traceway/SKILL.md) | Operates a Traceway instance through the `traceway` CLI: log in, query exceptions, logs, endpoints, and metrics, and debug production issues down to root cause. |
| [`traceway-setup`](skills/traceway-setup/SKILL.md) | Connects a project to a Traceway instance so it reports endpoints, spans, errors, background tasks, AI traces, and metrics. Backends use OpenTelemetry over OTLP/HTTP, frontends and mobile apps use the Traceway SDKs. |

## Usage

Once installed, invoke the skills from your agent:

- `/traceway login`, `/traceway debug <issue>`, or `/traceway what's broken in prod` to investigate errors, crashes, slowness, or logs
- `/traceway-setup with token <token> and url <instance url>` to instrument a project

## Repository layout

```
skills/
├── traceway/
│   └── SKILL.md
└── traceway-setup/
    ├── SKILL.md
    └── data-model.md
```

## Links

- [Traceway](https://tracewayapp.com)
- [Main repository](https://github.com/tracewayapp/traceway)
- [Documentation](https://tracewayapp.com/docs)

## License

[MIT](LICENSE)
