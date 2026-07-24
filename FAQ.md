# Frequently Asked Questions

## How do I invite Shoukaku?

Use the official least-privilege invite link:

https://discord.com/oauth2/authorize?client_id=1472185156809920615&permissions=0&integration_type=0&scope=bot+applications.commands

The link requests no preselected Discord permissions. A server administrator should grant only the permissions required for the features they choose to use.

## How do I view the available commands?

Run `/help` in Discord for commands that are active and visible with your current permissions and channel context.

The [complete command reference](COMMANDS.md) also lists restricted and disabled command implementations. A disabled command may still appear in source files, tests, old screenshots, or historical Discord registrations without being usable in the official hosted service.

## Why is a command missing or unavailable?

A feature may be unavailable because:

- it is disabled for legal, privacy, copyright, safety, or platform-policy review;
- the command is restricted to the bot owner, support server, administrators, or specific permissions;
- the command is disabled or restricted in the server;
- the user or Bot lacks a required Discord permission;
- the Bot's role is below the target member's role;
- a music, media, or third-party provider is unavailable;
- the request triggered a cooldown, rate limit, safety rule, or file-size limit;
- the command has changed during development.

The official hosted service currently does not register `/nhentai`, `/rule34`, `/download`, or `/snipe`.

## Why might an old disabled command still appear in Discord?

Discord application commands are removed only after the current backend performs a successful bulk overwrite of the application command registry. Removing an export from source code does not by itself delete a previously deployed command.

If a disabled command still appears, it may be an old registration. It should not execute against the current backend, and the Operator should redeploy the current registry.

## Why is Shoukaku offline?

Shoukaku may be restarting, undergoing maintenance, experiencing a hosting issue, or waiting for a third-party service.

Check:

- Status: https://altergolden.dev
- Support: https://discord.gg/qGwKsqH62k

## Why can Shoukaku not moderate a member?

Discord role hierarchy applies to bots. Shoukaku generally cannot moderate:

- the server owner;
- members whose highest role is equal to or higher than the Bot's highest role;
- members protected by permissions or integration-managed roles.

The user running the command must also have the relevant permission.

## Which music controls are available?

The `/music` command includes playback, queue, pause, stop, skip, volume, loop, shuffle, remove, move, clear, seek, history, and autoplay functions. Exact options are shown through `/help command:music` and in [COMMANDS.md](COMMANDS.md).

## Why did music playback fail?

Common causes include:

- the user or Bot is not in a usable voice channel;
- the Bot lacks Connect or Speak permission;
- the source is unsupported, unavailable, private, paid, subscriber-only, age-restricted, region-restricted, or DRM-protected;
- the Lavalink or source provider is temporarily unavailable;
- the requested URL changed or expired.

Do not submit passwords, cookies, access tokens, or private links. Try a different approved public source and check the support server if the issue continues.

## Does Shoukaku save music information?

The official backend may store user music preferences, favorites, and listening history in PostgreSQL. Favorites are limited to the most recent 200 entries per user and listening history to the most recent 100 entries per user under the current implementation.

Users can clear listening history through the supported music interface. Other access, correction, or deletion requests can be sent through the privacy contact described below. See the [Privacy Policy](PP.md) for retention details.

## Can Shoukaku download media?

The public `/download` command is currently disabled.

The remaining `/media` command can repair supported social embeds, display supported direct image or GIF links, and prepare supported public media previews. It must not be used to access private, paid, restricted, age-restricted, or DRM-protected content.

## How long can media-related information remain?

Different media components have different lifetimes:

- temporary source files default to a maximum age of 1,800 seconds;
- temporary public objects, when enabled, target a maximum of 86,400 seconds;
- stable YouTube media-mapping metadata in Redis defaults to a seven-day renewable TTL and is capped at 30 days from creation under the current configuration.

The longer Redis period applies to metadata and source mapping, not to retaining a downloaded source file for 30 days. See the [Privacy Policy](PP.md).

## Can `/media` display mature content?

Shoukaku does not provide dedicated adult-content commands in the official hosted service. However, some third-party image hosts may contain mature material.

Users and server administrators must not use `/media` to expose minors to adult content, evade channel restrictions, or violate Discord rules. The Operator may block a provider or request when necessary.

## Does Shoukaku store my messages?

Shoukaku does not store every message as a general chat archive. The official service currently has `/snipe` collection disabled. Enabled moderation, automoderation, anti-abuse, and reporting features may process limited message content when required for the requested feature.

See the [Privacy Policy](PP.md) for details.

## How do I request access, correction, or deletion?

Email **whittylord@gmail.com** with:

- your Discord user ID;
- the relevant Discord server ID, when applicable;
- the data or feature involved;
- the request you want completed.

Verification may be required to prevent unauthorized disclosure or deletion. You may also use the support server for initial support, but privacy and legal requests should be completed through email.

## Are NSFW commands available?

No. `/nhentai` and `/rule34` are not registered in the official hosted service. They remain listed in the complete command inventory only to explain historical implementation references.

## Is Shoukaku open source?

Both the public documentation and backend repositories are publicly viewable:

- Documentation: https://github.com/alG-N/ShoukakuDocs
- Backend: https://github.com/alG-N/ShoukakuBot

Public visibility does not by itself make a project open source. The repositories are source-visible and remain governed by their applicable license or copyright notice. Do not assume permission to copy, redistribute, modify, or operate the code beyond what the relevant license expressly allows.

## Can I contribute?

Public documentation corrections and improvements are welcome under [CONTRIBUTING.md](CONTRIBUTING.md). Do not include credentials, production details, private logs, internal dashboard access information, personal data, or secrets in public issues or pull requests.

Backend contributions are subject to the backend repository's maintainer rules and license status.

## How do I report abuse, copyright infringement, or a security issue?

- Abuse and support: https://discord.gg/qGwKsqH62k
- Privacy, legal, copyright, and security notices: **whittylord@gmail.com**
- Copyright procedure: [IP_POLICY.md](IP_POLICY.md)
- Vulnerability procedure: [SECURITY.md](SECURITY.md)

Do not post tokens, personal data, copyrighted material, exploit details, or an active vulnerability in a public issue.
