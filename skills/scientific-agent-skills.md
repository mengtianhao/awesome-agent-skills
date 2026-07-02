# Scientific Agent Skills

[??](scientific-agent-skills_zh.md)

## Links

- Repository: https://github.com/K-Dense-AI/scientific-agent-skills
- README: https://github.com/K-Dense-AI/scientific-agent-skills/blob/main/README.md
- Skills directory: https://github.com/K-Dense-AI/scientific-agent-skills/tree/main/skills
- Agent Skills standard: https://agentskills.io

## Summary

Scientific Agent Skills is a large open Agent Skills repository maintained by K-Dense AI. It is intended to turn an AI coding agent into a scientific research assistant by giving it curated instructions, examples, and integration notes for scientific workflows.

The README describes the repository as a collection of 148 ready-to-use scientific and research skills, with coverage across biology, chemistry, medicine, drug discovery, data analysis, visualization, scientific computing, and research communication. It also advertises access patterns for 100+ scientific and database resources.

## Main Capability Areas

- Bioinformatics, genomics, single-cell analysis, variant annotation, phylogenetics, and systems biology.
- Cheminformatics and drug discovery, including molecular property prediction, virtual screening, ADMET, docking, and lead optimization.
- Proteomics, mass spectrometry, clinical research, precision medicine, healthcare AI, and medical imaging.
- Scientific computing and machine learning, including PyTorch Lightning, scikit-learn, Qiskit, PennyLane, OpenMM, MDAnalysis, scVelo, TimesFM, and related Python package workflows.
- Materials science, chemistry, physics, astronomy, engineering, simulation, geospatial science, remote sensing, laboratory automation, and research methodology.
- Scientific communication workflows such as literature review, peer review, scientific writing, document processing, posters, slides, schematics, citation management, and diagrams.

## Installation Notes

Not installed locally.

The README gives the standard install command:

```text
npx skills add K-Dense-AI/scientific-agent-skills
```

It also documents GitHub CLI installation for compatible environments:

```text
gh skill install K-Dense-AI/scientific-agent-skills
gh skill install K-Dense-AI/scientific-agent-skills --agent codex
```

Because this is a large repository, install only the needed subset when possible and review individual `SKILL.md` files before use.

## Overlap With Current Installed Skills

| Scientific Agent Skills Area | Current Installed Skill(s) | Overlap |
| --- | --- | --- |
| Academic writing, reading, polishing, citation, peer review | `nature-writing`, `nature-polishing`, `nature-reader`, `nature-citation`, `nature-reviewer`, `nature-response`, `paper-spine` | High |
| Literature search and reference workflows | `nature-academic-search`, `nature-citation`, `paper-spine-citation` | High |
| Scientific figures and visualization | `nature-figure`, `spreadsheets` | Medium |
| Document, PDF, slide, and spreadsheet outputs | `docx`, `documents`, `pdf`, `presentations`, `spreadsheets` | Low-medium |
| General research automation | `paper-spine`, `agently-mail`, local Codex skills | Medium |

## Why Keep It

- It is one of the broadest public skill collections focused specifically on scientific research workflows.
- It covers many technical domains not fully covered by the local Nature and PaperSpine skills, especially bioinformatics, cheminformatics, drug discovery, scientific databases, scientific Python packages, and lab/research integrations.
- It is useful as a reference library even when individual skills are not installed.
- It follows the open Agent Skills convention and lists Codex compatibility.

## Cautions

- Skills can instruct the agent to install packages, run code, call external APIs, or modify files.
- The README itself recommends reviewing skills before installation.
- For production research, validate outputs and data provenance independently.

## Notes

- License: MIT.
- Stars when checked: about 29.8k.
- Last checked: 2026-07-02.
