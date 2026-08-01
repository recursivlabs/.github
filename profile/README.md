# recursiv

### Your company, running itself.

Agents do the work. You make the calls. Everything proven.

**[Start free](https://recursiv.io) · [Docs](https://docs.recursiv.io) · [Quickstart](https://docs.recursiv.io/guides/start-here/quickstart)**

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

| | |
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

## Start from a template

```bash
npx create-recursiv-app@latest my-app
```

[template-nextjs](https://github.com/recursivlabs/template-nextjs) ·
[template-expo](https://github.com/recursivlabs/template-expo)

---

recursiv · more from less
