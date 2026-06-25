# LawConnect Navigator (Claude Code plugin)

This plugin turns Claude Code into the **LawConnect Navigator** — it walks you through a legal
situation end to end and, when you're ready, connects you with a matched Australian lawyer.

It ships two things:

- A native **`legal-advisor` skill** (`skills/legal-advisor/SKILL.md`) that Claude loads
  automatically whenever you describe a legal issue.
- A bundled **MCP server** (`.mcp.json`) that exposes the LawConnect lawyer-matching tools
  (`mcp__lawconnect__*`), wired to the production endpoint.

## Install

Via the marketplace (inside Claude Code):

```
/plugin marketplace add law-connect/lawconnect-claude-plugin
/plugin install lawconnect@lawconnect
```

Or from a local copy of this directory:

```sh
claude --plugin-dir ./lawconnect
```

Once installed, the skill is available as `/lawconnect:legal-advisor` and the matching tools
appear as `mcp__lawconnect__*`.

## What it talks to

This build is wired to LawConnect's production MCP endpoint,
`https://mcp.ask.lawconnect.com/consumer` (see `.mcp.json`). The endpoint is an open
lead-generation funnel protected at the edge.

## Generated — do not edit

This directory is generated and kept in sync automatically. Do not hand-edit files here — changes
are overwritten when the plugin is regenerated.
