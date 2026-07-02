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

## Relevant Skills for My Research

My current research interests are medical natural language processing and medical signal analysis, especially ECG and medical imaging. The most relevant skills in this repository are:

| Skill | Relevance | Description |
| --- | --- | --- |
| `transformers` | Medical NLP | Hugging Face Transformers workflows for loading models, tokenizers, pipelines, text generation, fine-tuning, and multimodal model use. Useful for clinical text classification, named entity recognition, medical report understanding, and medical LLM experiments. |
| `pyhealth` | Healthcare ML, EHR, signal, imaging | Clinical deep learning toolkit covering EHR, physiological signal, and medical imaging datasets. Relevant for MIMIC-III/IV, eICU, OMOP, EHRShot, SleepEDF, ChestXray14, mortality/readmission prediction, ICD coding, sleep staging, EEG events, and medical code mapping. |
| `neurokit2` | ECG and biosignals | Biosignal processing toolkit for ECG, PPG, EEG, EDA, RSP, EMG, and EOG. Directly relevant for ECG cleaning, R-peak detection, ECG delineation, heart-rate variability, signal quality assessment, and multimodal physiological signal analysis. |
| `aeon` | Time-series ML | Time-series machine learning toolkit for classification, regression, clustering, forecasting, anomaly detection, segmentation, and similarity search. Useful for ECG beat/record classification, temporal phenotype modeling, and physiological time-series benchmarks. |
| `timesfm-forecasting` | Time-series forecasting | Zero-shot time-series forecasting with Google's TimesFM foundation model. Useful for exploratory forecasting of vitals, sensor streams, and other univariate medical time series. |
| `pydicom` | Medical imaging | Python DICOM toolkit for reading, writing, anonymizing, converting, and processing CT, MRI, X-ray, ultrasound, PET, and other medical imaging data. Core utility for radiology image pipelines. |
| `imaging-data-commons` | Medical imaging datasets | Query and download public cancer imaging data from NCI Imaging Data Commons. Useful for radiology AI dataset discovery, cohort construction, metadata filtering, and data access provenance. |
| `pathml` | Computational pathology | Full pathology image analysis toolkit for whole-slide images, stain normalization, nucleus segmentation, tissue graphs, multiplex imaging, and pathology ML workflows. |
| `histolab` | Pathology preprocessing | Lightweight WSI preprocessing toolkit for tissue detection, tile extraction, and H&E slide preparation. Useful for quick pathology dataset preparation. |
| `clinical-reports` | Clinical NLP and reports | Templates and validation for radiology, pathology, lab, case, trial, SOAP, discharge, and other clinical reports. Useful for understanding report structure and building report generation/extraction workflows. |
| `clinical-decision-support` | Clinical evidence and cohorts | Cohort analysis, biomarker stratification, outcomes analysis, survival curves, and evidence-based treatment recommendation reports. Useful for clinical research analytics around NLP or imaging-derived features. |
| `bids` | Biomedical data organization | Brain Imaging Data Structure support for MRI, EEG, MEG, iEEG, PET, microscopy, NIRS, EMG, and related biomedical datasets. Useful when organizing multimodal signal and imaging studies. |
| `scikit-learn` | Classical ML baseline | Classical ML pipelines, preprocessing, model evaluation, supervised/unsupervised learning. Useful for strong baselines on ECG features, radiomics features, and clinical text embeddings. |
| `pytorch-lightning` | Deep learning training | Structured PyTorch training framework for scalable experiments, logging, callbacks, distributed training, and reproducible model code. Useful for NLP, ECG, and imaging model training. |
| `shap` | Medical AI explainability | SHAP-based model interpretation for feature importance, bias analysis, and prediction explanation. Useful for clinical model interpretability and reporting. |
| `statistical-analysis` | Research statistics | Guided hypothesis testing, assumption checks, power analysis, and academic reporting. Useful for medical AI evaluation studies. |
| `statsmodels` | Statistical modeling | Regression, GLM, mixed models, ARIMA, diagnostics, and inferential modeling. Useful for clinical outcome modeling and time-series/statistical analysis. |
| `database-lookup` | Biomedical databases | Reproducible retrieval from documented public databases, including biomedical and regulatory sources such as ClinicalTrials, FDA, WHO, ClinVar, OMIM, PubChem, and related resources. |
| `literature-review` | Literature review | Systematic literature review workflows across PubMed, arXiv, bioRxiv, Semantic Scholar, and other sources. Useful for medical NLP, ECG AI, and medical imaging review work. |
| `venue-templates` | Medical manuscript preparation | Templates and formatting guidance for journals, conferences, posters, and grants, including medical journal styles and NIH-related materials. |

Recommended shortlist to inspect first: `pyhealth`, `neurokit2`, `pydicom`, `transformers`, `aeon`, `imaging-data-commons`, `pathml`, `histolab`, `shap`, and `literature-review`.

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
