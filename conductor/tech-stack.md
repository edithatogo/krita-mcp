# Krita CLI — Tech Stack

## Parent Project

This parent project (`krita-cli/`) is primarily for project management and coordination. It uses:

- **Conductor Framework** — Project management methodology
- **Markdown** — Documentation format
- **Git** — Version control

## Child Project (krita-mcp)

The core application tech stack is defined in `krita-mcp/conductor/tech-stack.md`:

### Key Technologies
- **Python >=3.12** — Primary language
- **uv** — Package manager
- **pydantic v2** — Data validation
- **fastmcp** — MCP server framework
- **typer** — CLI framework
- **httpx** — HTTP client

### Dev Tooling
- **ruff** — Linting + formatting
- **ty** — Type checking
- **pytest** — Testing
- **hypothesis** — Property-based testing
- **pre-commit** — Git hooks

## Communication

- Parent ↔ Child: Relative file paths within repository
- External: PyPI package distribution, GitHub releases

## Reference

For detailed tech stack information, see: `krita-mcp/conductor/tech-stack.md`
