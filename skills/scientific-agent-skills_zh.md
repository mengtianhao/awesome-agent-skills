# Scientific Agent Skills

[English](scientific-agent-skills.md)

## 链接

- 仓库：https://github.com/K-Dense-AI/scientific-agent-skills
- README：https://github.com/K-Dense-AI/scientific-agent-skills/blob/main/README.md
- Skills 目录：https://github.com/K-Dense-AI/scientific-agent-skills/tree/main/skills
- Agent Skills 标准：https://agentskills.io

## 简介

Scientific Agent Skills 是 K-Dense AI 维护的大型开放 Agent Skills 仓库。它的目标是把 AI coding agent 扩展为科研助手，通过结构化的 `SKILL.md`、示例和集成说明，帮助 agent 执行科学研究相关工作流。

该仓库 README 当前说明它包含 148 个可直接使用的科学与研究技能，覆盖生物学、化学、医学、药物发现、数据分析、可视化、科学计算和科研沟通等方向，并提供 100+ 科学数据库/资源的访问路径。

## 主要能力方向

- 生物信息学、基因组学、单细胞分析、变异注释、系统发育和系统生物学。
- 化学信息学与药物发现，包括分子性质预测、虚拟筛选、ADMET、分子对接和先导化合物优化。
- 蛋白质组学、质谱、临床研究、精准医学、医疗 AI 和医学影像。
- 科学计算与机器学习，包括 PyTorch Lightning、scikit-learn、Qiskit、PennyLane、OpenMM、MDAnalysis、scVelo、TimesFM 等 Python 包工作流。
- 材料科学、化学、物理、天文学、工程仿真、地理空间科学、遥感、实验室自动化和研究方法。
- 科研沟通，包括文献综述、同行评议、科学写作、文档处理、海报、幻灯片、示意图、引用管理和图表。

## 安装说明

当前未安装到本地。

README 给出的标准安装命令是：

```text
npx skills add K-Dense-AI/scientific-agent-skills
```

也提供 GitHub CLI 安装方式：

```text
gh skill install K-Dense-AI/scientific-agent-skills
gh skill install K-Dense-AI/scientific-agent-skills --agent codex
```

由于这是一个大型合集，建议按需安装子集；安装前先阅读具体技能的 `SKILL.md`。

## 与当前已安装技能的重叠

| Scientific Agent Skills 能力 | 当前已安装技能 | 重叠程度 |
| --- | --- | --- |
| 学术写作、阅读、润色、引用、审稿 | `nature-writing`, `nature-polishing`, `nature-reader`, `nature-citation`, `nature-reviewer`, `nature-response`, `paper-spine` | 高 |
| 文献检索与参考文献工作流 | `nature-academic-search`, `nature-citation`, `paper-spine-citation` | 高 |
| 科研绘图与可视化 | `nature-figure`, `spreadsheets` | 中 |
| 文档、PDF、幻灯片和表格输出 | `docx`, `documents`, `pdf`, `presentations`, `spreadsheets` | 低到中 |
| 通用科研自动化 | `paper-spine`, `agently-mail`, 本地 Codex skills | 中 |

## 为什么保留

- 它是目前公开仓库中覆盖面很广的科研类 Agent Skills 合集。
- 它覆盖了本地 Nature / PaperSpine 技能没有完全覆盖的方向，尤其是生物信息学、化学信息学、药物发现、科学数据库、科研 Python 包和实验室/科研平台集成。
- 即使不安装，也适合作为科研技能参考库。
- 它遵循开放 Agent Skills 约定，并明确列出兼容 Codex。

## 注意事项

- Skill 可能会指导 agent 安装包、运行代码、调用外部 API 或修改文件。
- README 本身也建议安装前先审查技能。
- 用于正式科研时，需要独立核验结果和数据来源。

## 备注

- License：MIT。
- 检查时 stars：约 29.8k。
- 最后检查日期：2026-07-02。
