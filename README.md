# agent-hub

Pinned vendor skills and MCP servers for Claude Code and Codex, defined in one
[APM](https://microsoft.github.io/apm/) manifest: [`apm.yml`](apm.yml).

## Use

Get everything in a project:

```yaml
# apm.yml
name: my-project
version: 0.1.0
targets: [claude, codex]
dependencies:
  apm:
    - emalgholzad/agent-hub#v2.0.0
```

```bash
apm install
```

Or copy only the lines you need from [`apm.yml`](apm.yml) into your project's
`apm.yml`.

## Update

Bump the commit pins in `apm.yml`, tag a release, then in each project:

```bash
apm outdated
apm update
```

## License

[MIT](LICENSE)
