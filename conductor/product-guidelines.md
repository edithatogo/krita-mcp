# Krita CLI — Product Guidelines

## Documentation Standards

- All conductor files use Markdown with clear heading hierarchy
- Track IDs follow format: `shortname_YYYYMMDD`
- Commit messages use [Conventional Commits](https://www.conventionalcommits.org/)
- Cross-references between parent and child conductor files should use relative paths

## Code Quality

- Inherited from `krita-mcp/conductor/workflow.md`
- Test coverage: 95% minimum
- Type coverage: 100% required
- Linting: ruff strict mode
- Formatting: ruff format

## Release Process

1. All tracks in current milestone must be completed
2. Run full test suite in `krita-mcp/`
3. Bump version using semantic-release
4. Update parent project tracks.md with completion status
5. Create release notes summarizing completed tracks

## Cross-Project Coordination

- Parent tracks.md references high-level milestones
- Child `krita-mcp/conductor/tracks.md` tracks implementation details
- When completing a parent track, verify corresponding child tracks are also complete
- Use `/conductor:implement` to work on specific tracks

## Quality Gates

- [ ] All tests passing in krita-mcp
- [ ] Coverage threshold met
- [ ] Type checks passing
- [ ] No linting errors
- [ ] Manual testing completed (if applicable)
- [ ] Documentation updated
