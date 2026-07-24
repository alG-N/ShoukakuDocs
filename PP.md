# Privacy Policy

**Version:** 2.0  
**Effective date:** July 24, 2026  
**Last updated:** July 24, 2026

This Privacy Policy explains how the official hosted instance of the Shoukaku Discord bot ("Shoukaku", the "Bot", or the "Service") processes personal data.

## 1. Controller and Contact

The Service is operated and controlled by **alterGolden**, an individual software developer based in Vietnam (the "Operator").

Privacy requests and legal notices may be sent to **whittylord@gmail.com**. The support server may help with ordinary support, but email is the primary channel for access, correction, deletion, objection, restriction, and complaint requests.

This policy applies only to the official hosted Service. It does not automatically apply to forks or independently hosted deployments.

## 2. Current Feature Status

The official Service currently does not register `/nhentai`, `/rule34`, `/download`, or `/snipe`.

- No new `/snipe` deleted-message collection should occur while the backend collection flag remains disabled.
- The public `/download` workflow is unavailable.
- Historical source code, tests, database schemas, or documentation references do not mean those features are active.

If a high-risk feature is re-enabled, the Operator must update this policy and implement appropriate controls before public use.

## 3. Data Categories, Purposes, and Retention

| Data category | Examples | Purpose and processing basis | Current retention |
|---|---|---|---|
| Discord identifiers and server context | User, guild, channel, role, message, and interaction IDs; display names; avatars; permissions | Execute requested commands, verify authorization, maintain server configuration, prevent abuse. Necessary to provide the requested Service and for legitimate security/operational interests. | Transient interaction data is kept only for the request or cache lifetime. Durable server configuration remains until an authorized administrator deletes it, a verified deletion request is completed, or it is no longer needed. |
| Moderation records | Warnings, cases, reasons, moderator IDs, action metadata | Provide server-requested moderation history, resolve disputes, prevent abuse. Controlled by authorized server staff and the Operator's legitimate interests. | Retained until deleted by an authorized server administrator or following a verified request, except where a temporary security or legal hold is necessary. Removing the Bot does not automatically erase every durable moderation record. |
| Command inputs and reports | Search terms, public URLs, report text, moderation reasons | Execute the requested feature, provide support, investigate abuse, enforce rules. | Kept for the request unless the feature requires a record. Reports and abuse records remain until resolved and no longer needed for security, dispute, or legal purposes. |
| Music state | Queue entries, requested tracks, playback state, optional history | Provide voice playback and requested queue/history features. | Active queue and playback state are temporary. Optional history remains until cleared, replaced, or removed through maintenance or a verified request. |
| Temporary media data | Public URL, processing job metadata, temporary files, generated public-object key | Provide approved `/media` and embed workflows. | Current source-file cleanup defaults to a maximum age of 1,800 seconds. If temporary public-object delivery is enabled, the configured object lifecycle currently targets no more than 86,400 seconds. Upstream URLs may expire under provider rules. |
| Rate limits and security signals | Cooldowns, request counters, abuse indicators, incident records | Prevent spam, fraud, attacks, and service disruption. | Short-lived counters expire according to cache configuration. Incident records may be retained while reasonably necessary to investigate and prevent repeated abuse. |
| Technical logs and diagnostics | Command name and timestamp, errors, stack traces, health and performance data | Debugging, security, availability, and incident response. | Core container logs use bounded rotating files by size rather than indefinite append-only storage. Optional external observability providers apply the retention configured in their account. Logs may be preserved longer only for an active incident or legal obligation. |
| Web request metadata | Standard request time, route, user agent, and network metadata when visiting official web endpoints | Deliver and secure the website, status, health, or media endpoint. | Retained in bounded operational logs and provider systems according to the controls above. Discord does not provide the Bot with a user's IP address merely because the user runs a Discord command. |

The Service does not sell personal data and does not use Discord API data for third-party behavioral advertising.

## 4. Message Content

Shoukaku does not operate as a general archive of all server messages.

Message content may be processed when required for an enabled moderation, automoderation, anti-abuse, reporting, or user-requested feature. The `/snipe` collection path is disabled by default in the official backend and is not registered as a public command.

Server administrators are responsible for enabling and configuring server-controlled moderation features lawfully and for limiting staff access.

## 5. Data Sources

Data may come from:

- Discord and the Discord user or server administrator;
- content and URLs intentionally submitted through commands;
- enabled third-party APIs requested by the user;
- the Operator's infrastructure, security controls, and support channels.

The Bot does not receive a Discord user's password. Users must not submit passwords, cookies, tokens, payment-card information, or private account credentials.

## 6. Service Providers and International Processing

Depending on enabled features, data may be processed by:

- **Discord**, for interactions, messages, permissions, and voice connectivity;
- **hosting and network providers**, including Cloudflare where configured;
- **Sentry or similar observability providers**, when enabled;
- **approved source providers**, such as Reddit, Pixiv, Steam, Wikipedia, anime information providers, and supported media/audio providers;
- infrastructure controlled by the Operator, including PostgreSQL, Redis, Lavalink, and media-processing services.

The Operator is based in Vietnam. Discord, Cloudflare, Sentry, and third-party providers may process data in the United States and other countries where they operate. Their own terms and privacy policies govern their independent processing.

The Operator should assess and document cross-border transfers and service-provider arrangements required by applicable law.

## 7. Sharing and Disclosure

Personal data may be shared only when necessary to:

- provide a user-requested feature through an approved provider;
- investigate abuse, security incidents, or Terms violations;
- protect users, the Service, the Operator, or the public;
- comply with a valid legal obligation or lawful request;
- transfer operation of the Service as part of a lawful reorganization with appropriate protections.

Discord API data is not sold. Service providers must receive only the data reasonably necessary for their task.

## 8. Your Rights and Choices

Subject to applicable law, you may request to:

- know whether and how your personal data is processed;
- access a copy of associated data;
- correct inaccurate data;
- delete data;
- restrict or object to processing;
- withdraw consent where processing relies on consent;
- complain to a competent authority;
- receive an explanation of a Service-level restriction affecting you.

Email **whittylord@gmail.com** with your Discord user ID, relevant server ID, the feature involved, and the request. Verification may be required to prevent unauthorized disclosure or deletion.

Some data may be retained temporarily where necessary for security, legal compliance, fraud prevention, dispute resolution, or the rights of others. The Operator will explain an applicable exception when reasonably possible.

Server-controlled moderation records may also require action by the relevant server administrator.

## 9. Deletion and Bot Removal

An authorized administrator may remove the Bot from a server at any time. Removal stops new server interactions and clears supported transient caches, but it may not immediately erase durable moderation records, backups, provider logs, or incident records.

A verified deletion request is the appropriate process for durable records that cannot be removed through an available server command.

## 10. Security

The Service uses access controls, secret management, network separation, least-privilege service accounts, bounded logging, and operational monitoring.

Production environments processing Discord API data must use encryption at rest and appropriate transport security. If a deployment does not meet that requirement, it must not be treated as an approved production environment.

No online service can guarantee absolute security. Security incidents will be investigated and affected users and Discord will be notified where required by law or platform terms.

See [SECURITY.md](SECURITY.md) for vulnerability reporting.

## 11. Children

The Service is not directed to children below Discord's minimum age or a higher minimum age required by local law. The official Service does not register adult-content commands.

If the Operator learns that data was collected from a person below the applicable minimum age without a lawful basis, the Operator will take appropriate steps to delete or restrict it.

## 12. Policy Changes

The current version and effective date will be published in this repository. Material changes will be announced through an appropriate project channel where reasonably practical.

A feature that materially changes data processing must not be publicly enabled before the policy is updated.

## 13. Contact and Complaints

- Privacy, legal, copyright, and security notices: **whittylord@gmail.com**
- Support server: https://discord.gg/qGwKsqH62k
- Terms: [TOS.md](TOS.md)
- Copyright procedure: [IP_POLICY.md](IP_POLICY.md)
- Security procedure: [SECURITY.md](SECURITY.md)

Canonical public policy:

https://github.com/alG-N/ShoukakuDocs/blob/main/PP.md
