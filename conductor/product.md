# Krita CLI — Parent Project Context

## What is this?

**Krita CLI** is the parent project that orchestrates and manages the `krita-mcp` subproject. This repository serves as:

1. **Integration Layer** — Coordinates the Krita MCP/CLI tool development.
2. **Conductor Hub** — Central project management using Conductor methodology.
3. **Release Manager** — Handles packaging, distribution, and cross-project workflows.

## Relationship to krita-mcp

The `krita-mcp/` subfolder contains the core application:
- **Krita MCP Server** — FastMCP server for AI agents (40+ tools).
- **Krita CLI** — Command-line interface for programmatic painting (grouped subcommands).
- **Krita Plugin** — High-performance Python plugin inside Krita.

This parent project manages tracks, milestones, and releases for the entire ecosystem.

## Architecture

```
krita-cli/ (Parent Project - This)
├── conductor/                    ← Project management
│   ├── product.md                ← This file
│   ├── tracks.md                 ← Cross-project tracks
│   └── tracks/                   ← Track plans
└── krita-mcp/                    ← Core Application (child project)
    ├── conductor/                ← Subproject conductor
    ├── src/                      ← Application source
    └── tests/                    ← Test suite (95.00% coverage)
```

## Project Status: Release 1.0.0 Ready

The project has achieved all core development goals:
- **Feature Complete**: Full suite of painting, selection, and session tools.
- **Integrated**: Seamless CLI and MCP interfaces sharing a core client.
- **Verified**: Comprehensive test suite with 680+ tests and mandatory 95% coverage.
- **Secure**: Built-in path sanitization and resource limits.

## Users

- **AI agents** (Claude, etc.) via MCP protocol.
- **Developers/Artists** via CLI for scripting and automation.
- **Integrators** using the `krita_client` library.
