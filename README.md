# agent-hub

My agent setup in one place: own skills, hooks and MCP servers as small
[APM](https://microsoft.github.io/apm/) packages, plus a pinned catalog of
vendor skills. Each project picks what it needs in its own `apm.yml`, and APM
writes it to the right place for Claude Code and Codex.

Requires APM 0.35+ (`brew install apm`).

## Packages

| Package | Contains | Targets |
| --- | --- | --- |
| `git-workflow` | `ship-pr`, `implement-issue`, `implement-in-worktree` | Claude, Codex |
| `planning` | `describe-feature`, `grill-one-by-one` | Claude, Codex |
| `hooks-fallow-gate` | Blocks `git commit`/`push` when `fallow audit` fails | Claude |
| `hooks-oxc-format` | Runs `oxlint --fix` and `oxfmt` on every edited file | Claude |
| `mcp-context7` | Context7 MCP server (needs `CONTEXT7_API_KEY`) | Claude, Codex |

Vendor skills from other authors are listed in [VENDOR.md](VENDOR.md).

The root [apm.yml](apm.yml) contains all vendor skills and the MCP server. Depend
on the whole repo to get everything, or copy single lines from it:

```yaml
dependencies:
  apm:
    - emalgholzad/agent-hub#v1.1.0
```

## Use it in a project

```yaml
# apm.yml
name: my-project
version: 0.1.0
targets: [claude, codex]
dependencies:
  apm:
    # own packages: pick the ones you need
    - emalgholzad/agent-hub/packages/git-workflow#v1.0.0
    - emalgholzad/agent-hub/packages/mcp-context7#v1.0.0
    # only some skills of a package
    - git: https://github.com/emalgholzad/agent-hub.git
      path: packages/planning
      ref: v1.0.0
      skills: [describe-feature]
    # vendor skills: copy lines from VENDOR.md
    - mattpocock/skills/skills/engineering/tdd#4ae2317ddb22b046e26455e4f9c9b3aaaf62212d
```

```bash
apm install
```

Commit `apm.yml`, `apm.lock.yaml` and the generated `.claude/`, `.codex/`,
`.agents/` folders. `apm_modules/` stays gitignored.

The `skills:` filter works on a package's own skills only, not on vendor
skills, so reference vendor skills directly as above.

## Update

Change a skill, hook or MCP here only, never inside a project. Then tag a
release (`v1.1.0`) and, in each project:

```bash
apm outdated
apm update
```

## Add something

- **Skill:** `packages/<package>/.apm/skills/<name>/SKILL.md`
- **Hook:** `packages/<package>/.apm/hooks/<name>.json` (plus scripts in `scripts/`, referenced as `${PLUGIN_ROOT}/scripts/...`)
- **MCP server:** `dependencies.mcp` in a package's `apm.yml`
- **Vendor skill:** add a row to `VENDOR.md`

## Not included

The Supabase MCP server stays in each project, because its URL contains the
project ID.

## License

[MIT](LICENSE)
