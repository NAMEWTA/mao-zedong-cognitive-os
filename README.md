# 毛泽东 · 认知操作系统 / Mao Zedong Cognitive OS

**English** · [简体中文](./README-zh.md)

> *"Who are our enemies? Who are our friends? This is a question of the first importance for the revolution."* — *Analysis of the Classes in Chinese Society*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://claude.ai/code)
[![AgentSkill](https://img.shields.io/badge/AgentSkill-valid-green)](https://docs.claude.com/en/docs/claude-code/skills)

An [AgentSkill](https://docs.claude.com/en/docs/claude-code/skills) that distills Mao Zedong's methodology for **analyzing problems, formulating strategy, and organizing action** — together with his personality and voice — into a conversational, citable **cognitive operating system**. When activated, it talks to you in the first person as *"the Teacher" (教员)*: investigate before judging, grasp the principal contradiction, despise the enemy strategically while taking it seriously tactically, the road is tortuous but the future is bright.

It is **not** a quotation bot. It is his *cognitive framework* applied to **your** problem.

---

## What's inside

A four-module operating system, grounded in the five volumes of the *Selected Works of Mao Zedong*, every model carrying its **source essay (number)**:

| Module | Content | Examples |
|--------|---------|----------|
| **A · Analyze problems** | 8 analytical models | Contradiction analysis · Practice→Knowledge cycle · Investigation & research · Seeking truth from facts · One-divides-into-two · Class/structure analysis · See essence through appearance · Concrete analysis of concrete conditions |
| **B · Formulate strategy** | 8 strategic frameworks | Protracted war (3 stages) · Encircle cities from the countryside · Concentrate superior force · United front · Paper-tiger doctrine · Mobile warfare & initiative · Self-reliance · Principled & measured struggle |
| **C · Organize action** | 8 organizational methods + 12-point Party-committee work method | Mass line · Criticism & self-criticism · Rectification · Democratic centralism · Cadre & team-building · Execution ("bridge or boat") · Discipline |
| **D · Personality core** | 11-dimension portrait + 6 psychological-reaction scripts | Strategic confidence · Struggle · Thorough dialectics · Anti-dogmatism · Despising strong foes · Romantic + hard-nosed · Revolutionary optimism… |

Plus: **12 decision heuristics** (selected from 33) · a complete **Expression DNA** (8 fingerprints, sentence templates, metaphor library, "five-beat rhythm") · a **dialogue protocol** (three opening questions, four closing moves, 8 anti-pattern guardrails).

---

## Install (Claude Code)

Skills live in `.claude/skills/<name>/`. Install at the **user level** (available everywhere) or **project level** (one repo).

```bash
git clone https://github.com/NAMEWTA/mao-zedong-cognitive-os.git
# user-level:
mkdir -p ~/.claude/skills && cp -r mao-zedong-cognitive-os/mao-zedong-cognitive-os ~/.claude/skills/
# or project-level:
mkdir -p /your/project/.claude/skills && cp -r mao-zedong-cognitive-os/mao-zedong-cognitive-os /your/project/.claude/skills/
```

> Note the nesting: the repo root is `mao-zedong-cognitive-os/`, and the skill folder you copy is the inner `mao-zedong-cognitive-os/` (the one containing `SKILL.md`).

Then trigger it in Claude Code:

```
> 教员    /  毛泽东  /  毛选
> Analyze this the way Mao would…
> 用毛泽东的方式分析……
> 教员会怎么看？
```

And just ask:

```
> We're a small startup; a giant shipped a similar product and users are leaving. What do we do?
> 团队两个 leader 互相看不顺眼，项目推不动，我怎么处理？
> I want to switch into AI but there's a glut of talent and I have no edge. I'm anxious.
> 我努力很久还是看不到希望，想放弃了。
```

---

## Optional: full-text knowledge base

The core framework is self-contained — install and go. For verbatim source retrieval and precise citation, mount the full *Selected Works* text (not bundled here, to avoid redistribution and repo bloat):

```bash
git clone https://github.com/weiyinfu/MaoZeDongAnthology.git ~/MaoZeDongAnthology
```

The skill auto-discovers it (env var `MAOXUAN_KB_PATH`, then `~/MaoZeDongAnthology`, then the current/parent directory). If absent, the skill silently falls back to its built-in frameworks — behavior is identical.

---

## Honest boundaries

This skill transfers **thinking methodology only**; it does not judge political positions. For post-1949 contested history (the Great Leap Forward, the Cultural Revolution, campaigns, the Korean War, etc.) it extracts **only the decision/thinking-method aspect and flags the boundary**. Three principles, baked in:

1. **Methodology ≠ political stance** — class analysis is neutralized to "stakeholder / power-structure analysis" in modern use.
2. **Ideal method ≠ historical practice** — don't over-idealize; theory and actual exercise of power diverged.
3. **Efficacy ≠ legitimacy** — "the efficacy of an organizational method" and "the legitimacy of a policy goal" are two different questions.

Contested negative personality claims (e.g. from *The Private Life of Chairman Mao*) are academically disputed and are **not** adopted as personality conclusions, only noted as existing.

> A skill that doesn't tell you where its limits are isn't worth trusting.

---

## Repository structure

```
mao-zedong-cognitive-os/                  ← this repo
├── README.md / README-zh.md              ← bilingual landing pages
├── LICENSE                               ← MIT
├── docs/                                 ← provenance (optional reading)
│   ├── 00-blueprint.md                   ← 17-chapter construction blueprint
│   └── quote-verification.md             ← quote-vs-source verification report
└── mao-zedong-cognitive-os/              ← the distributable Skill
    ├── SKILL.md                          ← the cognitive OS (17 sections)
    ├── LICENSE
    └── references/research/              ← on-demand knowledge base
        ├── 10-personality-profile.md     ← personality (11 dims + 6 scripts)
        ├── 11-analysis-frameworks.md     ← 8 analysis models + dialogue moves
        ├── 12-strategy-frameworks.md     ← 8 strategy frameworks + decision trees
        ├── 13-organization-action.md     ← 8 org methods + 12-point checklist
        ├── 14-voice-and-dialogue.md      ← voice layer + 4 response templates
        └── 15-quote-bank.md              ← quote bank + model→essay mapping
```

## How it was built

Haiku fan-out web research (personality / methods / rhetoric / external reception / key decisions / leadership — 6 angles) + close reading of 12 clustered *Selected Works* essays → Opus synthesis into the four modules and the dialogue protocol → every quote checked verbatim against the local full text (28 of 32 exact matches; the rest corrected or marked as paraphrase). See `docs/`.

---

## License

[MIT](LICENSE) — use it, change it, build on it. *A single spark can start a prairie fire.*
