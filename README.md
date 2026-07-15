# claude-md

Production `CLAUDE.md` configs for implementation agents.

Synthesized from the best open-source CLAUDE.md files:
- [zarfld/IntelAvbFilter](https://github.com/zarfld/IntelAvbFilter/blob/main/claude.md) — RULE 0, Root Cause Discipline, Investigation Protocol, Explicit Reasoning
- [Capataina/Flat-Browser](https://github.com/Capataina/Flat-Browser/blob/main/claude.md) — Underlying Intent, Scope Expansion, Proactive Improvement, Engineering Standards
- [samber/cc-skills-golang](https://github.com/samber/cc-skills-golang/blob/main/CLAUDE.md) — ultrathink/ultracode policy, Persona, Diagnose-before-fix

## Structure

```
clause-md/
├── README.md
├── draft/
│   └── CLAUDE.md          ← synthesized file, ready to drop in any repo
└── modules/
    ├── zarfld-IntelAvbFilter.md
    ├── capataina-flat-browser.md
    └── samber-cc-skills-golang.md
```

## Usage

Clone and copy `draft/CLAUDE.md` into your repo root. Trim any sections that don't apply to your stack.

```bash
git clone https://github.com/netbrah/claude-md
cp claude-md/draft/CLAUDE.md ./CLAUDE.md
```
