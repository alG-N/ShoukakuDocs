# Command Reference

This page provides a public inventory of Shoukaku's user-facing command surface, including commands that are currently active, restricted, or disabled.

> Use `/help` inside Discord for the most current active command names, options, permissions, and availability. This document also records disabled commands so that historical source files, screenshots, or old command registrations can be understood correctly.

## Status meanings

| Status | Meaning |
|---|---|
| **Active** | Registered by the current backend and intended for normal use, subject to permissions and configuration |
| **Restricted** | Registered, but limited to the bot owner, support server, administrators, specific channels, or other access rules |
| **Disabled** | Retained only as historical or implementation code and not registered by the official hosted service |

## General and Utility

| Command | Purpose | Status |
|---|---|---|
| `/afk` | Manage AFK status | Active |
| `/avatar` | Display a user's avatar | Active |
| `/display` | Display supported user or profile information | Active |
| `/help` | Browse the current in-bot command registry and exact usage | Active |
| `/invite` | Show the official bot invite link, which requests Administrator permission | Active |
| `/ping` | Check bot responsiveness | Active |
| `/report` | Submit a report through configured server or project channels | Active |
| `/roleinfo` | Display information about a Discord role | Active |
| `/serverinfo` | Display information about the current server | Active |

## Moderation and Server Safety

Moderation commands require the relevant Discord permissions and may be affected by role hierarchy or server configuration.

| Command | Purpose | Status |
|---|---|---|
| `/automod` | Configure or manage automated moderation | Restricted |
| `/ban` | Ban a member where permitted | Restricted |
| `/case` | View a moderation case | Restricted |
| `/clearwarns` | Clear supported warning records | Restricted |
| `/delete` | Delete supported messages | Restricted |
| `/delwarn` | Delete a warning record | Restricted |
| `/kick` | Kick a member where permitted | Restricted |
| `/lockdown` | Restrict channel or server activity during an incident | Restricted |
| `/mute` | Temporarily restrict a member where permitted | Restricted |
| `/raid` | Access anti-raid or raid-response tools | Restricted |
| `/setting` | Configure supported server settings | Restricted |
| `/slowmode` | Configure channel slowmode | Restricted |
| `/warn` | Create a warning record | Restricted |
| `/warnings` | View warning records | Restricted |

Server administrators remain responsible for reviewing moderation actions, configuring permissions, informing members where required, and following Discord rules and applicable law.

## Music

Shoukaku exposes music features through `/music` and its subcommands.

| Subcommand | Purpose | Status |
|---|---|---|
| `play` | Search for or play a song or playlist from an approved source | Active |
| `stop` | Stop playback and clear the current queue | Active |
| `skip` | Skip the current track | Active |
| `pause` | Pause or resume playback | Active |
| `queue` | View the current queue | Active |
| `nowplaying` | View the current track | Active |
| `volume` | Adjust playback volume | Active |
| `loop` | Configure track or queue looping | Active |
| `shuffle` | Toggle queue shuffle | Active |
| `remove` | Remove a queued track | Active |
| `move` | Move a track within the queue | Active |
| `clear` | Clear queued tracks while keeping the current track | Active |
| `seek` | Seek to a position in the current track | Active |
| `history` | View supported listening history | Active |
| `autoplay` | Configure autoplay behavior | Active |

Music must not be used to access private, paid, subscriber-only, age-restricted, region-restricted, or DRM-protected material, or in a way that violates a source's terms or a rights holder's permission.

## Approved External Services

| Command | Purpose | Status |
|---|---|---|
| `/anime` | Search supported anime information sources | Active |
| `/download` | Prepare and deliver a preview of supported public media | Active |
| `/media` | Repair supported social embeds, display supported direct images or GIFs, and prepare supported public media previews | Active |
| `/pixiv` | Retrieve supported Pixiv information or media | Active |
| `/reddit` | Retrieve supported Reddit content | Active |
| `/steam` | Retrieve supported Steam information | Active |
| `/wikipedia` | Search Wikipedia content | Active |

External-service commands depend on third-party APIs and may be unavailable, restricted, or removed. The official hosted deployment enables `/download` through `DOWNLOAD_COMMAND_ENABLED`. Users may submit only supported public media they own, have permission to use, or may use under applicable law. They must not provide account passwords, session cookies, access tokens, or URLs to private, paid, restricted, or DRM-protected content.

Downloaded source files used for processing default to a maximum local age of 1,800 seconds. Temporary public R2 objects, when enabled, target a maximum of 86,400 seconds.

Some third-party image hosts can contain mature material even though Shoukaku does not provide dedicated adult-content commands. Users and server administrators must not use `/media` to expose minors to adult content, evade channel restrictions, or violate Discord rules. The Operator may block a host or request without notice where necessary for safety, law, platform policy, or copyright compliance.

## Entertainment

| Command | Purpose | Status |
|---|---|---|
| `/deathbattle` | Run the supported entertainment interaction | Active |
| `/say` | Send supported bot-formatted text where permitted | Active |

## Owner-only Operations

| Command | Purpose | Status |
|---|---|---|
| `/botcheck` | View restricted operational diagnostics available to the bot owner | Restricted |

Owner-only commands are deployed separately to the configured support server and are not available to normal users.

## Disabled Command Implementations

The following commands are included in this complete inventory because implementation files, tests, database structures, or old screenshots may still refer to them. They are not exported by the current command registry and are not intended to be available in the official hosted service.

| Command | Historical purpose | Status |
|---|---|---|
| `/snipe` | Display recently deleted messages collected for a server | Disabled |
| `/nhentai` | Search or retrieve adult-oriented doujin content | Disabled |
| `/rule34` | Search or retrieve adult-oriented image content | Disabled |

Keeping implementation code in the repository does not activate a command. Previously deployed Discord commands disappear only after the official application command registry is successfully overwritten by a current deployment.

## Permissions and Errors

A command may fail when:

- the user or Bot lacks a required Discord permission;
- the Bot's role is below the target member's role;
- the feature is disabled in the server or official service;
- a third-party service is unavailable;
- the user is rate-limited;
- the provided URL, query, or content is unsupported or restricted;
- a legal, safety, copyright, privacy, or platform control blocks the request.

For help, use `/help` or visit the official support server:

https://discord.gg/qGwKsqH62k
