# Visio Copy

[English](visio-copy.md)

## 链接

- 仓库：https://github.com/zwj276765037-lab/Visio-copy
- 中文 README：https://github.com/zwj276765037-lab/Visio-copy/blob/main/README.md
- 英文 README：https://github.com/zwj276765037-lab/Visio-copy/blob/main/README.en.md
- Skill 文件：https://github.com/zwj276765037-lab/Visio-copy/blob/main/SKILL.md

## 简介

`visio-copy` 是一个 Codex skill，用于把 raster 技术图重画到 Microsoft Visio 中，并尽量生成可编辑的原生 Visio shapes。它适合论文图、PPT 图、截图、体系结构图、硬件模块图、数据流图、芯片/封装示意图、流程图，以及表格和架构混合的复杂图。

它的核心约束是：最终 `.vsdx` 应由可编辑的 Visio shapes、connector、文字、图层、表格、polygon 和原生 primitive 组成。它明确禁止把贴图、源图底图、raster trace、SVG/PDF trace import 或自动矢量化结果当成最终交付。

## 主要能力

- 将 PNG/JPG/PDF 参考图重画为可编辑 Visio shapes。
- 使用源图像像素坐标作为统一放置坐标系。
- 通过 PowerShell COM 脚本自动绘制 Visio。
- 提供可复用的手工绘图 primitive，用于模块框、connector、表格、粗箭头、hatched 区域、polygon、2.5D/3D 堆叠图、chiplet 网格和逻辑/电路符号。
- 使用 Python 工具分析颜色和组件区域。
- 导出 Visio 预览图，并对参考图和预览图做局部 crop 对比。
- 强调透明文字、图层顺序、箭头端点避让、重复网格对齐和密集硬件图结构。

## 仓库结构

重要文件和目录：

- `SKILL.md`：Codex skill 指令
- `scripts/visio_copy_manual_primitives.ps1`：可复用 Visio 绘图 primitive
- `scripts/visio_manual_redraw_scaffold.ps1`：手工重画 scaffold
- `scripts/analyze_reference_style.py`：颜色和结构分析
- `scripts/extract_color_components.py`：粗略颜色区域 bbox 提取
- `scripts/crop_compare.py`：参考图/预览图局部 crop 对比
- `scripts/export_visio_png_safe.ps1`：更安全的 Visio PNG 导出 wrapper
- `scripts/finalize_visio_copy_page.ps1`：最终 Visio 页面清理
- `references/redraw-checklist.md`：重画检查清单
- `references/stacked-grid-mode.md`：堆叠/网格图绘制指导

## 环境要求

- Windows
- Microsoft Visio 桌面版
- PowerShell
- Python 3.10+
- `requirements.txt` 中的 Python 包

安装 Python 依赖：

```powershell
python -m pip install -r requirements.txt
```

## 安装说明

README 建议将仓库直接 clone 到 Codex skills 目录，并保持目录名为 `visio-copy`：

```powershell
git clone https://github.com/zwj276765037-lab/Visio-copy.git "$env:USERPROFILE\.codex\skills\visio-copy"
```

然后在 Codex 中调用：

```text
$visio-copy
```

## 基本流程

1. 准备参考图片和目标 `.vsdx` 输出路径。
2. 使用 scaffold 或 manual primitives 脚本创建项目专用绘图脚本。
3. 将源图像像素坐标映射到 Visio 页面坐标。
4. 先绘制背景、外层模块和大区域，再绘制内部网格、端口、箭头、堆叠结构和细节。
5. 最后绘制文字，普通文字默认透明。
6. 导出 `preview.png`。
7. 对关键组件做局部 crop 对比。
8. 迭代修复几何、字体大小、文字框宽度、箭头端点、线宽、颜色、图层顺序和漏画元素。
9. 用户确认后，清理临时图层，只保留最终可编辑矢量 redraw。

## 与当前已安装技能的重叠

| Visio Copy 能力 | 当前已安装技能 | 重叠程度 |
| --- | --- | --- |
| 科研/技术图处理 | `nature-figure` | 中 |
| 视觉资产生成/编辑 | `imagegen` | 低到中 |
| 文档/PPT 图形复现 | `presentations`, `docx`, `pdf` | 低 |
| Windows 应用自动化 | Computer Use 能力 | 操作依赖，不是替代 |

## 为什么保留

- 它补上了一个很具体的空白：将技术 raster 图复刻成可编辑 Visio 文件。
- 它比普通图像 trace 更严格，因为最终必须是原生 Visio shapes。
- 它包含 Visio 导出、文字换行、局部 crop 审计和密集硬件图绘制的实用防线。
- 它特别适合体系结构、硬件、chiplet、NoC、memory、表格和流程图类图形。

## 备注

- License：MIT。
- 检查时 GitHub 约 23 stars、4 forks。
- 最后检查日期：2026-06-19。

