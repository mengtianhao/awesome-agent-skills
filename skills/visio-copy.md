# Visio Copy

[中文](visio-copy_zh.md)

## Links

- Repository: https://github.com/zwj276765037-lab/Visio-copy
- Chinese README: https://github.com/zwj276765037-lab/Visio-copy/blob/main/README.md
- English README: https://github.com/zwj276765037-lab/Visio-copy/blob/main/README.en.md
- Skill file: https://github.com/zwj276765037-lab/Visio-copy/blob/main/SKILL.md

## Summary

`visio-copy` is a Codex skill for redrawing raster technical diagrams into Microsoft Visio as editable native Visio shapes. It targets paper figures, PPT diagrams, screenshots, architecture diagrams, hardware module diagrams, data-flow diagrams, chip/package diagrams, flowcharts, and complex mixed table-plus-architecture figures.

The key constraint is that the final `.vsdx` should be made of editable Visio shapes, connectors, text, layers, tables, polygons, and native primitives. It explicitly forbids delivering pasted screenshots, source-image underlays, raster tracing, SVG/PDF trace imports, or auto-vectorized copies as the final artifact.

## Main Capabilities

- Recreate a reference PNG/JPG/PDF diagram as editable Visio shapes.
- Use source image pixel coordinates as the placement system.
- Automate Visio through PowerShell COM scripts.
- Provide reusable manual drawing primitives for boxes, connectors, tables, block arrows, hatched regions, polygons, 2.5D/3D stacked diagrams, chiplet grids, and logic/electrical symbols.
- Analyze colors and component regions with Python tools.
- Export Visio previews and compare local crops against the reference image.
- Preserve text transparency, layer order, arrow endpoint avoidance, repeated-grid alignment, and dense hardware figure structure.

## Repository Structure

Important files and folders:

- `SKILL.md`: Codex skill instructions
- `scripts/visio_copy_manual_primitives.ps1`: reusable Visio drawing primitives
- `scripts/visio_manual_redraw_scaffold.ps1`: manual redraw scaffold
- `scripts/analyze_reference_style.py`: color and structure analysis
- `scripts/extract_color_components.py`: rough color-region bbox extraction
- `scripts/crop_compare.py`: reference/preview crop comparison
- `scripts/export_visio_png_safe.ps1`: safer Visio PNG export wrapper
- `scripts/finalize_visio_copy_page.ps1`: cleanup for final Visio page
- `references/redraw-checklist.md`: redraw checklist
- `references/stacked-grid-mode.md`: stacked/grid diagram guidance

## Requirements

- Windows
- Microsoft Visio desktop
- PowerShell
- Python 3.10+
- Python packages from `requirements.txt`

Install Python dependencies:

```powershell
python -m pip install -r requirements.txt
```

## Installation Notes

The README recommends cloning the repository directly into the Codex skills directory with the directory name `visio-copy`:

```powershell
git clone https://github.com/zwj276765037-lab/Visio-copy.git "$env:USERPROFILE\.codex\skills\visio-copy"
```

Then invoke it in Codex as:

```text
$visio-copy
```

## Workflow

1. Prepare a reference image and target `.vsdx` output path.
2. Use the scaffold or manual primitives script to create a figure-specific drawing script.
3. Map source image pixels to Visio page coordinates.
4. Draw background, outer modules, large regions, internal grids, ports, arrows, stacked structures, and details.
5. Draw text last, using transparent text by default.
6. Export `preview.png`.
7. Run local crop comparisons for key components.
8. Iterate on geometry, font size, text lane width, arrow endpoints, line weight, color, layer order, and missing elements.
9. After user confirmation, clean up temporary layers and keep the final editable vector redraw.

## Overlap With Current Installed Skills

| Visio Copy Area | Current Installed Skill(s) | Overlap |
| --- | --- | --- |
| Scientific/technical figure work | `nature-figure` | Medium |
| Visual asset generation/editing | `imagegen` | Low-medium |
| Document/PPT figure reproduction | `presentations`, `docx`, `pdf` | Low |
| Windows app automation | Computer Use capability | Operational dependency, not a replacement |

## Why Keep It

- It fills a specific gap: editable Visio reproduction of technical raster diagrams.
- It is stricter than generic image tracing because it requires native Visio shapes.
- It includes practical safeguards for Visio export, text wrapping, crop auditing, and dense hardware diagrams.
- It is especially useful for architecture, hardware, chiplet, NoC, memory, table, and flowchart figures.

## Notes

- License: MIT.
- GitHub snapshot when checked: about 23 stars and 4 forks.
- Last checked: 2026-06-19.

