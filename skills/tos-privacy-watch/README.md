# ToS & Privacy Policy Watch

**Make your AI assistant read the fine print, so you don't have to.**

You get "We're updating our Terms of Service" emails all the time. Most people never open them, and the company's own summary usually skips the parts that matter. This is an [Agent Skill](https://agentskills.io) that has your AI assistant:

1. **Watch your inbox** for Terms of Service and Privacy Policy update emails, and for welcome emails from new sign-ups.
2. **Read the actual documents** on the company's official site, not the email's summary, and compare them with the previous version where possible.
3. **Flag what matters**: AI training on your content, data selling, forced arbitration, auto-renewal traps, broad licenses to your content, and more.
4. **Put deadlines first.** Some rights expire quietly, such as a 30-day window to opt out of arbitration, a free trial that converts to paid, or a mailed-letter-only way to reject new terms.

It's a single Markdown file with no code to run.

## What it found in a real inbox

From the first test run, with personal details removed (see [`examples/sample-digest.md`](examples/sample-digest.md)):

- **An online marketplace** updated its arbitration terms. The only way to reject the changes was a **mailed letter** within 30 days.
- **A B2B data platform** gives you **45 days from sign-up** to opt out of arbitration by email. Its terms also let your connected data help **grow its contact database**, which it sells to other customers.
- **A cloud storage service** now lets free accounts be closed after **6 months of inactivity**, and team admins can stop you from leaving a team.
- **A TV voice assistant** can turn on by accident, and human reviewers may read your chats if an activity setting is left on.

## Two modes

| Mode | When it runs | What you get |
|---|---|---|
| **Update watch** | A company emails about changed terms | What changed, what's concerning, and any deadline to act |
| **New sign-up snapshot** | You sign up for something new | What you just agreed to, the deadlines that started at sign-up, what you connected, how to leave, and a baseline for comparing future changes |

## Safety by design

This skill has an AI read email from strangers, so it's built to be careful:

- **Phishing check:** it confirms the sender's domain and never follows links in the email. It goes to the company's official site instead.
- **Prompt-injection guard:** text inside emails and documents is treated as data, never as instructions to the AI.
- **Ask before acting:** it never opts out, unsubscribes, replies or deletes anything without your OK.
- **Knows its limits:** it flags when you should bring in a lawyer, and every report ends with a not-legal-advice line.

## Install

### Claude (claude.ai, desktop, Claude Code)
- **Claude apps:** download [`SKILL.md`](SKILL.md) and upload it as a skill in Claude's settings.
- **Claude Code:** copy this folder into `~/.claude/skills/` (all your projects) or `.claude/skills/` (one project).

### GitHub Copilot, Cursor, Codex, Gemini CLI and other agents
```
gh skill install justLaurren/aetherr-public tos-privacy-watch
```
or
```
npx skills add justLaurren/aetherr-public --skill tos-privacy-watch
```

### Any AI assistant (ChatGPT, Gemini, Copilot…) as a prompt
Copy the contents of [`SKILL.md`](SKILL.md) into:
- **ChatGPT:** a Custom GPT's or Project's instructions
- **Gemini:** a Gem's instructions
- **Anything else:** paste it at the start of a chat

It works best with an email connector (Gmail or Outlook) and web browsing turned on. Without them, it asks you to paste the email or the policy text.

## Try it

> "Check my inbox for any terms of service or privacy policy updates."
>
> "Review the services I signed up for this month. What did I agree to?"
>
> "Here's an email from [company] about new terms. What changed?"

Run it weekly on a schedule if your assistant supports scheduled tasks.

## Customize it

Add your own priorities to the red-flag list in [`SKILL.md`](SKILL.md), for example:
- "I run a business. Flag anything about client data or confidentiality."
- "I care most about AI training on my content."
- "I'm in the EU/California/Colorado. Note any rights that gives me."

## Credits and related projects

- [Open Terms Archive](https://opentermsarchive.org) and [ToS;DR](https://tosdr.org): public archives and ratings of terms of service, used as sources
- [ConductAtlas](https://conductatlas.com): clause-level tracking that shows how common a clause is across platforms
- [Fineprint](https://dev.to/businessattire/fineprint-find-out-what-really-changed-in-the-tos-1405): an email-forwarding service whose lessons on choosing archived versions shaped Step 3

## Disclaimer

This is a plain-language awareness tool, **not legal advice**. AI can misread documents or miss details. For high-stakes decisions, especially business accounts, arbitration, or regulated data, talk to a lawyer.

## License

[MIT](LICENSE) © 2026 Laurren Kanner · Built by [AEtherR Advisory](https://aetherr.pro)
