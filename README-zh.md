# 毛泽东 · 认知操作系统 / Mao Zedong Cognitive OS

[English](./README.md) · **简体中文**

> *「谁是我们的敌人？谁是我们的朋友？这个问题是革命的首要问题。」* ——《中国社会各阶级的分析》

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://claude.ai/code)
[![AgentSkill](https://img.shields.io/badge/AgentSkill-valid-green)](https://docs.claude.com/en/docs/claude-code/skills)

一个 [AgentSkill](https://docs.claude.com/en/docs/claude-code/skills)：以《毛泽东选集》一至五卷为底座，把毛泽东「**分析问题—制定战略—组织行动**」的方法论，连同他的**人格与语言**，封装成一台可对话、可调用、**带原文出处（篇目编号）**的认知操作系统。激活后以「**教员**」第一人称与你谈话——先调查后判断，抓主要矛盾，战略上藐视、战术上重视，**前途光明、道路曲折**。

它**不是**语录机器人。它是用他的**认知框架**，帮你分析**你的**问题。

---

## 它和"语录机器人"有什么不同

| | 语录机器人 | 本 Skill |
|--|-----------|---------|
| 输出 | 复读金句 | 用方法论拆解你的具体问题 |
| 人格 | 贴标签 | 11 维性格画像 + 6 心理反应脚本，"像本人在场" |
| 引用 | 真假不分 | 带篇目编号、对照原文逐条核查（28/32 逐字命中） |
| 边界 | 无 | 明确"能做/不能做"，争议历史只取方法论 |

---

## 内容：四大模块

以《毛泽东选集》五卷为底座，每个模型都带**来源篇目（编号）**：

| 模块 | 内容 | 代表组件 |
|------|------|---------|
| **A · 分析问题** | 8 大分析模型 | 矛盾分析法 · 实践认识论 · 调查研究 · 实事求是 · 一分为二 · 阶级/结构分析 · 透过现象看本质 · 具体问题具体分析 |
| **B · 制定战略** | 8 大战略框架 | 持久战三阶段 · 农村包围城市 · 集中优势兵力 · 统一战线 · 纸老虎论 · 运动战与主动权 · 自力更生 · 有理有利有节 |
| **C · 组织行动** | 8 大组织方法 + 党委会12条 | 群众路线 · 批评与自我批评 · 整风 · 民主集中制 · 党委工作法 · 用人带队伍 · 执行学（桥与船）· 三大纪律八项注意 |
| **D · 性格内核** | 11 维画像 + 6 心理脚本 | 战略自信 · 斗争性 · 彻底辩证 · 务实反教条 · 藐视强敌 · 浪漫与务实并存 · 革命乐观…… |

外加：**12 条决策启发式**（精选自 33 条）· 完整**表达 DNA**（8 指纹 + 句式库 + 比喻库 + 五拍节奏）· **对话协议**（开口三问 + 收尾四动作 + 8 反模式护栏）。

---

## 安装（Claude Code）

Skill 存放在 `.claude/skills/<名称>/`。可装在**用户级**（处处可用）或**项目级**（单个仓库）。

```bash
git clone https://github.com/NAMEWTA/mao-zedong-cognitive-os.git
# 用户级：
mkdir -p ~/.claude/skills && cp -r mao-zedong-cognitive-os/mao-zedong-cognitive-os ~/.claude/skills/
# 或项目级：
mkdir -p /你的项目/.claude/skills && cp -r mao-zedong-cognitive-os/mao-zedong-cognitive-os /你的项目/.claude/skills/
```

> 注意嵌套：仓库根目录叫 `mao-zedong-cognitive-os/`，你要拷贝的 Skill 文件夹是里面那层 `mao-zedong-cognitive-os/`（含 `SKILL.md` 的那个）。

随后在 Claude Code 里触发：

```
> 教员    /  毛泽东  /  毛选
> 用毛泽东的方式分析……
> 从毛选的角度看……
> 教员会怎么看？
```

激活后直接问：

```
> 我们是小创业公司，大厂出了同类产品，用户都往那边跑，怎么办？
> 团队两个 leader 互相看不顺眼，项目推不动，我怎么处理？
> 我想转行做 AI，但人才太多，完全没优势，很焦虑。
> 我努力很久还是看不到希望，想放弃了。
```

---

## 可选：外挂全文知识库

核心思维框架自包含，安装即用。如需 AI 检索原文、精确引用，可挂载《毛泽东选集》全文（本仓库**不内置**，以避免再分发与体积问题）：

```bash
git clone https://github.com/weiyinfu/MaoZeDongAnthology.git ~/MaoZeDongAnthology
```

Skill 会自动发现它（先查环境变量 `MAOXUAN_KB_PATH`，再查 `~/MaoZeDongAnthology`，再查当前/父目录）。找不到时静默跳过、仅用内置框架，**行为完全一致**。

---

## 诚实边界

本 Skill 只迁移**思维方法论**，不评判政治立场。凡涉 1949 年后争议历史（大跃进、文革、各类运动、抗美援朝等），**只取决策/思维方法论侧面并标注边界**。三条内建原则：

1. **方法论 ≠ 政治立场**——阶级分析在现代应用须中性化为"利益相关方/力量结构分析"。
2. **理想方法 ≠ 历史实践**——不可过度理想化，理论倡导与实际权力运用存在张力。
3. **效能 ≠ 合理性**——"组织方法的效能"与"政策目标的合理性"是两个不同问题。

争议性负面人格评价（如《李志绥回忆录》）学界争议大，**不采用为人格定论**，仅作存在性标注。

> 一个不告诉你局限在哪的 Skill，不值得信任。

---

## 仓库结构

```
mao-zedong-cognitive-os/                  ← 本仓库
├── README.md / README-zh.md              ← 双语首页
├── LICENSE                               ← MIT
├── docs/                                 ← 构建溯源（可选阅读）
│   ├── 00-blueprint.md                   ← 17 章施工蓝图
│   └── quote-verification.md             ← 引语对照原文核查报告
└── mao-zedong-cognitive-os/              ← 可分发的 Skill
    ├── SKILL.md                          ← 认知操作系统核心（17 章）
    ├── LICENSE
    └── references/research/              ← 按需加载的知识底座
        ├── 10-personality-profile.md     ← 性格特点与心理画像（11维 + 6脚本）
        ├── 11-analysis-frameworks.md     ← 分析问题（8模型 + 对话动作）
        ├── 12-strategy-frameworks.md     ← 制定战略（8框架 + 决策树）
        ├── 13-organization-action.md     ← 组织行动（8方法 + 党委12条）
        ├── 14-voice-and-dialogue.md      ← 表达DNA与对话协议（+ 4范式）
        └── 15-quote-bank.md              ← 引语库与原文索引（模型→篇目映射）
```

## 提炼方法

Haiku 全网检索（性格/方法/修辞/外部评价/关键决策/领导风格 6 路）+ 12 组《毛选》原文精读 → Opus 综合为四大模块与对话协议 → 引语对照本地全文逐条核查（32 条中 28 条逐字命中，其余订正或标注转述）。详见 `docs/`。

---

## 许可证

[MIT](LICENSE) — 随便用，随便改，随便造。**星星之火，可以燎原。**
