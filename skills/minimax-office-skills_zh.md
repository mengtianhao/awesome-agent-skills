# MiniMax Office Skills

[English](minimax-office-skills.md)

## 链接

- 仓库：https://github.com/freeskychenjun/MiniMax-Office-skills
- README 中提到的上游仓库：https://github.com/MiniMax-AI/skills
- 中文 README：https://github.com/freeskychenjun/MiniMax-Office-skills/blob/main/README_zh.md
- Codex 安装说明：https://github.com/freeskychenjun/MiniMax-Office-skills/blob/main/.codex/INSTALL.md

## 简介

MiniMax Office Skills 是一组面向 AI coding agent 的技能集合。它覆盖 Office 文档处理、前端与全栈开发、移动端开发、Shader、GIF 表情制作，以及基于 MiniMax API 的多模态媒体生成。

## 可用技能

| 技能 | 用途 |
| --- | --- |
| `frontend-dev` | 前端与全栈 UI 开发、动画、MiniMax API 媒体资产 |
| `fullstack-dev` | 后端架构与前后端集成 |
| `android-native-dev` | Android 原生开发 |
| `ios-application-dev` | iOS 应用开发 |
| `shader-dev` | GLSL Shader 工作流 |
| `gif-sticker-maker` | 动态 GIF 表情制作 |
| `minimax-pdf` | PDF 创建、填写和重排 |
| `pptx-generator` | PowerPoint 生成、编辑和读取 |
| `minimax-xlsx` | Excel/表格创建、分析、编辑和校验 |
| `minimax-docx` | DOCX/Word 创建、编辑和排版 |
| `minimax-multimodal-toolkit` | MiniMax API 语音、音乐、视频、图像和 FFmpeg 工作流 |

## 安装说明

README 描述的 Codex 安装方式是：克隆上游 skills 仓库，然后把其中的 `skills` 目录链接到 agent 的 skills 目录。

Windows 下使用 junction：

```powershell
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.agents\skills"
cmd /c mklink /J "$env:USERPROFILE\.agents\skills\minimax-skills" "$env:USERPROFILE\.codex\minimax-skills\skills"
```

安装后需要重启 Codex。

## 与当前已安装技能的重叠

| MiniMax 技能 | 当前已安装技能 | 重叠程度 |
| --- | --- | --- |
| `minimax-docx` | `docx`, `documents` | 高 |
| `minimax-pdf` | `pdf` | 高 |
| `pptx-generator` | `presentations`, `nature-paper2ppt` | 高 |
| `minimax-xlsx` | `spreadsheets` | 高 |
| `frontend-dev` | `frontend-design` | 中高 |
| `gif-sticker-maker` | `imagegen` | 部分 |
| `minimax-multimodal-toolkit` | `imagegen` | 部分 |

## 可能值得额外保留的部分

- `minimax-multimodal-toolkit`
- `gif-sticker-maker`
- `shader-dev`
- `android-native-dev`
- `ios-application-dev`

## 备注

- 文档技能名是 `minimax-docx`，不是 `minimax-doc`。
- 最后检查日期：2026-06-19
