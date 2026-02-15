# sexy-claude-themes

Community theme store for [sexy-claude](https://github.com/MagnusPladsen/sexy-claude-code) (sc) — a beautiful terminal wrapper for Claude Code.

## Installing Themes

Copy any `.toml` file from `themes/` into your local themes directory:

```bash
# macOS / Linux
mkdir -p ~/.config/sexy-claude/themes
cp themes/nord.toml ~/.config/sexy-claude/themes/
```

Then switch themes in sexy-claude with `Ctrl+T` or set it in `~/.config/sexy-claude/config.toml`:

```toml
theme = "nord"
```

## Bundled Themes

| Theme | Preview Colors |
|-------|---------------|
| [Catppuccin Mocha](themes/catppuccin-mocha.toml) | Purple / Pink / Blue |
| [Dracula](themes/dracula.toml) | Purple / Pink / Cyan |
| [Gruvbox Dark](themes/gruvbox-dark.toml) | Orange / Yellow / Green |
| [Kanagawa](themes/kanagawa.toml) | Blue / Red / Green |
| [Monokai Pro](themes/monokai-pro.toml) | Yellow / Pink / Green |
| [Nord](themes/nord.toml) | Blue / Cyan / Teal |
| [One Dark](themes/one-dark.toml) | Blue / Purple / Cyan |
| [Rose Pine](themes/rose-pine.toml) | Pink / Gold / Rose |
| [Solarized Dark](themes/solarized-dark.toml) | Blue / Yellow / Cyan |
| [Tokyo Night](themes/tokyo-night.toml) | Blue / Purple / Cyan |

## Contributing a Theme

1. Fork this repo
2. Copy `TEMPLATE.toml` to `themes/your-theme-name.toml`
3. Fill in all color values (hex format: `#rrggbb`)
4. Open a PR

### Theme Structure

Every theme is a TOML file with a `name` and `[colors]` section containing **20 required color fields**:

```toml
name = "Your Theme Name"

[colors]
# Base
background = "#1e1e2e"
foreground = "#cdd6f4"
surface = "#313244"
overlay = "#45475a"

# Accent
primary = "#cba6f7"
secondary = "#89b4fa"
accent = "#f5c2e7"

# Semantic
success = "#a6e3a1"
warning = "#f9e2af"
error = "#f38ba8"
info = "#89dceb"

# Border
border = "#585b70"
border_focused = "#cba6f7"

# Status bar
status_bg = "#181825"
status_fg = "#a6adc8"

# Input
input_bg = "#313244"
input_fg = "#cdd6f4"
input_cursor = "#f5e0dc"
input_placeholder = "#6c7086"
```

### Color Guidelines

- **background** — Main app background (dark themes: `#1e-#2e`, light themes: `#f0-#ff`)
- **surface** — Slightly elevated from background (popups, input area)
- **overlay** — Highlighted rows in menus
- **primary** — Main accent (app name, headings, selected items)
- **secondary** / **accent** — Supporting accent colors
- **success** / **warning** / **error** / **info** — Semantic colors for status indicators
- **border** / **border_focused** — Unfocused and focused border colors
- All colors must be 6-digit hex: `#rrggbb`

## License

MIT
