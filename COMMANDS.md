# Command Reference

This page provides a public overview of Shoukaku's command surface.

> Use `/help` inside Discord for the most current command names, options, permissions, and availability. Commands may change as the bot is updated.

## Temporarily Disabled Commands

The official hosted service currently does not register the following public commands:

- `/nhentai`
- `/rule34`
- `/download`
- `/snipe`

They are disabled while legal, privacy, copyright, retention, and platform-policy controls are reviewed. Their presence in historical source code or documentation does not mean that they are available in the official hosted service.

## General and Utility

| Command | Purpose |
|---|---|
| `/afk` | Manage AFK status |
| `/avatar` | Display a user's avatar |
| `/display` | Display supported user or profile information |
| `/help` | Open the current in-bot help menu |
| `/invite` | Show the least-privilege bot invite link |
| `/ping` | Check bot responsiveness |
| `/report` | Submit a report through configured server or project channels |
| `/roleinfo` | Display information about a Discord role |
| `/serverinfo` | Display information about the current server |

## Moderation and Server Safety

Moderation commands require the relevant Discord permissions and may be affected by role hierarchy or server configuration.

| Command | Purpose |
|---|---|
| `/automod` | Configure or manage automated moderation |
| `/ban` | Ban a member where permitted |
| `/case` | View a moderation case |
| `/clearwarns` | Clear supported warning records |
| `/delete` | Delete supported messages |
| `/delwarn` | Delete a warning record |
| `/kick` | Kick a member where permitted |
| `/lockdown` | Restrict channel or server activity during an incident |
| `/mute` | Temporarily restrict a member where permitted |
| `/raid` | Access anti-raid or raid-response tools |
| `/setting` | Configure supported server settings |
| `/slowmode` | Configure channel slowmode |
| `/warn` | Create a warning record |
| `/warnings` | View warning records |

Server administrators remain responsible for reviewing moderation actions, configuring permissions, informing members where required, and following Discord rules and applicable law.

## Music

Shoukaku exposes music features through `/music` and its subcommands.

| Subcommand | Purpose |
|---|---|
| `play` | Search for or play a track from an approved source |
| `stop` | Stop playback and end the current session |
| `skip` | Skip the current track |
| `pause` | Pause or resume playback |
| `queue` | View the current queue |
| `nowplaying` | View the current track |
| `volume` | Adjust playback volume |
| `loop` | Configure looping behavior |
| `shuffle` | Shuffle the queue |
| `remove` | Remove a queued track |
| `move` | Move a track within the queue |
| `clear` | Clear the queue |
| `history` | View supported playback history |
| `autoplay` | Configure autoplay behavior |

Music must not be used to access private, paid, age-restricted, region-restricted, or DRM-protected material, or in a way that violates a source's terms or a rights holder's permission.

## Approved External Services

| Command | Purpose |
|---|---|
| `/anime` | Search supported anime information sources |
| `/media` | Retrieve or repair supported public media embeds |
| `/pixiv` | Retrieve supported Pixiv information or media |
| `/reddit` | Retrieve supported Reddit content |
| `/steam` | Retrieve supported Steam information |
| `/wikipedia` | Search Wikipedia content |

External-service commands depend on third-party APIs and may be unavailable, restricted, or removed. Users must not provide account passwords, session cookies, access tokens, or URLs to private, paid, restricted, or DRM-protected content.

## Entertainment

| Command | Purpose |
|---|---|
| `/deathbattle` | Run the supported entertainment interaction |
| `/say` | Send supported bot-formatted text where permitted |

## Owner-only Operations

| Command | Purpose |
|---|---|
| `/botcheck` | View restricted operational diagnostics available to the bot owner |

Owner-only commands and internal diagnostics are not available to normal users.

## Permissions and Errors

A command may fail when:

- the user or Bot lacks a required Discord permission;
- the Bot's role is below the target member's role;
- the feature is disabled in the server or official service;
- a third-party service is unavailable;
- the user is rate-limited;
- the provided URL, query, or content is unsupported or restricted;
- a legal, safety, copyright, or privacy control blocks the request.

For help, use `/help` or visit the official support server:

https://discord.gg/qGwKsqH62k
