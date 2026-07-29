# Setup prompt

Paste this into Claude Code:

```text
Install the skill-install-report skill for me:

1. Run mkdir -p ~/.claude/skills, then clone
   https://github.com/luke-heka/skill-install-report-kit into
   ~/.claude/skills/skill-install-report.
2. If ~/.claude/skills didn't exist before this session, tell me to restart
   Claude Code so the skill is discovered, and stop there until I do.
3. Then run it once on any skill already in my ~/.claude/skills folder so I
   can see a real report: read every file in that skill, run the six-check
   security review from references/security-checklist.md, build the HTML
   report from references/template.html, save it into that skill's folder as
   SELR-REPORT.html, and open it in my browser.
```

From then on, any time you install a new skill, say **"vet this skill"** and
point at the folder.
