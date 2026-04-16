# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-04-15

### Added
- **MCP Server**: Full Model Context Protocol (FastMCP) implementation with 40 tools.
- **CLI Interface**: Grouped subcommands for `painting`, `layers`, `selection`, `canvas`, `session`, and `system`.
- **Selection Suite**: Comprehensive geometric (rect, ellipse, polygon) and pixel-based (color, alpha) selection tools.
- **Selection Operations**: Support for transforms (rotate/scale/move), grow/shrink, and combination (union/intersect/subtract) ops.
- **Persistence**: Ability to save/load selections as PNG masks and named channels.
- **Session Management**: Full command history logging, session replay, and batch operations with rollback/undo/redo support.
- **Security Layer**: Integrated path sanitization, resource limits (max canvas/layers), and rate limiting.
- **Core Library**: `krita_client` Python package for typed programmatic control.
- **Krita Plugin**: High-performance plugin with numpy-accelerated rendering and thread-safe HTTP IPC.
- **Quality Gates**: 95.00% test coverage and 100% type safety.

### Fixed
- Fixed race conditions in Krita plugin command queue.
- Resolved export/save timeout issues for large canvases.
- Fixed layer visibility and opacity state sync bugs.

### Performance
- Optimized stroke and shape rendering using numpy array operations.
- Improved IPC latency between CLI/MCP and Krita.

---
[1.0.0]: https://github.com/github/krita-cli/releases/tag/v1.0.0
