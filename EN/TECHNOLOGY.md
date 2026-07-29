# Technology and Architecture

This page describes Shoukaku's technology at a public, high level. It intentionally excludes credentials, private endpoints, internal network access details, production secrets, and protected operational procedures.

## Core Application

| Technology | Role in Shoukaku |
|---|---|
| TypeScript | Primary application language and type-safe development surface |
| Node.js 22 | JavaScript runtime for the bot backend |
| Discord.js v14 | Discord gateway, interactions, commands, permissions, and voice integration |
| PostgreSQL | Persistent storage for durable feature, moderation, and user-music data |
| Redis | Shared cache, cooldowns, temporary state, media mappings, and multi-process coordination |
| Knex | Database migration and query tooling |

## Command Registration

Commands are loaded through explicit category manifests and module exports. The Discord deployment path performs a bulk overwrite of the application command list.

The complete public inventory is documented in [COMMANDS.md](COMMANDS.md):

- active commands are exported by the current registry;
- restricted commands are registered but access-controlled;
- disabled commands may remain in source or tests but are not exported by the official command registry.

A source-code change does not remove a previously deployed Discord command until the current registry is successfully deployed.

## Music

| Technology | Role in Shoukaku |
|---|---|
| Lavalink | Audio playback and approved source handling |
| Shoukaku / lavalink-client | Application-side Lavalink connectivity and player management |
| PostgreSQL | User preferences, favorites, and listening history |
| Redis | Active queue, session, cache, and shard-coordination state |

The current `/music` surface includes playback, queue editing, seeking, preferences used by the playback system, favorites in the backend data model, history, and autoplay-related behavior.

Music availability depends on configured nodes and approved sources. The official service must not intentionally use user-supplied credentials or technical measures to bypass private, paid, subscriber-only, age, region, or DRM restrictions. The backend may use its own service or API credentials for approved provider integrations where permitted.

## Media Processing

| Technology | Role in Shoukaku |
|---|---|
| Cobalt | Internal media retrieval and processing component |
| yt-dlp | Provider-specific extraction component used only in approved workflows |
| Media proxy services | Controlled preparation and delivery of temporary public media previews |
| Redis media store | Stable media identifiers and short-lived YouTube source mappings |
| Cloudflare R2 | Optional temporary public-object delivery for generated previews |

The official hosted deployment enables `/download` through `DOWNLOAD_COMMAND_ENABLED`. `/download` is limited to supported public media that the user owns, has permission to use, or may use under applicable law. The `/media` workflow supports selected social embed repairs, direct public image or GIF links, and supported public media previews. Users must not submit account credentials, private links, paid content, restricted content, or DRM-protected material.

Some supported third-party image hosts can contain mature material. The official service does not register dedicated adult-content commands, but server administrators and users remain responsible for appropriate channel use and compliance with Discord rules.

### Current media lifetimes

| Media data | Current default or cap |
|---|---|
| Downloaded source file used during processing | Maximum age of 1,800 seconds by default |
| Temporary public R2 preview object, when enabled | Retention target of 86,400 seconds |
| Stable YouTube media mapping in Redis | Renewable TTL of 604,800 seconds by default |
| Absolute lifetime of that Redis mapping | Capped at 2,592,000 seconds from creation by default |
| Direct upstream URL cache | 300 seconds by default |
| Signed media URL authorization | Up to 86,400 seconds |

The seven-to-30-day Redis period applies to mapping metadata such as the canonical source URL, video and format identifiers, representation metadata, timestamps, and integrity values. It does not mean the downloaded source file is retained for 30 days.

Configuration can be changed by the Operator, but the public Privacy Policy must be updated when a change materially affects user data retention.

## External Integrations

Shoukaku may integrate with services used for:

- anime information;
- Reddit content;
- Pixiv content;
- Steam information;
- Wikipedia searches;
- Spotify-assisted recommendations where configured;
- approved public music, media, image, and embed providers.

Dedicated adult-content integrations are not registered in the official hosted service. Each enabled integration remains subject to the third party's availability, terms, rate limits, privacy practices, and content rules.

## Deployment and Infrastructure

| Technology | Role in Shoukaku |
|---|---|
| Docker and Docker Compose | Reproducible application and service deployment |
| Linux / Ubuntu | Primary production-style host environment |
| Cloudflare tooling | Optional networking and public-route support |
| Nginx or proxy components | Controlled routing for selected public or internal services |

The exact production topology may change and is not fully described in this public overview.

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
    +--> PostgreSQL for durable configuration, moderation, and music data
    +--> Redis for shared temporary state and media mappings
    +--> Lavalink for approved music sources
    +--> Media services for approved temporary processing
    +--> Third-party APIs for requested public information
    |
    v
Response returned through Discord
```

## Public and Private Boundaries

Both the documentation and backend repositories are publicly viewable. Public source visibility does not authorize publication of production data or secrets and does not itself create an open-source license.

Public material may describe:

- user-facing and disabled command inventory;
- high-level technologies;
- general feature behavior;
- privacy, terms, IP, and security policies;
- support and status information;
- implementation code already present in the public backend repository.

The following must remain private:

- tokens, passwords, API keys, cookies, and credentials;
- private production configuration and unannounced endpoints;
- protected dashboard authentication and access details;
- database contents, backups, private logs, and personal data;
- anti-abuse thresholds that would enable bypassing protections;
- incident details or vulnerability information that would create active risk.

## Repository Links

- Public documentation: https://github.com/alG-N/ShoukakuDocs
- Publicly viewable backend source: https://github.com/alG-N/ShoukakuBot

Use and redistribution remain subject to the license or copyright notice in each repository.
