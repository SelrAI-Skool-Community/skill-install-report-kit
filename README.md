# Skill Install Report

**What it is:** a Claude Code skill that vets any other skill before you trust
it. It reads every file inside the skill, runs a six-check security review,
and hands you a single visual HTML report — a verdict banner, a plain-English
"how it works" walkthrough, a file-by-file table, and what the skill is
actually worth to your business.

**Who it's for:** anyone installing Claude skills from the internet. You should
never run an unvetted skill — this reviews everything in the skill's files
without executing a line of its code, and tells you plainly what was found.

One honest limit: it reads source, it never runs anything. Runtime behaviour,
live dependencies, and anything a skill downloads later are outside its scope,
and the report says so rather than pretending otherwise.

## The six checks

1. Hidden instructions (prompt injection)
2. Credential access
3. Network calls
4. Destructive commands
5. Obfuscated code
6. Scope of permissions

Score out of 100 → **Safe to use** (85+) / **Use with care** (60–84) /
**Do not use until fixed** (below 60, or any hard Fail).

## Install

Copy this folder into your skills directory:

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/luke-heka/skill-install-report-kit.git ~/.claude/skills/skill-install-report
```

If `~/.claude/skills` didn't exist before, restart Claude Code so it picks the
skill up. Then say: **"vet this skill"** or **"is this skill safe"**
about any skill folder. The report lands in the skill's own folder as
`SELR-REPORT.html` and opens in your browser.

See `SETUP-PROMPT.md` for a paste-ready prompt.

---

Made by Selr AI.
