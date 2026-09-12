---
name: important-gmail-notifier
description: Scans the user's Gmail inbox and flags which emails genuinely need their attention right now, filtering out newsletters, marketing, and automated confirmations first. Use this skill whenever the user asks to check their important emails, asks "any emails I need to deal with", "what's urgent in my inbox", "anything from work/bank/etc I'm missing", or otherwise wants a triage of their unread or recent Gmail rather than a full inbox read-through. Handles both Dutch and English emails. Do not use this skill for sending, drafting, or searching for a specific known email — only for the "what needs my attention" triage use case.
---

# Important Gmail Email Notifier

Triage the user's inbox and surface only what actually needs a human decision or action — nothing else. The value of this skill is precision: a short, trustworthy list beats a long, noisy one. When in doubt about whether something is important, lean toward including it, but always be able to state in one sentence *why* it needs attention.

## When this is invoked

Only run this on an explicit request from the user (e.g. "check my important emails," "anything urgent?"). This skill does not run in the background or on a schedule.

## Step 1: Determine scope

Default scope: unread emails, plus read emails from the last 24–48 hours. If the user specifies a different range or label in their request (e.g. "just today," "check my Bills label"), use that instead.

Use Gmail search/list tools to pull this set. Pull enough of the subject/snippet/sender to make Stage 1 decisions without necessarily opening every full message body yet — save full-body reads for emails that survive Stage 1 and need Stage 2 judgment.

## Step 2: Filter pass (noise removal)

Do this as its own explicit pass, before any importance judgment. The goal here is purely mechanical: remove what is clearly not actionable, regardless of sender.

Treat as noise and exclude, regardless of who it's from:
- Newsletters, marketing, and promotional emails
- Automated confirmations and status updates with no action required — e.g. "we received your application," "your order has shipped," "payment received" receipts, automated no-reply notifications
- Routine recurring statements with nothing flagged as due or overdue (e.g. a monthly account summary with no balance issue)

Important: sender identity does not exempt an email from this filter. A bank, employer, or club you care about can still send noise (e.g. Rabobank sending an automated "application received" email is noise, even though Rabobank as a sender can also send emails that matter). Judge the *email*, not the sender's general importance.

If genuinely unsure whether something is noise or not, don't drop it — pass it to Stage 2 instead. This filter should only remove clear-cut cases.

## Step 3: Judgment pass (importance)

For everything that survived the filter, decide if it needs the user's attention. Read enough of the body to judge accurately — don't guess from subject line alone. Look for these signals (in English and Dutch, since the user's inbox contains both):

| Signal | English cues | Dutch cues |
|---|---|---|
| Deadline / time pressure | "by [date]," "due," "expires," "last chance," "reminder" | "voor [datum]," "vervalt," "herinnering," "uiterlijk" |
| Decision or reply needed | "please confirm," "let us know," "RSVP," a direct question | "graag bevestigen," "laat weten," a direct question |
| Money involved | invoice, payment due, overdue balance, refund, fee | "factuur," "betaling," "openstaand bedrag," "achterstallig" |
| Account/identity issue | account number referenced with a problem, security alert, login issue | "klantnummer" referenced with a problem, "beveiliging" |
| Career-relevant step | interview invite, recruiter follow-up, an offer, a request for documents | "sollicitatiegesprek," "recruiter," "aanbieding" |
| Personal commitment | a club, team, or association needs a response, payment, or your presence | membership/association emails needing action |
| Suspicious sender domain | domain doesn't match the organization it claims to be from (e.g. a "bank" alert from a domain that isn't the bank's real one), unexpected login/transaction alerts, urgency + a link/request for credentials | same pattern in Dutch-language phishing attempts |

An email counts as important if it clearly needs the user to *do* something (reply, pay, decide, show up, prepare) or *know* something time-sensitive that affects them directly. It does not count as important just because the sender is generally significant (see Stage 2 filtering) — the content itself must carry the weight.

When genuinely ambiguous, include it and say why you weren't fully sure, rather than silently dropping it.

**Security caveat rule:** if an email claims to be from a bank, delivery service, government body, or other trusted institution but the sender's domain looks off (misspelled, wrong TLD, unrelated domain hosting a "bank" or "account" alert), flag it as important — but frame it as a security caution, not as a routine matter. Say plainly that it looks suspicious and the user should verify independently (e.g. log in directly via the official site/app) rather than click any link or reply. Don't just treat it like a normal transaction/account alert, and don't try to verify the domain's legitimacy yourself beyond a plausibility check — when in doubt, flag it as suspicious rather than deciding it's safe.

## Step 4: Report back

Output a short chat summary, not a file or long report. For each important email:

**Format:**
```
- [Sender] — [Subject]: [one-line reason it matters]
```

Group into two tiers only if there's a clear split worth calling out (e.g. "Needs action today" vs "Worth a look this week") — otherwise a flat list is fine. Keep the total response tight: this should be scannable in a few seconds, not read like a report.

If nothing important turned up, say so plainly and briefly — don't pad the response.

## Notes

- Don't ask the user for confirmation before filtering — apply your judgment and show the result. It's easier for the user to correct a flagged item than to review a huge unfiltered list.
- If the user gives feedback like "that one wasn't actually important" or "you missed one," treat it as a standing calibration signal for future checks in this conversation, not just a one-off correction.
- Never take action on emails (reply, archive, delete) as part of this skill — it's a read-and-report task only, unless the user separately asks you to act on something you found.