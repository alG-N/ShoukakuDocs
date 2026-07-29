# Shoukaku Bot Documentation

**Language:** **EN** | [VI](../VI/README.md)

Shoukaku is a multi-purpose Discord bot focused on music, moderation, utility commands, and selected third-party integrations.

> **This repository is the public documentation hub for Shoukaku.**
> The backend source is also publicly viewable in a separate repository, but credentials, private configuration, production data, protected monitoring access, and internal secrets must never be published.

## Quick Links

- [Invite Shoukaku](https://discord.com/oauth2/authorize?client_id=1472185156809920615&permissions=8&integration_type=0&scope=bot+applications.commands)
- [Support Server](https://discord.gg/qGwKsqH62k)
- [Service Status](https://altergolden.dev)
- [Complete Command Reference](COMMANDS.md)
- [Privacy Policy](PP.md)
- [Terms of Service](TOS.md)
- [Copyright and IP Policy](IP_POLICY.md)
- [Security Policy](SECURITY.md)
- [FAQ](FAQ.md)
- [Vietnamese Documentation](../VI/README.md)

## Project Background

Shoukaku is an independent personal software project created to apply the Operator's experience with TypeScript, Discord applications, distributed services, moderation systems, and media infrastructure.

The name is used as a historical reference. Shoukaku is not affiliated with, endorsed by, or sponsored by Discord, C2 Praparat, Kadokawa, DMM.com, Kantai Collection, the maintainers of similarly named software packages, or any third-party platform integrated with the Service.

## What Shoukaku Does

| Area | Highlights |
|---|---|
| Music | Playback, queues, seeking, preferences, favorites, history, autoplay, loop, shuffle, and voice-channel controls |
| Moderation | Warnings, cases, mutes, kicks, bans, automoderation, anti-raid, and server protection |
| Utility | AFK, avatar, role, user, and server information, reporting, and general tools |
| Integrations | Anime, Reddit, Pixiv, Steam, Wikipedia, supported public media downloads and previews, and other approved services |
| Entertainment | Fun and community-oriented commands |

The [complete command reference](COMMANDS.md) lists active, restricted, and disabled command implementations. The official hosted deployment enables `/download` through `DOWNLOAD_COMMAND_ENABLED`. Dedicated adult-content commands (`/nhentai` and `/rule34`) and `/snipe` remain disabled.

## Documentation

| Document | Purpose |
|---|---|
| [Complete Command Reference](COMMANDS.md) | Full inventory of active, restricted, and disabled command implementations |
| [Technology](TECHNOLOGY.md) | High-level tools, services, storage, retention, and architecture used by the project |
| [FAQ](FAQ.md) | Common setup, usage, availability, privacy, repository, and support questions |
| [Privacy Policy](PP.md) | Information the official hosted service processes and how it is handled |
| [Terms of Service](TOS.md) | Rules and conditions for using the official hosted service |
| [Copyright and IP Policy](IP_POLICY.md) | Copyright complaints, takedowns, counter-notices, and repeat infringement |
| [Security Policy](SECURITY.md) | Private vulnerability-reporting process |
| [Contributing](CONTRIBUTING.md) | Rules for documentation contributions |
| [License](LICENSE) | Copyright status and permitted use of this repository |

The English and Vietnamese legal documents are intended to express the same rules. If a language difference or ambiguity affects a user in Vietnam, the interpretation required by applicable law and mandatory consumer or data-subject protections controls.

## Repository Relationship

Shoukaku is split into two publicly viewable repositories with different purposes:

| Repository | Purpose |
|---|---|
| [`alG-N/ShoukakuDocs`](https://github.com/alG-N/ShoukakuDocs) | Public user documentation and the canonical Privacy Policy and Terms of Service |
| [`alG-N/ShoukakuBot`](https://github.com/alG-N/ShoukakuBot) | Backend implementation, tests, deployment assets, and maintainer documentation |

Public visibility does not itself grant an open-source license. Use of code and documentation remains governed by the license or copyright notice in the relevant repository.

Neither repository should contain live credentials, private configuration, production personal data, database exports, private logs, protected dashboard access, or secrets.

## Technology Overview

Shoukaku is built primarily with TypeScript and Node.js. The hosted stack uses Discord.js, PostgreSQL, Redis, Lavalink, Docker, selected media-processing components, and optional observability tools.

See [TECHNOLOGY.md](TECHNOLOGY.md) for a high-level breakdown. It describes relevant technologies and retention behavior without publishing credentials or protected production access details.

## Availability and Changes

Shoukaku is an actively developed service. Commands, integrations, limits, and availability may change as Discord, third-party APIs, laws, and project requirements evolve.

For current active behavior:

1. Use `/help` in Discord.
2. Check the [support server](https://discord.gg/qGwKsqH62k).
3. Check the [status page](https://altergolden.dev).
4. Use [COMMANDS.md](COMMANDS.md) when you also need the complete inventory of disabled implementations.

## Privacy, Safety, and Reports

- Shoukaku does not sell personal data.
- The official service may process Discord identifiers, server configuration, moderation records, command inputs, music preferences, favorites, listening history, temporary media data, media-mapping metadata, security signals, and technical logs as described in the [Privacy Policy](PP.md).
- `/download` is limited to supported public media that the user owns, has permission to use, or may use under applicable law. Local source files default to a maximum age of 1,800 seconds; temporary public R2 objects, when enabled, target a maximum of 86,400 seconds.
- Dedicated adult-content commands and deleted-message collection remain disabled in the official hosted service.
- Copyright complaints should follow [IP_POLICY.md](IP_POLICY.md).
- Security vulnerabilities should follow [SECURITY.md](SECURITY.md).
- Privacy, legal, copyright, and security notices may be sent to **whittylord@gmail.com**.

Do not publish vulnerabilities, tokens, credentials, personal data, copyrighted material, or exploit instructions in public issues.

## Permissions

The official invite link requests Discord's **Administrator** permission. This is broad access: invite Shoukaku only to a server you own or are explicitly authorized to administer, and review the requested access before confirming the installation.

## Documentation Contributions

Corrections and improvements to public documentation are welcome under [CONTRIBUTING.md](CONTRIBUTING.md). Keep submissions limited to information suitable for public release and do not include secrets, private data, or protected infrastructure access details.

## Rights and Trademarks

This repository is provided under the terms in [LICENSE](LICENSE). Third-party names, trademarks, APIs, software, and content remain the property of their respective owners. No affiliation or endorsement is implied.
