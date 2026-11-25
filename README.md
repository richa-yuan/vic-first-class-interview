# Vic's First-Class Interview Skill

> 蒸馏 B站/抖音创作者「艾维奇Vic」头等舱偶遇访谈系列的方法论与思维框架
> A distillation of creator Vic's first-class-cabin interview methodology, based on full transcripts of his latest 50 videos.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-compatible-blue.svg)](https://agentskills.io)

---

## 这是什么 / What is this

这是一个遵循 [Agent Skills 开放标准](https://agentskills.io/specification) 的 Markdown 知识技能包。它把创作者 **艾维奇Vic**（全网千万粉丝）最近 50 期视频，蒸馏成一套可被各类 AI Agent 加载使用的「访谈方法论 + 内容创作 + 认知框架」。

Unlike title-based summaries, this skill is built from **full audio transcripts**:
- Downloaded all 50 videos (2026-08-06 → 2026-11-22) and transcribed them with Whisper
- **18,856 segments / 446,000 Chinese characters** of verbatim transcripts (`transcripts/`)
- 5 parallel reading passes extracting real openers, question chains, rejection handling, closings, and guest quotes
- All scripts and quotes are from the transcripts, not inferred from titles

### 能力 / Capabilities

| 模式 | 说明 |
|------|------|
| 🎭 角色扮演 | 用 Vic 第一人称语气对话、模拟采访 |
| 🎤 访谈脚本 | 生成同款开场白、提问链、拒绝应对、收尾 |
| ✍️ 内容创作 | 标题公式、金句钩子、口播文案、选题矩阵 |
| 🧠 认知输出 | 用"选择>努力、认知变现、长期主义、视野破局"等框架分析问题 |

---

## 安装 / Installation

本 skill 是纯 Markdown，无运行时依赖。按你使用的 Agent 选择对应方式：

### Claude Code

```bash
# 方式1：克隆到 skills 目录
git clone https://github.com/richa-yuan/vic-first-class-interview.git \
  ~/.claude/skills/vic-first-class-interview

# 方式2：放到项目级 skills 目录
git clone https://github.com/richa-yuan/vic-first-class-interview.git \
  .claude/skills/vic-first-class-interview
```

### OpenAI Codex

```bash
git clone https://github.com/richa-yuan/vic-first-class-interview.git \
  ~/.codex/skills/vic-first-class-interview
```

### Cursor

将仓库克隆到 `.cursor/rules/` 或直接把 `SKILL.md` 内容加入 Cursor Rules。

### GitHub Copilot / Gemini CLI / 其他

把整个目录放到该 Agent 的 skills 目录；或直接把 `SKILL.md` 作为 system prompt / custom instruction 加载。

> 通用原则：任何支持读取本地 Markdown 作为上下文的 Agent，都可以把 `SKILL.md` 当作指令文件使用，并按其中引用按需加载 `references/`、`transcripts/`、`analysis/`。

---

## 使用示例 / Usage

安装后，直接用自然语言触发：

- "扮演艾维奇Vic，模拟采访我"
- "年轻人现在应该做什么最能成功？"（用 Vic 的认知框架回答）
- "帮我写一期头等舱采访脚本，采访一位创业者"
- "给我的视频起5个 Vic 风格的标题"
- "50期里关于AI的金句有哪些？"

Skill 会根据意图自动加载对应参考文件（见 `SKILL.md` 的"使用方式"表格）。

---

## 目录结构 / Structure

```
vic-first-class-interview/
├── SKILL.md                      # 标准入口：frontmatter + 指令
├── references/
│   ├── verbatim-scripts.md       # 真实话术库（开场/提问/拒绝/收尾）
│   ├── golden-quotes.md          # 受访者金句库（8大主题）
│   ├── question-bank.md          # 提问库（固定骨架+临场追问）
│   ├── content-formulas.md       # 内容公式（选题/标题/脚本）
│   ├── creator-profile.md        # 人物档案（经历/人设/语气）
│   ├── cognitive-framework.md    # 认知框架（五大底层逻辑）
│   └── video-catalog.md          # 50期片单+统计
├── transcripts/                  # 50期完整逐字稿（44.6万字）
├── analysis/                     # 5组分批精读报告
├── LICENSE                       # MIT
└── README.md
```

---

## 数据说明 / Data notes

- **来源**：B站公开视频（UID 1751550967），通过移动端公开 API 获取视频流，本地 Whisper 转写。
- **可信度分层**：【逐字实录】转写原文（已修明显错字）；【蒸馏】归纳规律；【背景资料】播客自述与媒体报道。
- **局限**：ASR 有个别识别误差；04/05 期为婚礼视频、32/38/41/42/49 期为独白式人文纪录片，无访谈对话，已单独归类。
- **版权**：原始数据版权归原作者所有。本仓库仅作个人研究与学习方法论蒸馏，引用金句请注明出处；请勿用于商业搬运或二次分发原视频内容。

---

## License

MIT — 详见 [LICENSE](LICENSE)。
