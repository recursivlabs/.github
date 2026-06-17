# Recursiv

### Build, run and govern autonomous agents.

Everything you need in one SDK to build, run and govern autonomous agents.
Connected to your data, tools and systems. Model agnostic, so you bring any
model and swap it anytime.

**[Website](https://recursiv.io) · [Docs](https://docs.recursiv.io) · [Quickstart](https://docs.recursiv.io/guides/start-here/quickstart)**

---

**Build** the whole backend in one SDK: agents, databases, storage, sandboxes,
auth, deploys, and hundreds of data and tool integrations.
**Run** them in production: orchestration, schedules, memory, learning.
**Govern** what they do: scoped identity, tool approvals, audit, self-evaluation,
self-host.

### For your coding agent

Point Claude Code, Cursor, or any agent at one file and it understands the whole
platform:

```
https://docs.recursiv.io/llms-full.txt
```

Or connect over MCP:

```bash
claude mcp add recursiv -e RECURSIV_API_KEY=sk_live_xxx -- npx -y @recursiv/mcp
```

### Built on Recursiv

- [evolve](https://github.com/recursivlabs/evolve): a social network for AI agents, built autonomously by a Recursiv agent swarm
- [minds](https://github.com/recursivlabs/minds): an open source social network with a decade of users, rebuilt on Recursiv
- [run](https://github.com/recursivlabs/run): autonomous businesses that run while you sleep
- [ticker](https://github.com/recursivlabs/ticker): the AI workspace for investor relations
- [research](https://github.com/recursivlabs/research): the Cost-to-Done model leaderboard
- [spark-lab](https://github.com/recursivlabs/spark-lab): a workbench for measuring agentic control and trust

### Start building

```bash
npm install @recursiv/sdk
```

```typescript
import { Recursiv } from '@recursiv/sdk';

const r = new Recursiv();
const { data: project } = await r.projects.create({ name: 'my-app' });

const { data: agent } = await r.agents.create({
  project_id: project.id,
  name: 'Researcher',
  username: 'researcher',
  model: 'claude-sonnet-4-6', // any model, swap anytime
  system_prompt: 'Research markets and cite sources.',
});
```

New to Recursiv? Start with the [Quickstart](https://docs.recursiv.io/guides/start-here/quickstart).
