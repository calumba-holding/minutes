# Reproducible Release Notes

Minutes now has a repeatable release-note generator at
[scripts/release_notes.sh](/Users/silverbook/Sites/minutes/scripts/release_notes.sh).

The goal is not fully automatic prose. The goal is a reproducible draft that
always includes:

- `What changed`
- `Who should care`
- `CLI / MCP / desktop impact`
- `Breaking changes or migration notes`
- `Known issues`

That keeps every release aligned with
[docs/RELEASE-CHANNELS.md](/Users/silverbook/Sites/minutes/docs/RELEASE-CHANNELS.md).

## How it works

The script accepts:

```bash
scripts/release_notes.sh <from-ref> <to-ref> [channel]
```

Examples:

```bash
scripts/release_notes.sh v0.1.0 HEAD stable
scripts/release_notes.sh v0.2.0-beta.1 HEAD preview
scripts/release_notes.sh v0.2.0 v0.2.1 stable
```

The script:

- walks commits in the selected git range
- groups them by surface based on touched paths
- emits a markdown draft with stable sections
- calls out CLI, desktop, MCP, and shared-engine impact separately

## Path mapping

Current buckets:

- `crates/cli/` → CLI
- `tauri/` → desktop
- `crates/mcp/` → MCP / agent integrations
- `crates/core/` → shared engine
- everything else → other repo changes

This is intentionally simple and auditable. If the repo adds a new
distribution-relevant surface later, update the script rather than asking
maintainers to remember it manually.

## Workflow integration

The macOS release workflow writes a generated release-note draft before
publishing the GitHub Release. Maintainers can still refine the generated text,
but the structure is no longer optional.

## Maintainer expectations

Treat the generated output as a draft, not gospel.

Before publishing:

1. read the generated notes end to end
2. replace generic lines where a more specific user-facing explanation is needed
3. add any known issues or migration notes that git history cannot infer
4. make sure preview releases explicitly say what is experimental

The release note is complete when a desktop user, a CLI user, and an MCP user
can each tell whether they should care about the release without reading the
full commit history.
