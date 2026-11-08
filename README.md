# Agent Hub

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
    - emalgholzad/agent-hub#v2.1.0
```

```bash
apm install
```

Or copy only the lines you need from [`apm.yml`](apm.yml) into your project's
`apm.yml`.

## Skills (55)

### [tt-a1i/archify](https://github.com/tt-a1i/archify)

| Skill | Description |
| --- | --- |
| `archify` | Create validated architecture, sequence, data-flow and other diagrams as standalone HTML. |

### [mattpocock/skills](https://github.com/mattpocock/skills)

| Skill | Description |
| --- | --- |
| `ask-matt` | Ask which skill or flow fits your situation. |
| `chief-of-staff` | Pursue a long-running goal in a single session by co-ordinating subagents. |
| `claude-handoff` | Hand the current conversation off to a fresh background agent that picks up the work immediately. |
| `code-review` | Review the changes since a fixed point (commit, branch, tag, or merge-base) along two axes: Standards… |
| `codebase-design` | Vocabulary for designing deep modules and finding deepening opportunities. |
| `diagnosing-bugs` | Diagnosis loop for hard bugs and performance regressions. |
| `domain-modeling` | Build and sharpen a project's domain model, glossary and ADRs. |
| `git-guardrails-claude-code` | Set up Claude Code hooks to block dangerous git commands (push, reset --hard, clean, branch -D, etc.)… |
| `grill-me` | A relentless interview to sharpen a plan or design. |
| `grill-with-docs` | A relentless interview to sharpen a plan or design, which also creates docs (ADR's and glossary) as we go. |
| `grilling` | Grill the user about a plan, decision or idea. |
| `handoff` | Compact the current conversation into a handoff document for another agent to pick up. |
| `implement` | Implement a piece of work based on a spec or set of tickets. |
| `implement-spec` | Implement the result of /to-spec and /to-tickets in code. |
| `improve-codebase-architecture` | Scan a codebase for deepening opportunities, present them as a visual HTML report, then grill through… |
| `loop-me` | Grill me about specs for the workflows I want to build, within this workspace. |
| `migrate-to-shoehorn` | Migrate test files from `as` type assertions to @total-typescript/shoehorn. |
| `pr` | Write a PR body. |
| `prototype` | Build a throwaway prototype to answer a design question. |
| `research` | Investigate a question against primary sources and save the findings as Markdown. |
| `retro` | Conduct a retrospective on a coding session. |
| `scaffold-exercises` | Create exercise directory structures with sections, problems, solutions, and explainers that pass linting. |
| `setup-matt-pocock-skills` | Configure this repo for the engineering skills: set up its issue tracker, triage label vocabulary, and… |
| `setup-pre-commit` | Set up Husky pre-commit hooks with lint-staged (Prettier), type checking, and tests in the current repo. |
| `setup-ts-deep-modules` | Wire dependency-cruiser into a TypeScript repo so each package is a deep module, with implementation… |
| `tdd` | Build features or fix bugs test-first (red-green-refactor). |
| `teach` | Teach the user a new skill or concept, within this workspace. |
| `to-questionnaire` | Turn a decision you can't fully answer into a questionnaire for someone else to fill in. |
| `to-spec` | Turn the current conversation into a spec and publish it to the project issue tracker: no interview, just… |
| `to-tickets` | Break a plan, spec, or the current conversation into a set of tracer-bullet tickets, each declaring its… |
| `triage` | Move issues and external PRs through a state machine of triage roles, categorise, verify, grill if needed,… |
| `wait-what` | Re-pitch your last message when it did not land. |
| `wayfinder` | Plan a huge chunk of work (more than one agent session can hold) as a shared map of decision tickets on… |
| `wizard` | Generate an interactive bash wizard that walks a human through steps only they can perform. |
| `writing-beats` | Writing, exploit; assemble raw material into a journey of beats, grounding each term before a beat leans… |
| `writing-for-agents` | Write documents for agents: skills, AGENTS.md, CLAUDE.md. |
| `writing-fragments` | Writing, explore: mine raw fragments, no structure yet. |
| `writing-shape` | Writing, exploit: shape raw material into an article, paragraph by paragraph. |

### [latent-spaces/brag](https://github.com/latent-spaces/brag)

| Skill | Description |
| --- | --- |
| `brag-slim` | Turn a project directory or a website URL into a short, shareable launch video with music, motion, and… |

### [netresearch/context7-skill](https://github.com/netresearch/context7-skill)

| Skill | Description |
| --- | --- |
| `context7` | Look up library docs through the Context7 REST API when the MCP is unavailable. |

### [fallow-rs/fallow-skills](https://github.com/fallow-rs/fallow-skills)

| Skill | Description |
| --- | --- |
| `fallow` | Static analysis for TypeScript and JavaScript: risk, dead code, duplication, boundaries. |
| `fallow-review` | Review AI-generated or human-written code changes with fallow's graph-grounded review brief. |

### [vercel-labs/skills](https://github.com/vercel-labs/skills)

| Skill | Description |
| --- | --- |
| `find-skills` | Find and install agent skills for a task. |

### [anthropics/skills](https://github.com/anthropics/skills)

| Skill | Description |
| --- | --- |
| `frontend-design` | Guidance for distinctive, intentional visual design. |

### [szkocot/andrej-karpathy-skills](https://github.com/szkocot/andrej-karpathy-skills)

| Skill | Description |
| --- | --- |
| `karpathy-guidelines` | Behavioral guidelines to reduce common LLM coding mistakes. |

### [humanlayer/skills](https://github.com/humanlayer/skills)

| Skill | Description |
| --- | --- |
| `show-me` | Help the user understand the current topic visually with concise diagrams, code-shape sketches, and… |
| `visual-pr` | Create or update a PR with a concise, reviewer-focused description. |

### [supabase/agent-skills](https://github.com/supabase/agent-skills)

| Skill | Description |
| --- | --- |
| `supabase` | Supabase tasks: database, auth, edge functions, realtime, storage, CLI and debugging. |
| `supabase-postgres-best-practices` | Postgres best practices for schemas, migrations, RLS, indexes and queries. |

### [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills)

| Skill | Description |
| --- | --- |
| `vercel-react-best-practices` | React and Next.js performance optimization guidelines from Vercel Engineering. |

### [lemomo-ai/lemo-opuscar](https://github.com/lemomo-ai/lemo-opuscar)

| Skill | Description |
| --- | --- |
| `lemo-opuscar` | Direct and produce a short film made entirely in code, in one of 66 styles. |

### [Panniantong/Agent-Reach](https://github.com/Panniantong/Agent-Reach)

| Skill | Description |
| --- | --- |
| `agent-reach` | Read-only search and reading across Twitter/X, Reddit, YouTube, GitHub and more. |

### [wheresryan22/anatomy](https://github.com/wheresryan22/anatomy)

| Skill | Description |
| --- | --- |
| `anatomy` | Build detailed, interactive isometric SVG figures that explain a technical idea as a physical object. |

### [heydamir/unslop](https://github.com/heydamir/unslop)

| Skill | Description |
| --- | --- |
| `unslop` | Turn vibecoded, AI-looking UI into a designed interface with its own character. |

## MCP servers

| Server | Notes |
| --- | --- |
| `context7` | Library documentation. Set `CONTEXT7_API_KEY` in your environment. |
| `vercel` | Vercel projects, deployments and logs. Sign in with OAuth on first use. |
| `supabase` | Supabase, account level (no project set). Sign in with OAuth on first use. |
| `figma` | Figma designs. Sign in with OAuth on first use. |

## Notes

- `lemo-opuscar` clones its library to `~/lemo-opuscar` and runs `npm install` the first time you use it.
- `agent-reach` needs the `agent-reach` CLI. Install it from GitHub following its
  [install guide](https://raw.githubusercontent.com/Panniantong/Agent-Reach/main/docs/install.md),
  not from PyPI: the PyPI package with that name is a different project.
- `anatomy` is about 27 MB, because it ships its examples.
- `supabase` here has no project set. A project that needs one defines its own
  `supabase` server with `project_ref` in its own config.
- `unslop` is CC BY 4.0: keep its credit if you copy or adapt it.

## Update

Bump the commit pins in `apm.yml`, tag a release, then in each project:

```bash
apm outdated
apm update
```

## License

[MIT](LICENSE)
