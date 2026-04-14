# Krita CLI

Parent project for the **Krita MCP** ecosystem — a SOTA CLI + MCP server for programmatic painting in Krita.

## Overview

This repository orchestrates and manages the `krita-mcp` subproject, which provides:

- **CLI Interface**: `krita stroke --points 100,100 200,200` — direct command-line control
- **MCP Server**: FastMCP server for AI agents (Claude, etc.) to paint programmatically
- **Krita Plugin**: Python plugin inside Krita that executes paint commands

Both CLI and MCP talk to the Krita plugin via HTTP on localhost:5678.

## Quick Start

### Prerequisites

- Python 3.12+
- [uv](https://github.com/astral-sh/uv) package manager
- Krita (with Python plugin support)

### Setup

```bash
# Navigate to the core application
cd krita-mcp

# Install dependencies
uv sync

# Install Krita plugin (copy to Krita's plugin directory)
# Windows: %APPDATA%\krita\pykrita\
# Linux: ~/.local/share/krita/pykrita/
# macOS: ~/Library/Application Support/krita/pykrita/

# Enable plugin in Krita: Settings → Configure Krita → Python Plugin Manager

# Run CLI
uv run krita health

# Run MCP server
uv run python -m krita_mcp.server
```

## Project Structure

```
krita-cli/
├── conductor/                    ← Project management (this project)
│   ├── product.md                ← Parent project purpose
│   ├── tech-stack.md             ← Technology stack
│   ├── workflow.md               ← Development workflow
│   ├── tracks.md                 ← High-level milestones
│   └── tracks/                   ← Track implementation plans
└── krita-mcp/                    ← Core Application
    ├── conductor/                ← Subproject conductor
    ├── src/
    │   ├── krita_client/         ← Core client library
    │   ├── krita_mcp/            ← MCP server
    │   └── krita_cli/            ← CLI interface
    ├── krita-plugin/             ← Krita plugin
    └── tests/                    ← Test suite
```

## Development

### Using Conductor

This project uses the Conductor methodology for spec-driven development:

- **Tracks** represent high-level units of work (features, bug fixes, etc.)
- Each track has a `plan.md` with phased tasks
- All work follows TDD workflow: write tests → implement → verify coverage
- Track progress in `conductor/tracks.md`

### Commands

```bash
# View project status
/conductor:status

# Implement next track
/conductor:implement

# Implement specific track
/conductor:implement "<track_description>"
```

### Quality Gates

- Test coverage: >80%
- Type coverage: 100% (enforced by ty)
- Linting: ruff strict mode
- All CI checks must pass before merging

## Documentation

- [Product Definition](conductor/product.md)
- [Tech Stack](conductor/tech-stack.md)
- [Workflow](conductor/workflow.md)
- [Tracks Registry](conductor/tracks.md)

## License

MIT License — see [LICENSE](krita-mcp/LICENSE)
