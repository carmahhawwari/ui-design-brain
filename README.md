# UI Design Brain

A Cursor skill that gives the AI agent real UI component knowledge — best practices, layout patterns, and design-system conventions for 60+ interface components — so it generates production-grade UI instead of generic output.

## What it does

When you ask Cursor to build a UI, it typically guesses at component patterns. This skill replaces guessing with a curated knowledge base sourced from [component.gallery](https://component.gallery) and enriched with:

- **Best practices** for every component (accessibility, sizing, behavior)
- **Common layouts** — proven arrangements for each pattern
- **Aliases** — so the agent recognizes components by any name
- **Design philosophy** — modern, minimal, SaaS-quality standards
- **Anti-patterns** — specific things to avoid

The result: interfaces that feel designed by a senior product designer, not assembled from a template.

## Install

### Option A — Personal skill (all projects)

```bash
# Clone into your Cursor skills directory
git clone https://github.com/YOUR_USERNAME/ui-design-brain.git \
  ~/.cursor/skills/ui-design-brain
```

### Option B — Project skill (shared with team)

```bash
# Clone into your project's .cursor/skills directory
git clone https://github.com/YOUR_USERNAME/ui-design-brain.git \
  .cursor/skills/ui-design-brain
```

### Option C — Manual

Copy the `SKILL.md` and `components.md` files into either:
- `~/.cursor/skills/ui-design-brain/` (personal)
- `.cursor/skills/ui-design-brain/` (project)

## Usage

Once installed, the skill activates automatically when you ask Cursor to build UI. You don't need to reference it explicitly.

### Examples

Just ask naturally:

```
Build a settings page with a sidebar navigation, toggle preferences, and a profile section.
```

```
Create a data table with search, filters, sortable columns, and pagination.
```

```
Design a SaaS dashboard with KPI cards, a chart area, and an activity feed sidebar.
```

The agent will automatically:
1. Identify which components your request needs
2. Look up best practices for each one
3. Apply the right design direction (SaaS, minimal, corporate, creative, or dashboard)
4. Generate production-ready code following the patterns

### Design directions

The skill includes 5 built-in style presets. You can request one explicitly:

| Preset | When to use |
|--------|-------------|
| **Modern SaaS** | Default — clean, spacious, professional |
| **Apple-level Minimal** | Ultra-clean with generous whitespace |
| **Enterprise / Corporate** | Information-dense, keyboard-navigable |
| **Creative / Portfolio** | Bold, expressive, editorial typography |
| **Data Dashboard** | Optimized for data scannability |

```
Build a pricing page with an Apple-minimal aesthetic.
```

## What's inside

```
ui-design-brain/
├── SKILL.md          # Main instructions — design philosophy, workflow, quick reference
├── components.md     # Full reference — 60 components with best practices and layouts
├── LICENSE.txt       # MIT license
└── README.md         # This file
```

### Component coverage

60 components including: Accordion, Alert, Avatar, Badge, Breadcrumbs, Button, Button group, Card, Carousel, Checkbox, Color picker, Combobox, Date input, Datepicker, Drawer, Dropdown menu, Empty state, Fieldset, File, File upload, Footer, Form, Header, Heading, Hero, Icon, Image, Label, Link, List, Modal, Navigation, Pagination, Popover, Progress bar, Progress indicator, Quote, Radio button, Rating, Rich text editor, Search input, Segmented control, Select, Separator, Skeleton, Skip link, Slider, Spinner, Stack, Stepper, Table, Tabs, Text input, Textarea, Toast, Toggle, Tooltip, Tree view, Video, Visually hidden.

## How it differs from frontend-design skills

| | Generic frontend skill | UI Design Brain |
|-|----------------------|-----------------|
| **Component knowledge** | None — relies on model training | 60 components with specific best practices |
| **Layout guidance** | General advice | Concrete layout patterns per component |
| **Anti-patterns** | Not addressed | Explicit list of things to avoid |
| **Accessibility** | Mentioned loosely | Specific per-component rules (focus trapping, ARIA, keyboard nav) |
| **Design system grounding** | Model's general knowledge | Sourced from real design systems via component.gallery |

## Contributing

PRs welcome. To add or update components:

1. Edit `components.md` — follow the existing format (name, aliases, description, best practices, common layouts)
2. If the component is commonly needed, add it to the quick reference table in `SKILL.md`
3. Keep `SKILL.md` under 500 lines

## License

MIT — see [LICENSE.txt](LICENSE.txt).

Component data sourced from [component.gallery](https://component.gallery).
