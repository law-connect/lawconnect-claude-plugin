# LawConnect Navigator — Claude Code plugin

This repository is the **public, installable mirror** of the LawConnect Navigator
[Claude Code plugin](https://code.claude.com/docs/en/plugins). It turns Claude Code into the
**LawConnect Navigator** — it walks you through a legal situation end to end and, when you're ready,
connects you with a matched Australian lawyer.

It ships two things:

- A native **`legal-advisor` skill** (`lawconnect/skills/legal-advisor/SKILL.md`) that Claude loads
  automatically whenever you describe a legal issue.
- A bundled **MCP server** (`lawconnect/.mcp.json`) that exposes the LawConnect lawyer-matching tools
  (`mcp__lawconnect__*`), wired to the production endpoint.

## Install

Inside Claude Code:

```
/plugin marketplace add law-connect/lawconnect-claude-plugin
/plugin install lawconnect@lawconnect
```

Once installed, the skill is available as `/lawconnect:legal-advisor` and the matching tools appear
as `mcp__lawconnect__*`.

## What it talks to

This build is wired to LawConnect's production MCP endpoint,
`https://mcp.ask.lawconnect.com/consumer` (see `lawconnect/.mcp.json`) — an open lead-generation
funnel protected at the edge.

## Not legal advice

LawConnect Navigator is **not a lawyer and does not give legal advice**. It helps you prepare for,
and connect with, one. **Australia-focused.**

## Generated mirror — do not edit by hand

This repository is **generated** and synced by automation from the
[`lawconnect-mono`](https://github.com/law-connect/lawconnect-mono) monorepo
(`apps/claude-plugin` generator + the `apps/mcp-consumer-server` skill, the single source of truth).
Hand edits here are overwritten on the next sync — change the source in the monorepo and regenerate.
