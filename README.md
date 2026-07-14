# Shoukaku Bot

Shoukaku is a multi-purpose Discord bot focused on music, media tools, moderation, utility commands, and entertainment.

> **This repository is the public documentation hub for Shoukaku.**
> The application source code, deployment configuration, credentials, and internal infrastructure are maintained separately.

## Quick Links

- [Invite Shoukaku](https://discord.com/oauth2/authorize?client_id=1472185156809920615&permissions=8&integration_type=0&scope=bot)
- [Support Server](https://discord.gg/qGwKsqH62k)
- [Service Status](https://altergolden.dev)
- [Command Reference](COMMANDS.md)
- [Privacy Policy](PP.md)
- [Terms of Service](TOS.md)
- [FAQ](FAQ.md)

## What Shoukaku Does

| Area | Highlights |
|---|---|
| Music | Playback, queues, history, autoplay, loop, shuffle, and voice-channel controls |
| Media | Media lookup, supported-platform downloads, and embed assistance |
| Moderation | Warnings, cases, mutes, kicks, bans, automoderation, anti-raid, and server protection |
| Utility | AFK, avatar, role, user, and server information, reporting, and general tools |
| Integrations | Anime, Reddit, Pixiv, Steam, Wikipedia, Rule34, and other supported services |
| Entertainment | Fun and community-oriented commands |

Use `/help` in Discord for the latest command list. The public command overview is available in [COMMANDS.md](COMMANDS.md).

## Documentation

| Document | Purpose |
|---|---|
| [Command Reference](COMMANDS.md) | Public command categories and currently documented commands |
| [Technology](TECHNOLOGY.md) | High-level tools, services, and architecture used by the project |
| [FAQ](FAQ.md) | Common setup, usage, availability, privacy, and support questions |
| [Privacy Policy](PP.md) | Information the official hosted service may process and how it is handled |
| [Terms of Service](TOS.md) | Rules and conditions for using the official hosted service |

## Repository Relationship

Shoukaku is split into two repositories with different audiences:

| Repository | Visibility and purpose |
|---|---|
| [`alG-N/ShoukakuDocs`](https://github.com/alG-N/ShoukakuDocs) | Public, user-facing documentation and the canonical Privacy Policy and Terms of Service |
| [`alG-N/ShoukakuBot`](https://github.com/alG-N/ShoukakuBot) | Backend implementation and operational documentation intended for maintainers and approved collaborators |

The public documentation must not contain credentials, private configuration, internal monitoring access details, or secrets from the backend repository.

## Technology Overview

Shoukaku is built primarily with TypeScript and Node.js. The hosted stack uses Discord.js, PostgreSQL, Redis, Lavalink, Docker, media-processing services, and optional observability tools.

See [TECHNOLOGY.md](TECHNOLOGY.md) for a high-level breakdown. That document intentionally describes technologies without publishing sensitive deployment details.

## Inspiration

> This section is reserved for the project owner to complete.

You can write about:

- why the name **Shoukaku** was chosen
- the original idea or personal goal behind the bot
- bots, communities, games, characters, or projects that influenced it
- the design principles Shoukaku should follow
- people or projects you want to acknowledge
- how Shoukaku has changed since its first version

## Availability and Changes

Shoukaku is an actively developed service. Commands, integrations, limits, and availability may change as Discord, third-party APIs, and project requirements evolve.

For the most current behavior:

1. Use `/help` in Discord.
2. Check the [support server](https://discord.gg/qGwKsqH62k).
3. Check the [status page](https://altergolden.dev).

## Privacy, Safety, and Abuse Reports

- Shoukaku does not sell personal data.
- Some features process Discord identifiers, command inputs, moderation records, temporary media data, and technical logs as described in the [Privacy Policy](PP.md).
- Users must follow Discord's rules, applicable laws, and the [Terms of Service](TOS.md).
- Security issues, abuse reports, and data requests should be submitted through the official support server.

Do not publish security vulnerabilities, tokens, credentials, personal data, or exploit instructions in public issues.

## Documentation Contributions

Corrections and improvements to public documentation are welcome. Keep submissions limited to public information and do not copy secrets or private infrastructure details from the backend repository.

## Rights

Unless the repository owner states otherwise, the Shoukaku name, branding, documentation, bot implementation, and infrastructure remain the property of their respective owner. Third-party names, trademarks, APIs, and content remain the property of their respective owners.