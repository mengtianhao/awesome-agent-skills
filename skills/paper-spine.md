# PaperSpine

[中文](paper-spine_zh.md)

## Links

- Repository: https://github.com/WUBING2023/PaperSpine
- Chinese README: https://github.com/WUBING2023/PaperSpine/blob/main/README.md
- English README: https://github.com/WUBING2023/PaperSpine/blob/main/README.en.md
- Codex skills directory: https://github.com/WUBING2023/PaperSpine/tree/main/dist/codex/skills

## Summary

PaperSpine is a motivation-driven academic paper and report writing skill suite for Codex, Claude Code, and OpenClaw. It is designed for tasks where the target writing format matters, including journal papers, conference papers, course or technical reports, reviews, and competition papers.

The workflow asks the agent to learn the target scene and strong examples before writing, confirm a controlling motivation with the user, then produce auditable artifacts such as research dossiers, citation support banks, writing rationale matrices, LaTeX reports, and final artifact manifests.

## Installed Codex Skills

| Skill | Purpose |
| --- | --- |
| `paper-spine` | Main orchestrator for the full workflow |
| `paper-spine-ui` | Terminal configuration UI |
| `paper-spine-intake` | Configuration validation and repair |
| `paper-spine-research` | Target-scene research, exemplar learning, and motivation options |
| `paper-spine-citation` | Citation support bank for claim-level literature support |
| `paper-spine-rewrite` | Substantive rewrite of an existing manuscript |
| `paper-spine-build` | Build a paper/report from materials |
| `paper-spine-latex` | LaTeX/PDF/Word assembly and checks |
| `paper-spine-audit` | Completeness, logic, citation, translation, and artifact audits |
| `paper-spine-translate` | Chinese translation package generation |
| `paper-spine-humanize` | Tiered academic humanization workflow, usable standalone |
| `paper-spine-update` | Local PaperSpine update checks |

## Installation Notes

Installed locally on 2026-06-19 into:

```text
C:\Users\Lenovo\.codex\skills\paper-spine*
```

Installed from:

```text
WUBING2023/PaperSpine
dist/codex/skills/*
```

Restart Codex to pick up the newly installed skills.

## Main Workflow

PaperSpine has two primary workflows:

- `rewrite_existing`: improve an existing manuscript or report without reducing the task to surface polishing.
- `build_from_materials`: build a manuscript or report from a materials folder containing notes, PDFs, figures, data summaries, partial drafts, or experiment descriptions.

Supported scenes:

- `journal`
- `conference`
- `report/review`
- `competition`

Core outputs include:

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
- optional `paper.pdf`, `paper.docx`, and `translation_zh/`

## Overlap With Current Installed Skills

| PaperSpine Area | Current Installed Skill(s) | Overlap |
| --- | --- | --- |
| Academic writing and structure | `nature-writing`, `nature-polishing` | High |
| Citation support | `nature-citation`, `nature-academic-search` | Medium-high |
| Reviewer-style audit | `nature-reviewer`, `nature-response` | Medium |
| LaTeX and layout checks | `nature-polishing`, `pdf`, `docx` | Medium |
| Humanization | `humanizer`, `humanizer-zh` | Medium |

## Why Keep It

- It is a full paper-engineering pipeline rather than a single polishing skill.
- It emphasizes confirmed motivation, evidence-aware planning, and auditable writing decisions.
- It produces intermediate artifacts that make paper logic and revision choices easier to inspect.
- It can generate LaTeX-first final outputs with optional PDF, Word, and Chinese translation packages.

## Notes

- The README says maintenance is temporarily paused until early July.
- License: MIT.
- Last checked: 2026-06-19.

