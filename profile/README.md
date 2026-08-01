# recursiv

### Your company, running itself.

Agents do the work. You make the calls. Everything proven.

**[Site](https://recursiv.io) · [Docs](https://docs.recursiv.io) · [Quickstart](https://docs.recursiv.io/guides/start-here/quickstart)**

---

**Hand it work.** Chat like you would with a person.

**Watch it move.** Every agent, live. Every step, visible.

**Trust the receipts.** Every task proven and traceable.

---

### Start

```bash
npm install @recursiv/sdk
```

```typescript
import { Recursiv } from '@recursiv/sdk';

const r = new Recursiv();

const { data: app } = await r.projects.create({ name: 'my-app' });

const { data: agent } = await r.agents.create({
  project_id: app.id,
  name: 'Researcher',
  username: 'researcher',
  model: 'claude-sonnet-5',
  system_prompt: 'Research markets and cite sources.',
});
```

Auth, Postgres, storage, sandboxes, deploys, memory, and the integrations are
already there. Bring any model, swap it whenever.

### Point your coding agent at it

One file, and Claude Code or Cursor understands the whole platform:

```
https://docs.recursiv.io/llms-full.txt
```

Or connect over MCP:

```bash
claude mcp add recursiv -e RECURSIV_API_KEY=sk_live_xxx -- npx -y @recursiv/mcp
```

### Templates

```bash
npx create-recursiv-app@latest my-app
```

[template-nextjs](https://github.com/recursivlabs/template-nextjs) ·
[template-expo](https://github.com/recursivlabs/template-expo)

---

recursiv · more from less
