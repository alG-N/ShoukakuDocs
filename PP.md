# Privacy Policy

**Version:** 2.1  
**Effective date:** July 24, 2026  
**Last updated:** July 24, 2026

**Vietnamese version:** [PP_VI.md](PP_VI.md)

This Privacy Policy explains how the official hosted instance of the Shoukaku Discord bot ("Shoukaku", the "Bot", or the "Service") processes personal data.

## Language and scope

The English and Vietnamese versions are intended to express the same privacy practices. For users in Vietnam, the Vietnamese version is provided for accessibility and compliance purposes. If the versions differ, the interpretation required by applicable law controls and any mandatory protection for the data subject or consumer remains unaffected.

This policy applies only to the official hosted Service. It does not automatically apply to forks or independently hosted deployments.

## 1. Controller and Contact

The Service is operated and controlled by an individual software developer residing in Vietnam under the public project name **alterGolden** (the "Operator"). The Operator determines the purposes and means of processing for the official Service and acts as the personal-data controller where that classification applies.

Privacy requests and legal notices may be sent to **whittylord@gmail.com**. The support server may help with ordinary support, but email is the primary channel for access, correction, deletion, objection, restriction, withdrawal, and complaint requests.

The Operator's verified legal identity may be provided where required by applicable law or a valid legal process. This policy does not publish a residential address.

## 2. Current Feature Status

The official Service currently does not register `/nhentai`, `/rule34`, `/download`, or `/snipe`.

- No new `/snipe` deleted-message collection should occur while the backend collection flag remains disabled.
- The public `/download` workflow is unavailable.
- Historical source code, tests, database schemas, or documentation references do not mean those features are active.

If a high-risk feature is re-enabled, the Operator must update this policy and implement appropriate controls before public use.

## 3. Processing Principles and Legal Grounds

The Service is intended to process personal data lawfully, transparently, for stated purposes, and only to the extent reasonably necessary for those purposes.

Depending on the activity and applicable law, processing may be based on:

- the user's or server administrator's request to provide a feature or perform an agreed service;
- the data subject's valid consent where consent is required;
- compliance with a legal obligation or valid lawful request;
- protection of users, systems, or legal rights against fraud, abuse, attacks, or unlawful conduct where permitted by law;
- another specific ground expressly permitted by applicable law.

Consent is not treated as valid merely because a user failed to opt out. Where consent is required, it must be informed and capable of being withdrawn. Withdrawal does not retroactively invalidate lawful processing completed before withdrawal, but affected optional processing must stop as required by law.

A feature that requires consent, a formal assessment, or another compliance control must remain disabled until the required control exists.

## 4. Data Categories, Purposes, and Retention

| Data category | Examples | Purpose and applicable ground | Current retention or deletion trigger |
|---|---|---|---|
| Discord identifiers and server context | User, guild, channel, role, message, and interaction IDs; display names; avatars; permissions | Execute requested commands, verify authorization, maintain server configuration, and prevent abuse. Based on the requested Service, consent where required, and permitted security or legal grounds. | Transient interaction data is kept only for the request or cache lifetime. Durable server configuration remains until an authorized administrator deletes it, a verified deletion request is completed, or the configuration is no longer needed. |
| Moderation records | Warnings, cases, reasons, moderator IDs, action metadata | Provide server-requested moderation history, review actions, resolve disputes, and prevent abuse. Based on administrator instructions, the requested Service, and permitted security or legal grounds. | Retained until deleted by an authorized server administrator or following a verified request, except where a temporary security, dispute, or legal hold is necessary. Removing the Bot does not automatically erase every durable moderation record. |
| Command inputs and reports | Search terms, public URLs, report text, moderation reasons | Execute the requested feature, provide support, investigate abuse, and enforce rules. | Kept for the request unless the feature requires a record. Reports and abuse records remain until resolved and no longer necessary for security, dispute, or legal purposes. |
| Music state | Queue entries, requested tracks, playback state, optional history | Provide voice playback and requested queue or history features. | Active queue and playback state are temporary. Optional history remains until cleared, replaced, disabled, or removed through maintenance or a verified request. |
| Temporary media data | Public URL, processing job metadata, temporary files, generated public-object key | Provide approved `/media` and embed workflows at the user's request. | Current source-file cleanup defaults to a maximum age of 1,800 seconds. If temporary public-object delivery is enabled, the configured object lifecycle currently targets no more than 86,400 seconds. Upstream URLs may expire under provider rules. |
| Rate limits and security signals | Cooldowns, request counters, abuse indicators, incident records | Prevent spam, fraud, attacks, and service disruption under permitted security and legal grounds. | Short-lived counters expire according to cache configuration. Incident records may be retained only while reasonably necessary to investigate and prevent repeated abuse or meet a legal obligation. |
| Technical logs and diagnostics | Command name and timestamp, errors, stack traces, health and performance data | Debugging, security, availability, and incident response. | Core container logs use bounded rotating files by size rather than indefinite append-only storage. Optional external observability providers apply the retention configured in their account. Logs may be preserved longer only for an active incident or legal obligation. |
| Web request metadata | Standard request time, route, user agent, and network metadata when visiting official web endpoints | Deliver and secure the website, status, health, or media endpoint. | Retained in bounded operational logs and provider systems according to the controls above. Discord does not provide the Bot with a user's IP address merely because the user runs a Discord command. |

The Service does not sell personal data and does not use Discord API data for third-party behavioral advertising.

Some durable records do not yet have a universal automated time-based deletion job. Where no fixed automated deadline is stated, the listed purpose and deletion trigger apply, and verified deletion requests are handled manually unless retention is temporarily required by law, security, or dispute needs.

## 5. Message Content

Shoukaku does not operate as a general archive of all server messages.

Message content may be processed when required for an enabled moderation, automoderation, anti-abuse, reporting, or user-requested feature. The `/snipe` collection path is disabled by default in the official backend and is not registered as a public command.

Server administrators are responsible for enabling and configuring server-controlled moderation features lawfully, informing members where required, and limiting staff access.

## 6. Data Sources

Data may come from:

- Discord and the Discord user or server administrator;
- content and URLs intentionally submitted through commands;
- enabled third-party APIs requested by the user;
- the Operator's infrastructure, security controls, and support channels.

The Bot does not receive a Discord user's password. Users must not submit passwords, cookies, tokens, payment-card information, or private account credentials.

## 7. Service Providers and International Processing

Depending on enabled features, data may be processed by:

- **Discord**, for interactions, messages, permissions, and voice connectivity;
- **hosting and network providers**, including Cloudflare where configured;
- **Sentry or similar observability providers**, when enabled;
- **approved source providers**, such as Reddit, Pixiv, Steam, Wikipedia, anime information providers, and supported media or audio providers;
- infrastructure controlled by the Operator, including PostgreSQL, Redis, Lavalink, and media-processing services.

The Operator is based in Vietnam. Discord, Cloudflare, Sentry, GitHub, hosting providers, and third-party APIs may process data in the United States or other countries where they operate.

Before enabling or continuing processing that transfers personal data across national borders, the Operator is responsible for determining which notices, consents, contracts, assessments, records, safeguards, and regulatory procedures are required by applicable law. Processing that cannot meet a required safeguard must be disabled or redesigned. This policy does not claim that merely naming a foreign provider completes those obligations.

Each independent provider's own terms and privacy policy govern processing for which that provider independently determines the purposes and means.

## 8. Sharing and Disclosure

Personal data may be shared only when necessary to:

- provide a user-requested feature through an approved provider;
- investigate abuse, security incidents, or Terms violations;
- protect users, the Service, the Operator, or the public where permitted by law;
- comply with a valid legal obligation or lawful request;
- transfer operation of the Service as part of a lawful reorganization with required notice, consent, and safeguards.

Discord API data is not sold. Service providers must receive only the data reasonably necessary for their task.

## 9. Your Rights and Choices

Subject to applicable law, you may request to:

- know whether and how your personal data is processed;
- access a copy of associated data;
- correct inaccurate data;
- delete data;
- restrict or object to processing;
- give, refuse, or withdraw consent where processing relies on consent;
- complain to a competent authority;
- receive an explanation of a Service-level restriction affecting you.

Email **whittylord@gmail.com** with your Discord user ID, relevant server ID, the feature involved, and the request. Verification may be required to prevent unauthorized disclosure or deletion. Do not send passwords, tokens, or identity documents unless the Operator specifically explains a secure and lawful verification method.

Requests will be handled without unreasonable delay and within any mandatory period required by applicable law. If a request is refused or limited, the Operator will explain the applicable reason where legally permitted.

Some data may be retained temporarily where necessary for security, legal compliance, fraud prevention, dispute resolution, or the rights of others. Server-controlled moderation records may also require action by the relevant server administrator.

## 10. Deletion and Bot Removal

An authorized administrator may remove the Bot from a server at any time. Removal stops new server interactions and clears supported transient caches, but it may not immediately erase durable moderation records, backups, provider logs, or incident records.

A verified deletion request is the appropriate process for durable records that cannot be removed through an available server command. Backups and provider logs may remain until their normal secure rotation or deletion cycle, unless earlier deletion is technically and legally required.

## 11. Security

The Service uses access controls, secret management, network separation, least-privilege service accounts, bounded logging, and operational monitoring.

Production environments processing Discord API data must use appropriate transport security and encryption at rest where required by Discord rules or applicable law. A deployment that does not meet a mandatory requirement must not be treated as an approved production environment.

No online service can guarantee absolute security. Security incidents will be investigated, contained, documented, and notified to affected persons, Discord, or competent authorities where required by law or platform terms.

See [SECURITY.md](SECURITY.md) for vulnerability reporting.

## 12. Children

The Service is not directed to children below Discord's minimum age or a higher minimum age required by local law. The official Service does not register adult-content commands.

If the Operator learns that personal data was collected from a person below the applicable minimum age without a lawful basis, the Operator will take appropriate steps to delete or restrict it.

## 13. Vietnam Legal Context

For processing subject to Vietnamese law, relevant requirements may include the Law on Personal Data Protection No. 91/2025/QH15 and Decree No. 356/2025/ND-CP, both effective January 1, 2026. Where the Service is supplied in a consumer transaction, mandatory protections under Vietnam's Law on Protection of Consumers' Rights and its implementing rules may also apply.

Official references:

- https://vanban.chinhphu.vn/?classid=1&docid=214590&pageid=27160&typegroupid=3
- https://vanban.chinhphu.vn/?docid=216387&pageid=27160

These references are provided for transparency and are not legal advice. Operational compliance, assessments, records, and any required filings must be separately verified.

## 14. Policy Changes

The current version and effective date will be published in this repository. Material changes will be announced through an appropriate project channel where reasonably practical.

A feature that materially changes data processing must not be publicly enabled before the policy and required controls are updated. Continued use does not replace consent where fresh consent is legally required.

## 15. Contact and Complaints

- Privacy, legal, copyright, and security notices: **whittylord@gmail.com**
- Support server: https://discord.gg/qGwKsqH62k
- Terms: [TOS.md](TOS.md)
- Vietnamese Privacy Policy: [PP_VI.md](PP_VI.md)
- Copyright procedure: [IP_POLICY.md](IP_POLICY.md)
- Security procedure: [SECURITY.md](SECURITY.md)

Canonical public policy:

https://github.com/alG-N/ShoukakuDocs/blob/main/PP.md
