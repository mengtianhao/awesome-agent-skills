# MiniMax Office Skills

## Links

- Repository: https://github.com/freeskychenjun/MiniMax-Office-skills
- Upstream repository mentioned by README: https://github.com/MiniMax-AI/skills
- Chinese README: https://github.com/freeskychenjun/MiniMax-Office-skills/blob/main/README_zh.md
- Codex install guide: https://github.com/freeskychenjun/MiniMax-Office-skills/blob/main/.codex/INSTALL.md

## Summary

MiniMax Office Skills is a skill collection for AI coding agents. It includes Office document workflows, frontend and full-stack development guidance, mobile development, shader work, GIF sticker creation, and MiniMax API-powered multimodal media generation.

## Available Skills

| Skill | Purpose |
| --- | --- |
| `frontend-dev` | Frontend and full-stack UI development, animation, MiniMax API media assets |
| `fullstack-dev` | Backend architecture and frontend-backend integration |
| `android-native-dev` | Android native development |
| `ios-application-dev` | iOS development |
| `shader-dev` | GLSL shader workflows |
| `gif-sticker-maker` | Animated GIF sticker generation |
| `minimax-pdf` | PDF creation, filling, and reformatting |
| `pptx-generator` | PowerPoint generation, editing, and reading |
| `minimax-xlsx` | Excel and spreadsheet creation, analysis, editing, and validation |
| `minimax-docx` | DOCX and Word creation, editing, and formatting |
| `minimax-multimodal-toolkit` | MiniMax API voice, music, video, image, and FFmpeg workflows |

## Installation Notes

The README describes installing for Codex by cloning the upstream skills repository and linking its `skills` directory into the agent skills directory.

Windows installation uses a junction:

```powershell
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.agents\skills"
cmd /c mklink /J "$env:USERPROFILE\.agents\skills\minimax-skills" "$env:USERPROFILE\.codex\minimax-skills\skills"
```

Restart Codex after installation.

## Overlap With Current Installed Skills

| MiniMax Skill | Current Installed Skill(s) | Overlap |
| --- | --- | --- |
| `minimax-docx` | `docx`, `documents` | High |
| `minimax-pdf` | `pdf` | High |
| `pptx-generator` | `presentations`, `nature-paper2ppt` | High |
| `minimax-xlsx` | `spreadsheets` | High |
| `frontend-dev` | `frontend-design` | Medium-high |
| `gif-sticker-maker` | `imagegen` | Partial |
| `minimax-multimodal-toolkit` | `imagegen` | Partial |

## Potentially Useful Additions

- `minimax-multimodal-toolkit`
- `gif-sticker-maker`
- `shader-dev`
- `android-native-dev`
- `ios-application-dev`

## Notes

- The document skill is named `minimax-docx`, not `minimax-doc`.
- Last checked: 2026-06-19

