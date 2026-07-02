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

## 与我的研究方向相关的技能

我的研究方向是医学自然语言处理和医学信号分析，重点包括 ECG 和医学图像。该仓库中最相关的技能如下：

| Skill | 相关方向 | 说明 |
| --- | --- | --- |
| `transformers` | 医学 NLP | Hugging Face Transformers 工作流，包括模型加载、tokenizer、pipeline、文本生成、微调和多模态模型使用。适合临床文本分类、命名实体识别、医学报告理解和医学大模型实验。 |
| `pyhealth` | 医疗机器学习、EHR、信号、影像 | 面向临床深度学习的工具包，覆盖 EHR、生理信号和医学影像数据集。适合 MIMIC-III/IV、eICU、OMOP、EHRShot、SleepEDF、ChestXray14、死亡/再入院预测、ICD 编码、睡眠分期、EEG 事件和医学编码映射。 |
| `neurokit2` | ECG 与生理信号 | 生理信号处理工具包，支持 ECG、PPG、EEG、EDA、RSP、EMG 和 EOG。直接适合 ECG 清洗、R 峰检测、ECG delineation、HRV、信号质量评估和多模态生理信号分析。 |
| `aeon` | 时间序列机器学习 | 时间序列机器学习工具包，支持分类、回归、聚类、预测、异常检测、分割和相似性搜索。适合 ECG beat/record 分类、时序表型建模和生理时间序列基准实验。 |
| `timesfm-forecasting` | 时间序列预测 | Google TimesFM 基础模型的零样本时间序列预测。适合生命体征、传感器流和其他单变量医学时间序列的探索性预测。 |
| `pydicom` | 医学影像 | Python DICOM 工具，用于读取、写入、匿名化、转换和处理 CT、MRI、X-ray、超声、PET 等医学影像数据。是放射影像管线的核心基础技能。 |
| `imaging-data-commons` | 医学影像数据集 | 查询和下载 NCI Imaging Data Commons 的公开癌症影像数据。适合放射影像 AI 数据发现、队列构建、元数据筛选和数据访问溯源。 |
| `pathml` | 计算病理 | 全切片病理图像分析工具，支持 WSI、染色归一化、细胞核分割、组织图、多重成像和病理机器学习工作流。 |
| `histolab` | 病理图像预处理 | 轻量级 WSI 预处理工具，支持组织检测、tile 提取和 H&E 切片准备。适合快速构建病理图像数据集。 |
| `clinical-reports` | 临床 NLP 与报告 | 面向放射、病理、检验、病例、临床试验、SOAP、出院小结等临床报告的模板和校验。适合理解报告结构，以及构建报告生成/信息抽取流程。 |
| `clinical-decision-support` | 临床证据与队列 | 支持队列分析、biomarker 分层、结局分析、生存曲线和循证治疗推荐报告。适合围绕 NLP 或影像特征做临床研究分析。 |
| `bids` | 生物医学数据组织 | Brain Imaging Data Structure 支持 MRI、EEG、MEG、iEEG、PET、显微成像、NIRS、EMG 等数据。适合组织多模态信号和影像研究数据。 |
| `scikit-learn` | 传统机器学习基线 | 传统机器学习 pipeline、预处理、模型评估、监督/无监督学习。适合 ECG 特征、radiomics 特征和临床文本 embedding 的强基线。 |
| `pytorch-lightning` | 深度学习训练 | 结构化 PyTorch 训练框架，支持可扩展实验、日志、callback、分布式训练和可复现实验代码。适合 NLP、ECG 和影像模型训练。 |
| `shap` | 医学 AI 可解释性 | 基于 SHAP 的模型解释，包括特征重要性、偏差分析和预测解释。适合临床模型可解释性和结果报告。 |
| `statistical-analysis` | 医学研究统计 | 假设检验、前提假设检查、功效分析和学术报告。适合医学 AI 评估研究。 |
| `statsmodels` | 统计建模 | 回归、GLM、混合模型、ARIMA、诊断和统计推断。适合临床结局建模和时间序列/统计分析。 |
| `database-lookup` | 生物医学数据库 | 从有文档的公共数据库进行可复现检索，包括 ClinicalTrials、FDA、WHO、ClinVar、OMIM、PubChem 等生物医学和监管资源。 |
| `literature-review` | 文献综述 | 面向 PubMed、arXiv、bioRxiv、Semantic Scholar 等来源的系统综述工作流。适合医学 NLP、ECG AI 和医学影像综述。 |
| `venue-templates` | 医学论文准备 | 面向期刊、会议、海报和基金的模板与格式指南，包括医学期刊风格和 NIH 相关材料。 |

建议优先检查的短名单：`pyhealth`、`neurokit2`、`pydicom`、`transformers`、`aeon`、`imaging-data-commons`、`pathml`、`histolab`、`shap`、`literature-review`。

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
