# PaperSpine

## Links

* Repository: https://github.com/WUBING2023/PaperSpine
* Documentation: https://github.com/WUBING2023/PaperSpine/blob/main/README.md
* English README: https://github.com/WUBING2023/PaperSpine/blob/main/README.en.md
* Install guide: https://github.com/WUBING2023/PaperSpine/blob/main/README.md#快速安装
* Windows install script: https://github.com/WUBING2023/PaperSpine/blob/main/install.ps1
* macOS / Linux install script: https://github.com/WUBING2023/PaperSpine/blob/main/install.sh

## Summary

PaperSpine is a motivation-driven academic writing skill suite for Codex, Claude Code, and OpenClaw. It is designed for writing tasks where target format, argument structure, citation support, and final deliverable quality are important, including journal papers, conference papers, course reports, technical reports, reviews, and competition papers.

PaperSpine is not a simple polishing or sentence-level rewriting tool. Its core workflow asks the agent to first learn the target venue or target writing scenario, study strong examples, clarify the paper's motivation and contribution spine, then perform rewriting or paper construction with evidence, section blueprints, citation support, revision matrices, LaTeX generation, translation support, and final audit.

## Available Skills

| Skill                   | Purpose                                                                                                                                                   |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `paper-spine`           | Main controller for the full PaperSpine workflow. It routes the task across research, citation, rewriting/building, LaTeX, translation, and audit stages. |
| `paper-spine-ui`        | Opens or supports the external configuration UI for one PaperSpine run.                                                                                   |
| `paper-spine-intake`    | Validates or repairs `paper_spine_config.json` before the main workflow starts.                                                                           |
| `paper-spine-research`  | Learns target venue requirements, official writing constraints, exemplar papers, and relevant high-quality papers.                                        |
| `paper-spine-citation`  | Builds a claim-level citation support bank for Introduction, Related Work, Discussion, limitations, and application background.                           |
| `paper-spine-rewrite`   | Rewrites an existing manuscript based on confirmed motivation, evidence, section blueprints, and writing rationale matrices.                              |
| `paper-spine-build`     | Builds a paper or report from a materials folder, such as notes, figures, PDFs, experiment summaries, partial drafts, and descriptions.                   |
| `paper-spine-latex`     | Assembles and checks LaTeX output, handles figures, tables, labels, references, PDF generation when available, and optional Word output.                  |
| `paper-spine-audit`     | Audits output completeness, writing-rationale depth, citation support quality, translation coverage, and file health.                                     |
| `paper-spine-translate` | Generates a Chinese translation package for English output, including translated intermediate and final Markdown artifacts.                               |
| `paper-spine-humanize`  | Applies controlled humanization passes and records changes through a humanize matrix.                                                                     |
| `paper-spine-update`    | Checks or updates the local PaperSpine installation while preserving global configuration.                                                                |

## Installation Notes

PaperSpine supports Codex, Claude Code, and OpenClaw. The repository provides installation scripts for Windows and macOS / Linux.

### Windows PowerShell

```powershell
git clone https://github.com/WUBING2023/PaperSpine.git
cd PaperSpine
.\install.ps1 -Target all
```

Install only one host:

```powershell
.\install.ps1 -Target codex
.\install.ps1 -Target claude
.\install.ps1 -Target openclaw
```

Clean legacy or duplicated installations while installing:

```powershell
.\install.ps1 -Target all -CleanLegacy
```

### macOS / Linux

```bash
git clone https://github.com/WUBING2023/PaperSpine.git
cd PaperSpine
bash install.sh --target all
```

### Manual Installation for Codex

Codex now recommends the flat skill suite layout. Copy:

```text
dist/codex/skills/*
```

to:

```text
~/.codex/skills/
```

Expected Codex layout:

```text
~/.codex/skills/paper-spine/SKILL.md
~/.codex/skills/paper-spine-research/SKILL.md
~/.codex/skills/paper-spine-citation/SKILL.md
~/.codex/skills/paper-spine-latex/SKILL.md
~/.codex/skills/paper-spine-update/SKILL.md
```

After installation, restart Codex. Use:

```text
$paper-spine
```

or call a branch skill directly, for example:

```text
$paper-spine-research
$paper-spine-citation
$paper-spine-latex
```

### Manual Installation for Claude Code

Copy:

```text
dist/claude/skills/*
dist/claude/commands/*.md
```

to:

```text
~/.claude/skills/
~/.claude/commands/
```

Expected Claude Code layout:

```text
~/.claude/skills/paper-spine/SKILL.md
~/.claude/skills/paper-spine-ui/SKILL.md
~/.claude/skills/paper-spine-intake/SKILL.md
~/.claude/skills/paper-spine-research/SKILL.md
~/.claude/skills/paper-spine-citation/SKILL.md
~/.claude/skills/paper-spine-update/SKILL.md
~/.claude/commands/paperspine.md
```

After installation, restart or reload Claude Code. Use:

```text
/paperspine
```

### Claude Code Plugin Installation

Claude Code can also install PaperSpine through plugin commands:

```text
/plugin marketplace add https://github.com/WUBING2023/PaperSpine
/plugin install paper-spine
/reload-plugins
```

### Manual Installation for OpenClaw

Copy:

```text
dist/openclaw/skills/*
```

to:

```text
~/.openclaw/skills/
```

Expected OpenClaw layout:

```text
~/.openclaw/skills/paper-spine/SKILL.md
~/.openclaw/skills/paper-spine-research/SKILL.md
~/.openclaw/skills/paper-spine-citation/SKILL.md
~/.openclaw/skills/paper-spine-update/SKILL.md
```

After installation, restart or reload OpenClaw. Use:

```text
paper-spine
```

or call a branch skill directly, for example:

```text
paper-spine-research
paper-spine-citation
paper-spine-update
```

### Important Installation Warning

Do not copy the whole PaperSpine repository directly into a `skills` directory. The installable content is under `dist/`. Copying the entire repository may cause duplicated discovery, nested skill folders, or missing skills.

## Main Workflows

PaperSpine has two main workflows.

### Rewrite Existing

Use this workflow when there is already a manuscript, paper draft, report draft, or partially written document. The goal is not shallow polishing, but structural rewriting based on target requirements, motivation, evidence, citation support, section-level planning, and audit results.

Typical use cases:

* rewriting a journal paper draft;
* strengthening Introduction motivation;
* restructuring Method and Experiment sections;
* improving Discussion and limitations;
* converting a weak report into a target-format academic report;
* checking whether claims are supported by citations and experiment evidence.

### Build From Materials

Use this workflow when there is not yet a complete manuscript, but there are materials such as experiment notes, figures, tables, PDF references, result summaries, partial drafts, project descriptions, or method notes.

Typical use cases:

* building a paper from experiment outputs and method descriptions;
* building a course report from notes and references;
* building a technical report from project materials;
* building a competition paper from solution notes and results.

## Target Scenarios

PaperSpine supports the following target scenarios:

| Scenario        | Meaning                                    |
| --------------- | ------------------------------------------ |
| `journal`       | Journal paper                              |
| `conference`    | Conference paper                           |
| `report/review` | Course report, technical report, or review |
| `competition`   | Competition paper or competition report    |

## Research Depth

| Mode    | Meaning                                                                                                                               |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| `flash` | Lighter research mode. It studies a smaller set of target examples, recent or high-quality related papers, and official requirements. |
| `pro`   | Deeper research mode. It studies more target examples, more recent or high-quality related papers, and official requirements.         |

## Output Language

PaperSpine supports:

* `English`
* `Chinese`

When English output is selected, PaperSpine can also generate a Chinese translation package for intermediate artifacts and final Markdown output.

## Typical Outputs

Depending on the selected workflow and available tools, PaperSpine may produce files such as:

```text
paper_rewriting_output/research_dossier.md
paper_rewriting_output/sota_gap_map.md
paper_rewriting_output/citation_support_bank.md
paper_rewriting_output/section_blueprints.md
paper_rewriting_output/writing_rationale_matrix.md
paper_rewriting_output/rewrite_matrix.md
paper_rewriting_output/latex_report.md
paper_rewriting_output/final_paper/main.tex
paper_rewriting_output/final_paper/paper.pdf
paper_rewriting_output/final_paper/paper.docx
paper_rewriting_output/translation_zh/
```

The most important idea is that PaperSpine keeps a traceable writing process. It does not only output the final paper; it also records research findings, motivation choices, section plans, citation support, and rationale for major writing decisions.

## Example Usage

### Codex Full Workflow

```text
$paper-spine

Task type: rewrite_existing
Target scenario: journal
Research depth: flash
Output language: English
Materials folder: ./materials
Special requirements:
1. Do not invent unsupported experimental results.
2. Do not exaggerate contributions.
3. Strengthen motivation, method rationale, ablation explanation, and clinical relevance.
4. Preserve LaTeX equations, tables, figure numbers, and citation keys.
5. Output final_paper/main.tex and optional docx if supported.
```

### Codex Research Only

```text
$paper-spine-research

Study the target journal requirements, strong exemplar papers, and recent related work.
Generate a research dossier, SOTA gap map, and candidate motivation options.
```

### Codex Citation Support Only

```text
$paper-spine-citation

Build a claim-level citation support bank for the current manuscript.
Focus on Introduction, Related Work, Discussion, limitations, and clinical/application background.
```

### Claude Code

```text
/paperspine
```

Then select or configure the workflow according to the target paper or report task.

## Overlap With Current Installed Skills

| PaperSpine Skill        | Current Installed Skill(s)          | Overlap    | Notes                                                                                                                                   |
| ----------------------- | ----------------------------------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| `paper-spine-latex`     | `latex`, `pdf`, `docx`              | Medium     | PaperSpine focuses on paper/report assembly and audit, while general LaTeX/PDF/Word skills are broader document tools.                  |
| `paper-spine-audit`     | `documents`, `pdf`, `docx`          | Medium     | Overlap exists in document checking, but PaperSpine adds academic-writing-specific checks such as rationale depth and citation support. |
| `paper-spine-rewrite`   | writing and rewriting workflows     | Medium     | It overlaps with general rewriting, but is more structured and motivation-driven.                                                       |
| `paper-spine-build`     | document drafting workflows         | Medium     | It overlaps with report generation, but adds research, evidence, and academic structure constraints.                                    |
| `paper-spine-citation`  | web research and citation workflows | Medium     | It focuses on claim-level academic citation support rather than general web search.                                                     |
| `paper-spine-translate` | translation workflows               | Low-medium | It focuses on translating PaperSpine outputs and maintaining coverage across generated artifacts.                                       |
| `paper-spine-humanize`  | style rewriting workflows           | Low-medium | It provides controlled humanization with traceable change records.                                                                      |
| `paper-spine-update`    | none                                | Low        | Mainly useful for maintaining the local PaperSpine installation.                                                                        |

## Why Keep It

* It is useful for research papers, technical reports, course reports, reviews, and competition papers where argument structure matters.
* It supports both rewriting existing manuscripts and building papers from materials.
* It encourages agents to learn the target venue or target scenario before writing.
* It separates research, citation support, rewriting/building, LaTeX generation, translation, and audit into dedicated branch skills.
* It is suitable for tasks that need traceable writing decisions instead of shallow polishing.
* It can help reduce unsupported claims by building a citation support bank before final writing.
* It can help keep LaTeX, PDF, optional Word output, translation package, and audit records organized.

## Best Fit

PaperSpine is especially useful for:

* journal paper rewriting;
* conference paper rewriting;
* Introduction and motivation reconstruction;
* Method section restructuring;
* experiment analysis and ablation explanation;
* Discussion and limitation writing;
* literature-backed academic report generation;
* LaTeX paper assembly;
* claim-level citation checking;
* English paper output with Chinese translation package.

## Less Suitable For

PaperSpine may be less suitable for:

* very small sentence-level polishing tasks;
* casual blog posts;
* tasks that do not need citations or target-format control;
* simple document conversion tasks;
* quick grammar-only edits.

For these tasks, a smaller writing, document, or translation skill may be more efficient.

## Notes

* Status: useful academic writing skill suite.
* Recommended install source: use the relevant `dist/*/skills/*` folder rather than the whole repository.
* Recommended entry for Codex: `$paper-spine`.
* Recommended entry for Claude Code: `/paperspine`.
* Recommended entry for OpenClaw: `paper-spine`.
* Last checked: 2026-06-19.
