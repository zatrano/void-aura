# Void Aurora

A deep dark VS Code theme with a violet-black canvas and warm syntax spectrum.

The color system flows cold to warm: violet keywords → periwinkle functions → sage strings → peach numbers → amber types. Every token has a semantic reason for its color — not decoration, but signal.

---

## Color Palette

### Canvas layers

| Role | Hex |
|------|-----|
| Canvas (window bg) | `#080810` |
| Editor background | `#0e0e1a` |
| Panel / widget | `#13131f` |
| Sidebar | `#0b0b16` |
| Hover / selection | `#21213a` |

### Syntax spectrum

| Token | Color | Hex |
|-------|-------|-----|
| Keyword | Violet | `#c792ea` |
| Function | Periwinkle | `#82aaff` |
| String | Sage | `#c3e88d` |
| Number | Peach | `#f78c6c` |
| Type | Amber | `#ffcb6b` |
| Operator | Cyan | `#89ddff` |
| Parameter | Rose | `#f07178` |
| Comment | Dim violet | `#4a4570` |

### UI accent

| Role | Hex |
|------|-----|
| Primary accent | `#7b68d4` |
| Selection | `#7b68d432` |
| Active line | `#c792ea08` |
| Cursor | `#c792ea` |

---

## Language support

Full semantic and TextMate token coverage for:

- **JavaScript / TypeScript** — JSX, TSX, decorators, generics, template literals
- **Python** — decorators, f-strings, dunder methods, type hints
- **Rust** — lifetimes, macros, traits, unsafe, attributes
- **Go** — built-ins, package imports
- **HTML / CSS / SCSS** — pseudo-classes, custom properties, at-rules
- **JSON / YAML** — keys, values, anchors
- **Markdown** — headings, bold, italic, code, blockquotes
- **Shell / Bash**
- **GraphQL**

---

## Installation

### From VSIX (recommended for local use)

```bash
git clone https://github.com/your-username/void-aurora.git
cd void-aurora
npm install
npx vsce package
code --install-extension void-aurora-1.0.0.vsix
```

### Manual

1. Copy this folder into `~/.vscode/extensions/void-aurora`
2. Restart VS Code
3. Open **Command Palette** → **Preferences: Color Theme** → select **Void Aurora**

### From VS Code Marketplace

Search **Void Aurora** in the Extensions panel (`Ctrl+Shift+X` / `Cmd+Shift+X`).

---

## Recommended settings

```jsonc
{
  // Font — JetBrains Mono pairs perfectly with this theme
  "editor.fontFamily": "'JetBrains Mono', 'Cascadia Code', monospace",
  "editor.fontSize": 13.5,
  "editor.lineHeight": 1.7,
  "editor.fontLigatures": true,
  "editor.fontWeight": "300",

  // Cursor
  "editor.cursorStyle": "line",
  "editor.cursorBlinking": "phase",
  "editor.cursorWidth": 2,
  "editor.cursorSmoothCaretAnimation": "on",

  // Indent guides
  "editor.guides.indentation": true,
  "editor.guides.bracketPairs": "active",

  // Bracket colorization
  "editor.bracketPairColorization.enabled": true,
  "editor.bracketPairColorization.independentColorPoolPerBracketType": true,

  // Minimap
  "editor.minimap.enabled": true,
  "editor.minimap.renderCharacters": false,
  "editor.minimap.scale": 2,
  "editor.minimap.showSlider": "always",

  // Whitespace
  "editor.renderWhitespace": "boundary",
  "editor.renderLineHighlight": "gutter",

  // Smooth scroll
  "editor.smoothScrolling": true,
  "workbench.list.smoothScrolling": true,
  "terminal.integrated.smoothScrolling": true,

  // Semantic tokens (enables richer coloring)
  "editor.semanticHighlighting.enabled": true,

  // Workbench
  "workbench.colorTheme": "Void Aurora",
  "workbench.iconTheme": "material-icon-theme"
}
```

---

## Building & publishing

```bash
# Install tooling
npm install

# Package as .vsix
npm run package

# Publish to marketplace (requires a Personal Access Token)
npm run publish
```

To publish, you need:
1. A [Visual Studio Marketplace publisher account](https://marketplace.visualstudio.com/manage)
2. Update `publisher` in `package.json` to your publisher ID
3. A Personal Access Token from [Azure DevOps](https://dev.azure.com)

---

## Credits

Syntax palette inspired by [Material Theme](https://github.com/material-theme/vsc-material-theme) and [Moonlight](https://github.com/atomiks/moonlight-vscode-theme). Canvas depth and UI layer system designed from scratch.

---

## License

MIT © Your Name
