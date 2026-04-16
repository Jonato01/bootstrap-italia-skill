# Bootstrap Italia Plugin for Claude Code

[Claude Code](https://claude.ai/claude-code) plugin for building Italian Public Administration websites using **[Bootstrap Italia](https://italia.github.io/bootstrap-italia/) v2.x** — the official design system based on Bootstrap 5.2.3.

## Installation

### As a plugin (recommended)

Add to your `.claude/settings.json`:

```json
{
  "enabledPlugins": {
    "bootstrap-italia@bootstrap-italia": true
  },
  "extraKnownMarketplaces": {
    "bootstrap-italia": {
      "source": {
        "source": "github",
        "repo": "Jonato01/bootstrap-italia-skill"
      }
    }
  }
}
```

### As a standalone skill

```bash
npx skills add Jonato01/bootstrap-italia-skill@bootstrap-italia -g -y
```

## What it does

This plugin gives Claude Code deep knowledge of Bootstrap Italia, enabling it to:

- Generate PA-compliant HTML/CSS/JS using correct Bootstrap Italia components
- Follow Italian PA design guidelines (Linee guida di design per i siti internet e i servizi digitali della PA)
- Use the institutional color palette (Blu Italia `#0066CC`, semantic colors, neutral grays)
- Implement proper PA page structure (slim header, center header, navbar, footer)
- Apply Titillium Web typography and Bootstrap Italia icon set
- Ensure WCAG 2.1 AA accessibility and GDPR compliance (Cookiebar)

## Coverage

| Category | Count | Examples |
|----------|-------|---------|
| **Components** | 27 | Accordion, Alert, Avatar, Card, Callout, Hero, Steppers, Timeline... |
| **Form elements** | 11 | Input, Date picker, Time picker, Autocomplete, Upload, Transfer... |
| **Navigation** | 13 | Header, Footer, Megamenu, Sidebar, BottomNav, Breadcrumbs... |
| **Layout & Spacing** | 13 | Grid, Flex, Display, Borders, Shadows, Sizing... |
| **Utilities** | 3 | Colors, Custom colors, Icons |

## Plugin Structure

```
bootstrap-italia-skill/
├── .claude-plugin/
│   └── plugin.json              # Plugin metadata
├── skills/
│   └── bootstrap-italia/
│       └── SKILL.md             # Main skill with all patterns & components
└── README.md
```

## Usage

After installing, invoke when working on Bootstrap Italia projects:

- Type `/bootstrap-italia` in Claude Code
- Or ask: *"usa bootstrap italia per questo componente"*

### Example prompts

- *"Crea un header PA completo con slim header, center header e navbar"*
- *"Genera un form di contatto con validazione usando Bootstrap Italia"*
- *"Implementa una card con avatar, badge e callout"*
- *"Crea la struttura base di un sito PA con header e footer istituzionale"*

## Based on

- [Bootstrap Italia](https://italia.github.io/bootstrap-italia/) v2.18.0
- [Bootstrap](https://getbootstrap.com/) 5.2.3
- [Designers Italia](https://designers.italia.it/) — Design system del Paese

## Contributing

PRs welcome! If you want to add more component examples or improve patterns, feel free to contribute.

## License

MIT
