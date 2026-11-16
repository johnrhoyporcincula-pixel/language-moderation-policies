# How Moderation Works

This page explains how the bot decides what to do with a message, what each severity level means, how strikes work, and how to ask a human to look again. It is linked from every moderation notice the bot sends you.

**Short version:** an AI model reads each message and rates it as *None*, *Mild*, *Moderate* or *Severe*. What happens next depends on that rating, how sure the AI is, and how many recent strikes you already have in that severity. The AI can be wrong, and you can always ask a moderator to review the decision.

> Your server's admins can change some of the numbers below. To see the exact rules and your own strikes in a server, run **`/mystrikes`** in that server (only you can see the result).

---

## 1. The four severity levels

| Level | What it means |
|---|---|
| **None** | Ordinary conversation, disagreement, and non-targeted profanity. Nothing happens. |
| **Mild** | Low-intensity personal insults and name-calling. |
| **Moderate** | Stronger or repeated insults and degrading language. |
| **Severe** | Slurs, threats, dehumanizing language, and harassment. |

The bot understands English, Tagalog and Taglish. It reads the text of your message after cleaning up common tricks such as spaced-out letters, look-alike characters and stretched-out words.

## 2. What happens at each level (default settings)

| Level | 1st strike | Later strikes |
|---|---|---|
| **Mild** | Public warning | From the 3rd Mild strike, the message is also deleted |
| **Moderate** | Message deleted + warning | From the 2nd Moderate strike, a 10-minute timeout is added |
| **Severe** | Message deleted + warning + 30-minute timeout | Timeouts get longer with each repeat: 30 minutes, 1 day, 7 days, then 28 days |

Every action comes with a private message from the bot explaining what was detected and what happens if it occurs again.

## 3. How strikes work

- **Each severity is counted separately.** Two Mild strikes and one Moderate strike are not "three strikes"; the Mild count and the Moderate count each follow their own ladder above.
- **Strikes expire.** By default a Mild strike expires after 30 days, a Moderate strike after 60 days, and a Severe strike after 90 days. Expired strikes no longer affect what happens next.
- **Moderators can change your record.** If a moderator reviews a decision and changes the severity, your strikes are updated to match.
- **`/mystrikes`** shows your active strikes, when the next one expires, and what your next violation of each severity would lead to.

## 4. When the AI isn't sure

The AI gives every rating a confidence score. If the score is below the server's minimum (60% by default), the bot **does not punish you**. It sends a short reminder at most, and **no strike is recorded**.

## 5. Server-specific word rules

Server admins can also set rules for particular words. Depending on how an admin sets a word up, the bot may hide it, quietly flag the message for a moderator, apply a severity level, or delete / warn / time out regardless of the AI's rating. When a message is actioned because of one of these rules, your notice says so instead of showing an AI confidence score.

## 6. Reports

Any member can report a message the AI missed. **A report never punishes anyone by itself.** It goes to the moderators, and nothing counts toward anyone's strikes until a moderator confirms it.

## 7. If you think a decision was wrong

1. Press **Request Review** on the private message the bot sent you, and explain what you think went wrong (optional but helpful).
2. A moderator in that server claims your request and decides whether to uphold the decision or change the severity.
3. If they change it to **None**, the strike is removed and any timeout from that decision is lifted. A deleted message can't be restored, but the record is corrected.

You can check the status of your requests with **`/appeal-status`**.

## 8. Who is not moderated

Server administrators, the server's designated moderators, and any channels an admin has marked exempt are not run through the automatic moderation.

## 9. Limits you should know about

- The AI reads text only, not images or voice, and it can misread context, sarcasm or friendly banter. That is exactly why reviews exist.
- A moderator review decision is what counts. The AI's rating is a first pass, not a final judgment.

For how your data is handled, see the [Privacy Policy](PRIVACY_POLICY.md). For the rules of using the bot, see the [Terms of Service](TERMS_OF_SERVICE.md).
