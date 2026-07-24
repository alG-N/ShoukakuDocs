# Technology and Architecture

This page describes Shoukaku's technology at a public, high level. It intentionally excludes credentials, private endpoints, internal network details, production secrets, and restricted operational procedures.

## Core Application

| Technology | Role in Shoukaku |
|---|---|
| TypeScript | Primary application language and type-safe development surface |
| Node.js 22 | JavaScript runtime for the bot backend |
| Discord.js v14 | Discord gateway, interactions, commands, permissions, and voice integration |
| PostgreSQL | Persistent storage for durable feature and moderation data |
| Redis | Shared cache, cooldowns, temporary state, and multi-process coordination |
| Knex | Database migration and query tooling |

## Music

| Technology | Role in Shoukaku |
|---|---|
| Lavalink | Audio playback and approved source handling |
| Shoukaku / lavalink-client | Application-side Lavalink connectivity and player management |

Music availability depends on configured nodes and approved sources. The official service must not intentionally use credentials or technical measures to bypass private, paid, age, region, or DRM restrictions.

## Media Processing

| Technology | Role in Shoukaku |
|---|---|
| Cobalt | Internal media retrieval and processing component |
| yt-dlp | Provider-specific extraction component used only in approved workflows |
| Media proxy services | Controlled delivery of temporary media and public health/status routes |

The public `/download` command is disabled. The remaining `/media` workflow is intended for supported public content and embed assistance only. Users must not submit account credentials, private links, paid content, restricted content, or DRM-protected material.

Temporary source files used by the current media stack are configured for automatic cleanup, with the default source-file maximum age set to 1,800 seconds. Public-object retention, when enabled, must follow the configured lifecycle and the [Privacy Policy](PP.md).

## External Integrations

Shoukaku may integrate with services used for:

- anime information;
- Reddit content;
- Pixiv content;
- Steam information;
- Wikipedia searches;
- approved public media and embed providers.

Adult-content integrations are not registered in the official hosted service. Each enabled integration remains subject to the third party's availability, terms, rate limits, privacy practices, and content rules.

## Deployment and Infrastructure

| Technology | Role in Shoukaku |
|---|---|
| Docker and Docker Compose | Reproducible application and service deployment |
| Linux / Ubuntu | Primary production-style host environment |
| Cloudflare tooling | Optional networking and public-route support |
| Nginx or proxy components | Controlled routing for selected public or internal services |

The exact production topology is private and may change without being reflected in this public overview.

## Reliability, Logging, and Observability

| Technology | Role in Shoukaku |
|---|---|
| Prometheus | Metrics collection |
| Grafana | Operational dashboards |
| Alertmanager | Alert routing |
| Sentry | Optional error reporting and diagnostics |
| Structured logging | Debugging, reliability, security, and abuse investigation |

The Docker deployment uses bounded rotating container-log files for core services. Optional external observability providers may apply their own configured retention. Public users do not receive access to protected dashboards, credentials, or detailed diagnostics.

## Development Quality

| Technology | Role in Shoukaku |
|---|---|
| Jest | Automated tests |
| ESLint | Static code-quality checks |
| Prettier | Consistent formatting |
| TypeScript strict checks | Type-safety and architecture guardrails |

## High-Level Request Flow

```text
Discord user
    |
    v
Discord interaction or event
    |
    v
Shoukaku command / handler
    |
    +--> PostgreSQL for durable data
    +--> Redis for shared temporary state
    +--> Lavalink for approved music sources
    +--> Media services for approved temporary processing
    +--> Third-party APIs for requested public information
    |
    v
Response returned through Discord
```

## Public and Private Boundaries

Public documentation may describe:

- user-facing commands;
- high-level technologies;
- general feature behavior;
- privacy, terms, IP, and security policies;
- support and status information.

The following must remain private:

- tokens, passwords, API keys, cookies, and credentials;
- internal hostnames, ports, firewall rules, and network topology;
- protected dashboard access details;
- database contents, backups, and production logs;
- anti-abuse thresholds that would enable bypassing protections;
- unpublished source code or infrastructure details.

## Repository Links

- Public documentation: https://github.com/alG-N/ShoukakuDocs
- Backend repository for maintainers and approved collaborators: https://github.com/alG-N/ShoukakuBot
