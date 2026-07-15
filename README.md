# claude-md

Production `CLAUDE.md` configs for implementation agents.

Synthesized from the best open-source CLAUDE.md files, then rewritten to obey Anthropic's own published guidance on effective CLAUDE.md files:
- [zarfld/IntelAvbFilter](https://github.com/zarfld/IntelAvbFilter/blob/main/claude.md) — Root Cause Discipline, Investigation Protocol, Chesterton's Fence, Handoff
- [Capataina/Flat-Browser](https://github.com/Capataina/Flat-Browser/blob/main/claude.md) — Underlying Intent, Scope Expansion, Proactive Improvement, Engineering Standards
- [samber/cc-skills-golang](https://github.com/samber/cc-skills-golang/blob/main/CLAUDE.md) — Persona, Diagnose-before-fix
- [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills/blob/main/CLAUDE.md) — Simplicity-first, Surgical Changes, Goal-Driven Execution

### Why the draft is short

Anthropic's [Claude Code best practices](https://www.anthropic.com/engineering/claude-code-best-practices) and [memory docs](https://docs.claude.com/en/docs/claude-code/memory) are explicit: keep CLAUDE.md under ~200 lines, apply the deletion test to every line ("would removing this cause a mistake?"), and dial back aggressive emphasis (`NEVER`/`YOU MUST`) because current models overtrigger on it. Long, emphatic files are a named anti-pattern ("the over-specified CLAUDE.md") — Claude ignores half of it because the important rules get lost in the noise. The draft is 114 lines of universal behavior; the project-specific commands, architecture, and gotchas (the highest-value content) go in the commented template at the bottom.

## Structure

```
claude-md/
├── README.md
├── draft/
│   ├── CLAUDE.md          ← synthesized behavioral file + project template
│   └── CLAUDE.vibes.md    ← pure posture/mindset, zero mechanics
└── modules/
    ├── zarfld-IntelAvbFilter.md
    ├── capataina-flat-browser.md
    ├── samber-cc-skills-golang.md
    └── multica-karpathy-skills.md
```

### Two flavors

- **`draft/CLAUDE.md`** — the full behavioral file: operator posture, root-cause and investigation discipline, surgical-change rules, verification, the ISR/SITREP decision flow, and a commented project-context template to fill in per repo. Stack-agnostic; drop in and add your commands/architecture/gotchas.
- **`draft/CLAUDE.vibes.md`** — the same headspace stripped to pure posture and mindset. No tools, no skills, no commands, no file layouts. Sets who the operator is and how they think, and lets the work fill in the rest. Run it alone, or pair it with a project file that carries the concrete mechanics.

## Usage

Clone and copy the flavor you want into your repo root. Trim any sections that don't apply to your stack.

```bash
git clone https://github.com/netbrah/claude-md
cp claude-md/draft/CLAUDE.md ./CLAUDE.md        # full behavioral file + project template
# or, pure posture only:
cp claude-md/draft/CLAUDE.vibes.md ./CLAUDE.md
```
