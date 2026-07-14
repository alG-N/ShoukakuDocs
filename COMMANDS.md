# Command Reference

This page provides a public overview of Shoukaku's command surface.

> Use `/help` inside Discord for the most current command names, options, permissions, and availability. Commands may change as the bot is updated.

## General and Utility

| Command | Purpose |
|---|---|
| `/afk` | Manage AFK status |
| `/avatar` | Display a user's avatar |
| `/display` | Display supported user or profile information |
| `/help` | Open the current in-bot help menu |
| `/invite` | Show the bot invite link |
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
| `/snipe` | Display supported recently deleted-message information |
| `/warn` | Create a warning record |
| `/warnings` | View warning records |

Server administrators remain responsible for reviewing moderation actions, configuring permissions, and following Discord rules and applicable law.

## Music

Shoukaku exposes music features through `/music` and its subcommands.

| Subcommand | Purpose |
|---|---|
| `play` | Search for or play a track |
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

Music availability depends on voice permissions, Lavalink availability, and supported media sources.

## Media and External Services

| Command | Purpose |
|---|---|
| `/anime` | Search supported anime information sources |
| `/media` | Retrieve or repair supported media and embeds |
| `/nhentai` | Access age-restricted content where permitted |
| `/pixiv` | Retrieve supported Pixiv information or media |
| `/reddit` | Retrieve supported Reddit content |
| `/rule34` | Access age-restricted content where permitted |
| `/steam` | Retrieve supported Steam information |
| `/wikipedia` | Search Wikipedia content |
| `/download` | Process supported media URLs for lawful downloading or delivery |

External-service commands depend on third-party APIs and may be temporarily unavailable or limited.

### Age-restricted commands

Age-restricted commands must only be used:

- by users who meet applicable age requirements;
- in appropriately marked Discord channels;
- in compliance with Discord policy and local law.

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
- the feature is disabled in the server;
- a third-party service is unavailable;
- the user is rate-limited;
- the provided URL, query, or content is unsupported;
- the command is restricted to an NSFW channel or a project owner.

For help, use `/help` or visit the official support server:

https://discord.gg/qGwKsqH62k
