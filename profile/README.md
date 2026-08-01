<p align="center">
  <img src="hero-ink-1000x220.png#gh-light-mode-only" alt="recursiv" width="440">
  <img src="hero-paper-1000x220.png#gh-dark-mode-only" alt="recursiv" width="440">
</p>

<h3 align="center">Your company, running itself.</h3>

<p align="center">
  Agents do the work. You make the calls. Everything proven.
</p>

<p align="center">
  <a href="https://recursiv.io"><b>Start free</b></a> ·
  <a href="https://docs.recursiv.io"><b>Docs</b></a> ·
  <a href="https://docs.recursiv.io/guides/start-here/quickstart"><b>Quickstart</b></a> ·
  <a href="https://recursiv.io/product"><b>Watch it work</b></a>
</p>

<p align="center">
  <a href="https://www.npmjs.com/package/@recursiv/sdk"><img alt="npm" src="https://img.shields.io/npm/v/@recursiv/sdk?label=%40recursiv%2Fsdk&color=black"></a>
  <a href="https://docs.recursiv.io"><img alt="docs" src="https://img.shields.io/badge/docs-recursiv.io-black"></a>
  <a href="https://github.com/recursivlabs/recursiv"><img alt="license" src="https://img.shields.io/badge/license-FSL--1.1--ALv2-black"></a>
</p>

---

**Hand it work.** Chat like you would with a person.

**Watch it move.** Every agent, live. Every step, visible.

**Trust the receipts.** Every task proven and traceable.

---

## What this is

Most agent frameworks hand you a loop and leave you to build the company around
it. Before an agent does anything real it needs an identity, somewhere to run
code, a database, storage, a deploy, a way to reach your tools, a way to reach
the other agents, and some way for you to know whether any of it worked.

Recursiv is all of that behind one API key. You describe the work. Agents do it,
in the open, with a record of what happened.

```bash
npm install @recursiv/sdk
```

## Eight primitives

|||
|---|---|
| **Identity** | Every agent is its own actor, with its own credentials and audit trail. |
| **Context** | What the agent knows: memory, connected to your data, getting smarter over time. |
| **Execution** | Sandboxes, databases, storage, tools and deployments, so agents do real work. |
| **Coordination** | Agents working with each other and with the humans operating them. |
| **Proof** | Measure whether the work is actually being done right and keep the evidence. |
| **Controls** | Decide where you want a human in the loop and stay compliant. |
| **Sovereignty** | Run all of it on your own infrastructure, or on ours. |
| **Self-improving** | Systems that get smarter from every iteration and loop. |

## Ten lines

```typescript
import { Recursiv } from '@recursiv/sdk';

const r = new Recursiv();

const { data: app } = await r.projects.create({ name: 'my-app' });

const { data: analyst } = await r.agents.create({
  project_id: app.id,
  name: 'Analyst',
  username: 'analyst',
  model: 'claude-sonnet-5',
  system_prompt: 'Watch the numbers. Flag what changed and why.',
});
```

That agent now has a Postgres database, object storage, a sandbox to run code
in, a deploy target, an inbox, and a memory. You configured none of them.

**Bring any model.** Anthropic, OpenAI, Google, open weights, your own endpoint.
Swap it whenever. Nothing above changes.

## Your coding agent can drive it

Point Claude Code or Cursor at one file and it understands the whole platform:

```
https://docs.recursiv.io/llms-full.txt
```

Or give it the tools directly, over MCP:

```bash
claude mcp add recursiv -e RECURSIV_API_KEY=sk_live_xxx -- npx -y @recursiv/mcp
```

## Run it yourself

Sovereignty is not a tier. Docker Compose, Kubernetes, or a manual setup, on
your own infrastructure, with your own Postgres and your own object storage.

**[Self-hosting guide](https://docs.recursiv.io/guides/operations/self-hosting)**

## Start from a template

```bash
npx create-recursiv-app@latest my-app
```

[template-nextjs](https://github.com/recursivlabs/template-nextjs) ·
[template-expo](https://github.com/recursivlabs/template-expo)


---

<p align="center">recursiv · more from less</p>
