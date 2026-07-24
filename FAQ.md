# Frequently Asked Questions

## How do I invite Shoukaku?

Use the official least-privilege invite link:

https://discord.com/oauth2/authorize?client_id=1472185156809920615&permissions=0&integration_type=0&scope=bot+applications.commands

The link requests no preselected Discord permissions. A server administrator should grant only the permissions required for the features they choose to use.

## How do I view the available commands?

Run `/help` in Discord. The in-bot help command is the most current source because features may change between documentation updates.

A public overview is also available in [COMMANDS.md](COMMANDS.md).

## Why is a command missing or unavailable?

A feature may be unavailable because:

- it is disabled for legal, privacy, copyright, safety, or platform-policy review;
- the command is disabled or restricted in the server;
- the user or Bot lacks a required Discord permission;
- the Bot's role is below the target member's role;
- a music, media, or third-party provider is unavailable;
- the request triggered a cooldown, rate limit, safety rule, or file-size limit;
- the command has changed during development.

The official hosted service currently does not register `/nhentai`, `/rule34`, `/download`, or `/snipe`.

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
- the source is unsupported, unavailable, private, paid, age-restricted, region-restricted, or DRM-protected;
- the Lavalink or source provider is temporarily unavailable;
- the requested URL changed or expired.

Do not submit passwords, cookies, access tokens, or private links. Try a different approved public source and check the support server if the issue continues.

## Can Shoukaku download media?

The public `/download` command is currently disabled. The remaining `/media` command is limited to supported public media and embed assistance. It must not be used to access private, paid, restricted, or DRM-protected content.

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

No. `/nhentai` and `/rule34` are not registered in the official hosted service. Their historical source code must not be treated as an available feature.

## Is Shoukaku open source?

The public documentation is maintained in this repository. The backend implementation and operational material are maintained separately for the operator, maintainers, and approved collaborators.

Repository relationship:

- Public docs: https://github.com/alG-N/ShoukakuDocs
- Backend: https://github.com/alG-N/ShoukakuBot

The public documentation repository is not offered under an open-source license. See [LICENSE](LICENSE).

## Can I contribute?

Public documentation corrections and improvements are welcome under [CONTRIBUTING.md](CONTRIBUTING.md). Do not include credentials, production details, private logs, internal dashboard access information, personal data, or secrets in public issues or pull requests.

## How do I report abuse, copyright infringement, or a security issue?

- Abuse and support: https://discord.gg/qGwKsqH62k
- Privacy, legal, copyright, and security notices: **whittylord@gmail.com**
- Copyright procedure: [IP_POLICY.md](IP_POLICY.md)
- Vulnerability procedure: [SECURITY.md](SECURITY.md)

Do not post tokens, personal data, copyrighted material, exploit details, or an active vulnerability in a public issue.
