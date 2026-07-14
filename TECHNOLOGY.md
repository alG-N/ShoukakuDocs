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
| Lavalink | Audio playback and source handling |
| Shoukaku / lavalink-client | Application-side Lavalink connectivity and player management |

Music availability depends on the configured Lavalink nodes and supported audio sources.

## Media Processing

| Technology | Role in Shoukaku |
|---|---|
| Cobalt | Supported media retrieval and processing workflows |
| yt-dlp | Provider-specific extraction and fallback media processing |
| Media proxy services | Controlled delivery of supported media and public health/status routes |

Media commands may pass a user-provided URL or query to a required processing service. Supported platforms can change when third-party websites or APIs change.

## External Integrations

Shoukaku may integrate with services used for:

- anime information;
- Reddit content;
- Pixiv content;
- Steam information;
- Wikipedia searches;
- supported media and embed providers;
- age-restricted content providers where enabled and permitted.

Each integration remains subject to the third party's availability, terms, rate limits, and content rules.

## Deployment and Infrastructure

| Technology | Role in Shoukaku |
|---|---|
| Docker and Docker Compose | Reproducible application and service deployment |
| Linux / Ubuntu | Primary production-style host environment |
| Cloudflare tooling | Optional networking and public-route support |
| Nginx or proxy components | Controlled routing for selected public or internal services |

The exact production topology is private and may change without being reflected in this public overview.

## Reliability and Observability

| Technology | Role in Shoukaku |
|---|---|
| Prometheus | Metrics collection |
| Grafana | Operational dashboards |
| Alertmanager | Alert routing |
| Sentry | Optional error reporting and diagnostics |
| Structured logging | Debugging, reliability, security, and abuse investigation |

Public users do not receive access to protected operational dashboards, credentials, or detailed diagnostics.

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
    +--> Lavalink for music
    +--> Media services for supported downloads
    +--> Third-party APIs for requested content
    |
    v
Response returned through Discord
```

## Public and Private Boundaries

Public documentation may describe:

- user-facing commands;
- high-level technologies;
- general feature behavior;
- Privacy Policy and Terms of Service;
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
