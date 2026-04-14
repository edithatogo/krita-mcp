# Krita CLI — Parent Project Context

## What is this?

**Krita CLI** is the parent project that orchestrates and manages the `krita-mcp` subproject. This repository serves as:

1. **Integration Layer** — Coordinates the Krita MCP/CLI tool development
2. **Conductor Hub** — Central project management using Conductor methodology
3. **Release Manager** — Handles packaging, distribution, and cross-project workflows

## Relationship to krita-mcp

The `krita-mcp/` subfolder contains the core application:
- **Krita MCP Server** — FastMCP server for AI agents
- **Krita CLI** — Command-line interface for programmatic painting
- **Krita Plugin** — Python plugin inside Krita

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
    └── tests/                    ← Test suite
```

## Goals

- Manage feature development across CLI, MCP server, and Krita plugin
- Coordinate releases and versioning
- Ensure quality gates (test coverage, type safety, linting)
- Track progress on Phase 11+ features

## Users

- **Project Maintainers** — Using Conductor to manage development
- **Contributors** — Following track-based workflows
- **Release Engineers** — Coordinating cross-component releases
