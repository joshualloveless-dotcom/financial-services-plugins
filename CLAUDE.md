# Financial Services Plugins

This is a marketplace of Claude Cowork plugins for financial services professionals. Each subdirectory is a standalone plugin.

## Repository Structure

```
├── financial-analysis/        # Core financial modeling and analysis (install first)
├── investment-banking/        # Investment banking productivity
├── equity-research/           # Equity research workflows
├── private-equity/            # Private equity deal sourcing and workflow
├── wealth-management/         # Wealth management and financial advisory
├── partner-built/
│   ├── lseg/                  # LSEG financial data and analytics
│   └── spglobal/              # S&P Global financial data and analytics
├── claude-in-office/          # Microsoft 365 Claude Office add-in deployment
└── .claude-plugin/
    └── marketplace.json       # Marketplace manifest (registers all plugins)
```

## Plugin Structure

Each plugin follows this layout:
```
plugin-name/
├── .claude-plugin/plugin.json   # Plugin manifest (name, description, version)
├── commands/                    # Slash commands (.md files)
├── skills/                      # Knowledge files for specific tasks
├── hooks/                       # Event-driven automation
├── mcp/                         # MCP server integrations
└── .claude/                     # User settings (*.local.md)
```

## Key Files

- `marketplace.json`: Marketplace manifest - registers all plugins with source paths
- `plugin.json`: Plugin metadata - name, description, version, and component discovery settings
- `commands/*.md`: Slash commands invoked as `/plugin:command-name`
- `skills/*/SKILL.md`: Detailed knowledge and workflows for specific tasks
- `*.local.md`: User-specific configuration (gitignored)
- `mcp-categories.json`: Canonical MCP category definitions shared across plugins

## Development Workflow

1. Edit markdown files directly - changes take effect immediately
2. Test commands with `/plugin:command-name` syntax
3. Skills are invoked automatically when their trigger conditions match
