# Contributing to Panacea

Thanks for your interest in contributing a plugin to the Panacea marketplace!

## Submitting a Plugin

1. Fork this repository
2. Create your plugin under `plugins/<your-plugin-name>/`
3. Include a `.claude-plugin/plugin.json` manifest
4. Add a `LICENSE` file to your plugin directory
5. Open a pull request

## Plugin Structure

Your plugin directory should follow this layout:

```
plugins/your-plugin/
├── .claude-plugin/
│   └── plugin.json
├── agents/          (optional)
├── commands/        (optional)
├── hooks/           (optional)
├── skills/          (optional)
└── LICENSE
```

## Requirements

- **plugin.json** must include `name`, `version`, and `description`
- Plugin name must be lowercase, alphanumeric, and may include hyphens
- Include a `LICENSE` file (MIT recommended)
- No external dependencies that require installation steps

## Review Process

All submissions are reviewed for quality and safety before being added to the marketplace registry. Once approved, your plugin will be added to `.claude-plugin/marketplace.json` and available for installation.
