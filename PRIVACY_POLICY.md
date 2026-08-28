# Privacy Policy — Deployer Bot

_Last updated: 2026-08-28_

Deployer Bot ("the bot") is a self-hosted, community-specific Discord bot built for a single Discord server. It is not a public/multi-server product, and it does not sell, share, or monetize any data it collects.

## What data the bot collects

The bot only processes data it receives through Discord's API as part of normal server activity, and only from the server it is installed in:

- **Discord user ID and username/tag** — attached to moderation records and archived submissions so actions can be attributed correctly.
- **Server role membership** — read to determine whether a member holds a moderator role or the muted role.
- **Message content** — read from messages sent in designated suggestion/bug-report channels, from direct messages sent to the bot, and from any message in the server (to detect commands such as `!!tagname` or `!suggested`).
- **Server nicknames** — read to detect and block a small set of reserved values that could be used to impersonate bot output.

The bot does not read or store voice data, presence/status data, or data from channels other than where it operates.

## How the data is used

- **Suggestion/bug-report archive** — when a member posts in a designated channel and tags it as a suggestion or bug report, the message text, author tag, and a link to the original message are saved to a local file so staff can review it. This entry is removed automatically when the message is deleted on Discord, or when an authorized moderator (or the original author) reacts to remove it.
- **Mute persistence** — if a member is given the server's mute role and later leaves the server, their user ID and username are kept in a local list so the mute role can be automatically re-applied if they rejoin, preventing moderation evasion. The entry is removed once the member is un-muted.
- **Reaction-based role self-assignment** — used only at the moment a reaction is added, to add the corresponding role. Nothing is stored.
- **DM relay** — if a member sends the bot a direct message, its content is forwarded to a staff member so it can be answered, since the bot has no other support channel. It is not otherwise stored.
- **Operational logs** — the bot writes debug/info logs to local log files on its host for troubleshooting. These logs may include message content and user tags involved in the events above.

## Where data is stored

All of the above is stored locally on the server that hosts the bot. It is never transmitted to any third party, external analytics service, or advertising service. None of this data is used to train machine learning or AI models.

## Data retention

- Submission archive entries persist until the source message is deleted or a moderator/author removes them.
- Mute records persist only while the mute is active.
- Log files are size-capped and rotated/compressed automatically, and are periodically cleared by the bot operator.

## Your choices

Because this bot is a moderation/community-management tool operating on data you send within a specific Discord server, individual opt-out isn't offered as a toggle — participation in the server's suggestion/bug-report channels and use of the bot's commands are voluntary. You can avoid the bot processing your messages by not posting in the designated channels and not DMing the bot. You may contact the operator (below) to request removal of any archived data concerning you.

## Contact

For questions or data removal requests, contact the operator at: **deployer-bot@zelophed.me**
