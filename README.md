# Shoukaku Bot

Shoukaku is a multi-purpose Discord bot focused on music, moderation, utility commands, and selected third-party integrations.

> **This repository is the public documentation hub for Shoukaku.**
> The application source code, deployment configuration, credentials, and internal infrastructure are maintained separately.

## Quick Links

- [Invite Shoukaku](https://discord.com/oauth2/authorize?client_id=1472185156809920615&permissions=0&integration_type=0&scope=bot+applications.commands)
- [Support Server](https://discord.gg/qGwKsqH62k)
- [Service Status](https://altergolden.dev)
- [Command Reference](COMMANDS.md)
- [Privacy Policy — English](PP.md)
- [Chính sách Quyền riêng tư — Tiếng Việt](PP_VI.md)
- [Terms of Service — English](TOS.md)
- [Điều khoản Dịch vụ — Tiếng Việt](TOS_VI.md)
- [Copyright and IP Policy](IP_POLICY.md)
- [Security Policy](SECURITY.md)
- [FAQ](FAQ.md)

## Project Background

Shoukaku is an independent personal software project created to apply the operator's experience with TypeScript, Discord applications, distributed services, moderation systems, and media infrastructure.

The name is used as a historical reference. Shoukaku is not affiliated with, endorsed by, or sponsored by Discord, C2 Praparat, Kadokawa, DMM.com, Kantai Collection, the maintainers of similarly named software packages, or any third-party platform integrated with the Service.

## What Shoukaku Does

| Area | Highlights |
|---|---|
| Music | Playback, queues, history, autoplay, loop, shuffle, and voice-channel controls |
| Moderation | Warnings, cases, mutes, kicks, bans, automoderation, anti-raid, and server protection |
| Utility | AFK, avatar, role, user, and server information, reporting, and general tools |
| Integrations | Anime, Reddit, Pixiv, Steam, Wikipedia, and other approved services |
| Entertainment | Fun and community-oriented commands |

The public `/download`, `/nhentai`, `/rule34`, and `/snipe` commands are disabled while legal, privacy, and platform-policy controls are reviewed. Use `/help` in Discord for the current command list.

## Documentation

| Document | Purpose |
|---|---|
| [Command Reference](COMMANDS.md) | Public command categories and currently documented commands |
| [Technology](TECHNOLOGY.md) | High-level tools, services, and architecture used by the project |
| [FAQ](FAQ.md) | Common setup, usage, availability, privacy, and support questions |
| [Privacy Policy — English](PP.md) | Information the official hosted service processes and how it is handled |
| [Chính sách Quyền riêng tư — Tiếng Việt](PP_VI.md) | Bản tiếng Việt về dữ liệu được xử lý, mục đích, thời gian lưu và quyền của người dùng |
| [Terms of Service — English](TOS.md) | Rules and conditions for using the official hosted service |
| [Điều khoản Dịch vụ — Tiếng Việt](TOS_VI.md) | Bản tiếng Việt về quy tắc và điều kiện sử dụng Dịch vụ chính thức |
| [Copyright and IP Policy](IP_POLICY.md) | Copyright complaints, takedowns, counter-notices, and repeat infringement |
| [Security Policy](SECURITY.md) | Private vulnerability-reporting process |
| [Contributing](CONTRIBUTING.md) | Rules for documentation contributions |
| [License](LICENSE) | Copyright status and permitted use of this repository |

The English and Vietnamese legal documents are intended to express the same rules. If a language difference or ambiguity affects a user in Vietnam, the interpretation required by applicable law and mandatory consumer or data-subject protections controls.

## Repository Relationship

Shoukaku is split into two repositories with different audiences:

| Repository | Visibility and purpose |
|---|---|
| [`alG-N/ShoukakuDocs`](https://github.com/alG-N/ShoukakuDocs) | Public, user-facing documentation and the canonical Privacy Policy and Terms of Service |
| [`alG-N/ShoukakuBot`](https://github.com/alG-N/ShoukakuBot) | Backend implementation and operational documentation intended for maintainers and approved collaborators |

The public documentation must not contain credentials, private configuration, internal monitoring access details, or secrets from the backend repository.

## Technology Overview

Shoukaku is built primarily with TypeScript and Node.js. The hosted stack uses Discord.js, PostgreSQL, Redis, Lavalink, Docker, selected media-processing components, and optional observability tools.

See [TECHNOLOGY.md](TECHNOLOGY.md) for a high-level breakdown. That document intentionally describes technologies without publishing sensitive deployment details.

## Availability and Changes

Shoukaku is an actively developed service. Commands, integrations, limits, and availability may change as Discord, third-party APIs, laws, and project requirements evolve.

For the most current behavior:

1. Use `/help` in Discord.
2. Check the [support server](https://discord.gg/qGwKsqH62k).
3. Check the [status page](https://altergolden.dev).

## Privacy, Safety, and Reports

- Shoukaku does not sell personal data.
- The official service processes limited Discord identifiers, command inputs, moderation records, temporary service data, and technical logs as described in the [Privacy Policy](PP.md) and [Chính sách Quyền riêng tư](PP_VI.md).
- Risky public features are disabled unless and until the backend and documentation provide adequate controls.
- Copyright complaints should follow [IP_POLICY.md](IP_POLICY.md).
- Security vulnerabilities should follow [SECURITY.md](SECURITY.md).
- Privacy, legal, copyright, and security notices may be sent to **whittylord@gmail.com**.

Do not publish vulnerabilities, tokens, credentials, personal data, copyrighted material, or exploit instructions in public issues.

## Permissions

The official invite link requests no preselected Discord permissions. A server administrator should grant only the permissions required for the features they enable. Administrator permission is not required as a default installation permission.

## Documentation Contributions

Corrections and improvements to public documentation are welcome under [CONTRIBUTING.md](CONTRIBUTING.md). Keep submissions limited to public information and do not copy secrets or private infrastructure details from the backend repository.

## Rights and Trademarks

This repository is provided under the terms in [LICENSE](LICENSE). Third-party names, trademarks, APIs, software, and content remain the property of their respective owners. No affiliation or endorsement is implied.
