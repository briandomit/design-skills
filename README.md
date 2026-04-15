# Design Skills

7 AI skills for the UX design process. Each skill is a focused instruction set that can be used individually or in sequence.

## Skills

| Skill | What it does |
|-------|-------------|
| **define** | Problem definition, JTBD, requirements, OOUX object modeling (ORCA tables) |
| **research** | Discovery interviews, usability tests, UserTesting.com studies, synthesis |
| **prototype** | Interactive single-file HTML prototype generation |
| **review** | Design evaluation — coaching mode or structured 25-principle analysis |
| **cleanup** | Prototype file maintenance (dead code, inline styles, duplication) |
| **interview-guide-analysis** | Interview guide quality check against 7 dimensions |
| **design-pipeline** | Automated Blueprint prototype pipeline (Plan > Build > Evaluate) |

## Workflow

```
define > research (discovery) > prototype > review > research (usability) > cleanup
```

- **interview-guide-analysis** — use anytime before fieldwork
- **design-pipeline** — optional shortcut for prototype + review (Blueprint only)

## Installation

Copy the skill folders you want into your `~/.claude/skills/` directory:

```bash
# Clone the repo
git clone https://github.com/YOUR-USERNAME/design-skills.git

# Copy all skills
cp -r design-skills/*/ ~/.claude/skills/

# Or copy individual skills
cp -r design-skills/define ~/.claude/skills/
cp -r design-skills/research ~/.claude/skills/
```

Each skill folder contains a `SKILL.md` file and any reference files the skill needs.
