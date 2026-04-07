# VS Code Dark Modern for Zed

A faithful, pixel-perfect port of VS Code's built-in **Dark Modern** theme to Zed.

## Why another port?

Existing ports ([vscode_dark_modern.zed](https://github.com/kevcamel/vscode_dark_modern.zed), [vscode-dark-polished](https://github.com/y7ya-com/vscode-dark-polished)) each deviate from the source in different ways. This theme was built by cross-referencing the actual VS Code source files (`dark_modern.json`, `dark_plus.json`, `dark_vs.json`) to get every value right.

### Issues with existing ports

**kevcamel/vscode_dark_modern.zed**
- Active line uses opaque `#282828` instead of translucent `#FFFFFF0A`
- Many UI keys left null (no button, input, badge, or tab border styling)
- `surface.background` set to `#79797966` (gray overlay) instead of `#181818`
- `punctuation.bracket` uses `#CCCCCC` instead of VS Code's `#808080`
- Missing tokens: `enum`, `label`, `link_text`, `link_uri`, `variant`, `title`, `hint`, `predictive`

**y7ya-com/vscode-dark-polished**
- Editor foreground shifted from `#CCCCCC` to `#D4D4D4`
- `text` set to `#FFFFFF` (pure white, way too bright)
- All keywords use `#C586C0` — doesn't differentiate declaration (`#569CD6`) vs control flow (`#C586C0`)
- Terminal ANSI palette replaced with syntax highlight colors (not VS Code's actual palette)
- Selection uses `#0078D43D` instead of VS Code's `#264F78`
- Constructor uses function color `#DCDCAA` instead of `#569CD6`
- Terminal background uses `#1F1F1F` instead of `#181818`
- Warning color uses `#BB8009` instead of `#CCA700`

## Install

Copy or symlink this directory into your Zed extensions folder, or install from the Zed extension registry once published.

## Source of truth

All colors were derived from the VS Code repository:
- [`dark_modern.json`](https://github.com/microsoft/vscode/blob/main/extensions/theme-defaults/themes/dark_modern.json) — workbench colors
- [`dark_plus.json`](https://github.com/microsoft/vscode/blob/main/extensions/theme-defaults/themes/dark_plus.json) — syntax token overrides
- [`dark_vs.json`](https://github.com/microsoft/vscode/blob/main/extensions/theme-defaults/themes/dark_vs.json) — base syntax tokens
- Terminal ANSI colors from VS Code's `terminalColorRegistry.ts` defaults
