# Track: Parent Project Setup & krita-mcp Integration

## Overview

Establish the parent project conductor structure for `krita-cli` and integrate it with the existing `krita-mcp` subproject.

## Goals

1. Create parent-level conductor files that reference and manage the krita-mcp subproject
2. Establish cross-project workflow for managing tracks and releases
3. Document the relationship between parent and child projects
4. Ensure all conductor tooling works correctly at both levels

## Scope

- Parent conductor/ directory creation
- Integration with krita-mcp/conductor/
- Track registry at parent level
- Cross-reference documentation

## Out of Scope

- Changes to krita-mcp implementation
- New feature development
- Refactoring of existing krita-mcp code

## Success Criteria

- [ ] Parent conductor/ structure created
- [ ] All core conductor files present (product.md, tech-stack.md, workflow.md, index.md)
- [ ] tracks.md references krita-mcp tracks
- [ ] `/conductor:implement` works for parent project
- [ ] Clear documentation of parent-child relationship
