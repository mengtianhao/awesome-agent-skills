# PaperSpine

[English](paper-spine.md)

## 链接

- 仓库：https://github.com/WUBING2023/PaperSpine
- 中文 README：https://github.com/WUBING2023/PaperSpine/blob/main/README.md
- 英文 README：https://github.com/WUBING2023/PaperSpine/blob/main/README.en.md
- Codex skills 目录：https://github.com/WUBING2023/PaperSpine/tree/main/dist/codex/skills

## 简介

PaperSpine 是一个面向 Codex、Claude Code 和 OpenClaw 的学术论文/报告写作 skill suite。它以 motivation 为主线，适合目标格式很重要的写作任务，例如期刊论文、会议论文、课程或技术报告、综述和竞赛论文。

它要求 agent 在写作前先学习目标场景和优秀样例，与用户确认核心 motivation，然后再生成可审计的中间产物，例如研究档案、引用支持库、写作理由矩阵、LaTeX 报告和最终产物清单。

## 已安装的 Codex Skills

| Skill | 用途 |
| --- | --- |
| `paper-spine` | 全流程主控入口 |
| `paper-spine-ui` | 终端配置 UI |
| `paper-spine-intake` | 配置校验和修复 |
| `paper-spine-research` | 目标场景研究、样例学习和 motivation 选项 |
| `paper-spine-citation` | 为句子级 claim 构建引用支持库 |
| `paper-spine-rewrite` | 对已有论文/报告进行实质性改写 |
| `paper-spine-build` | 从材料文件夹构建论文/报告 |
| `paper-spine-latex` | LaTeX/PDF/Word 组装和检查 |
| `paper-spine-audit` | 完整性、逻辑、引用、翻译和产物审计 |
| `paper-spine-translate` | 中文翻译包生成 |
| `paper-spine-humanize` | 分层学术文本 humanize 工作流，可独立使用 |
| `paper-spine-update` | 本地 PaperSpine 更新检查 |

## 安装说明

已于 2026-06-19 安装到本机：

```text
C:\Users\Lenovo\.codex\skills\paper-spine*
```

安装来源：

```text
WUBING2023/PaperSpine
dist/codex/skills/*
```

安装后需要重启 Codex 才能发现新技能。

## 主工作流

PaperSpine 有两条主流程：

- `rewrite_existing`：改进已有论文或报告，但不把任务降级为表层润色。
- `build_from_materials`：从材料文件夹构建论文或报告，材料可以包括笔记、PDF、图片、数据摘要、部分初稿或实验描述。

支持场景：

- `journal`：期刊论文
- `conference`：会议论文
- `report/review`：课程报告、技术报告或综述
- `competition`：竞赛论文或竞赛报告

核心产物包括：

- `paper_spine_config.json`
- `reference_materials/source_index.md`
- `research_dossier.md`
- `exemplar_learning_dossier.md`
- `sota_gap_map.md`
- `citation_support_bank.md`
- `confirmed_motivation.md`
- `section_blueprints.md`
- `writing_rationale_matrix.md`
- `latex_report.md`
- `final_paper/main.tex`
- 可选 `paper.pdf`、`paper.docx` 和 `translation_zh/`

## 与当前已安装技能的重叠

| PaperSpine 能力 | 当前已安装技能 | 重叠程度 |
| --- | --- | --- |
| 学术写作与结构设计 | `nature-writing`, `nature-polishing` | 高 |
| 引用支持 | `nature-citation`, `nature-academic-search` | 中高 |
| 审稿式检查 | `nature-reviewer`, `nature-response` | 中 |
| LaTeX 与排版检查 | `nature-polishing`, `pdf`, `docx` | 中 |
| Humanize | `humanizer`, `humanizer-zh` | 中 |

## 为什么保留

- 它是完整的论文工程流水线，不只是单点润色技能。
- 它强调确认 motivation、证据感知规划和可审计写作决策。
- 它会保留中间产物，方便检查论文逻辑和修改理由。
- 它可以生成 LaTeX 优先的最终产物，并支持可选 PDF、Word 和中文翻译包。

## 备注

- README 说明该项目暂时暂停维护到 7 月初。
- License：MIT。
- 最后检查日期：2026-06-19。

