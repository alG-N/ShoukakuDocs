# Frequently Asked Questions

## How do I invite Shoukaku?

Use the official invite link:

https://discord.com/oauth2/authorize?client_id=1472185156809920615&permissions=8&integration_type=0&scope=bot

You must have permission to add applications to the target Discord server.

## How do I view the available commands?

Run `/help` in Discord. The in-bot help command is the most current source because features may change between documentation updates.

A public overview is also available in [COMMANDS.md](COMMANDS.md).

## Why is a command missing or unavailable?

A feature may be unavailable because:

- the command is disabled or restricted in the server;
- the user or Bot lacks a required Discord permission;
- the Bot's role is below the target member's role;
- the command requires an NSFW channel;
- a music, media, or third-party provider is unavailable;
- the request triggered a cooldown, rate limit, safety rule, or file-size limit;
- the command has changed during development.

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

## Why did music playback fail?

Common causes include:

- the user or Bot is not in a usable voice channel;
- the Bot lacks Connect or Speak permission;
- the source is unsupported, unavailable, private, age-restricted, or region-restricted;
- the Lavalink or source provider is temporarily unavailable;
- the requested URL changed or expired.

Try a different search query or source and check the support server if the issue continues.

## Why did a media download fail?

Media processing depends on the source platform and third-party tools. A download may fail because the URL is unsupported, private, expired, protected, too large, restricted, or temporarily unavailable.

Users are responsible for ensuring that downloading and using content is lawful and permitted by the relevant platform and rights holder.

## Does Shoukaku store my messages?

Shoukaku does not store every message as a general chat archive. Some features may process message content or temporarily store limited message information when required for automoderation, anti-abuse, moderation, snipe, reporting, or media functionality.

See the [Privacy Policy](PP.md) for more detail.

## How do I request deletion of data?

Contact the project owner through the official support server and provide:

- your Discord user ID;
- the relevant Discord server ID, when applicable;
- a clear description of the data or feature involved.

Verification may be required. Some records may need to be retained for security, abuse prevention, legal compliance, or protection of other users.

Support: https://discord.gg/qGwKsqH62k

## Are NSFW commands allowed everywhere?

No. Age-restricted commands must only be used by legally eligible users in appropriately configured Discord channels and in compliance with Discord policy and local law.

Server administrators are responsible for channel configuration and community rules.

## Is Shoukaku open source?

The public documentation is maintained in this repository. The backend implementation and operational material are maintained separately for the project owner, maintainers, and approved collaborators.

Repository relationship:

- Public docs: https://github.com/alG-N/ShoukakuDocs
- Backend: https://github.com/alG-N/ShoukakuBot

## Can I contribute?

Public documentation corrections and improvements are welcome. Do not include credentials, production details, private logs, internal dashboard access information, or secrets in public issues or pull requests.

## How do I report abuse or a security issue?

Use the official support server:

https://discord.gg/qGwKsqH62k

Do not post tokens, personal data, exploit details, or an active vulnerability in a public issue.
