# Bootstrap Italia Skill for Claude Code

[Claude Code](https://claude.ai/claude-code) skill for building Italian Public Administration websites using **[Bootstrap Italia](https://italia.github.io/bootstrap-italia/) v2.x** — the official design system based on Bootstrap 5.2.3.

## Installation

```bash
npx skills add Jonato01/bootstrap-italia-skill@bootstrap-italia -g -y
```

## What it does

This skill gives Claude Code deep knowledge of Bootstrap Italia, enabling it to:

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

## Usage

After installing, invoke manually when working on Bootstrap Italia projects:

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

## License

MIT
