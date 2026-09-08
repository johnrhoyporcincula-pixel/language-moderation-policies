# Privacy Policy

**Last updated:** [DATE]

This Privacy Policy explains what data this Discord moderation bot ("the Bot") collects, why, and how it is handled. By adding the Bot to a server or sending messages in a server where the Bot is active, you agree to this Policy.

## Data We Process

**Message content.** The Bot reads the text of messages sent in channels it has access to, in order to classify them for abusive language using a locally-run machine learning model. Message text is **not** sent to any third-party API or external cloud service — classification runs entirely on infrastructure operated by the Bot's developer.

**Discord identifiers.** The Bot stores Discord user IDs, server (guild) IDs, and channel/message IDs where relevant to a moderation action — for example, recording who sent a flagged message, who reported it, or which moderator resolved a review.

**Violation records.** When a message is classified as abusive, the Bot stores the message text, the detected severity, the moderator action taken, and the outcome of any review or appeal. This is used to track a member's moderation history and to apply consistent, escalating responses to repeated violations.

**Server configuration.** Server administrators may configure settings such as confidence thresholds, exempt roles/users, custom word rules, and a moderation-log channel. These settings are stored per-server.

## How Long Data Is Kept

Violation records used for automatic escalation expire after a configured number of days depending on severity (see the server's `/config` settings). Full historical records may be retained longer for moderator reference (e.g. `/history`, `/modstats`) unless a server administrator deletes them.

## Who Can Access Data

Access to stored data is limited to the Bot's developer and, within a given server, that server's moderators and administrators through the Bot's own commands (e.g. `/history`, `/reviews`). Data is **not sold, shared, or provided to any third party**, except where required by law.

## Data Deletion

A server administrator can remove all of the Bot's stored data for their server by deleting the Bot's local database file, or by contacting the developer to request deletion. Individual members may contact the developer to request removal of their personal violation history.

## Children's Privacy

The Bot is intended to be used in accordance with Discord's own Terms of Service, including Discord's minimum age requirements. The Bot does not knowingly collect data from users who do not meet those requirements.

## Changes to This Policy

This Policy may be updated as the Bot's features change. Continued use of the Bot after an update constitutes acceptance of the revised Policy.

## Contact

Questions about this Policy or data handling requests can be directed to: [YOUR CONTACT — e.g. Discord username, email, or support server link]
