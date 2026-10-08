# Dubai Company Setup — Dubai Setup Index plugin

Dubai and UAE company setup data for Claude, ChatGPT, Cursor and Grok: free
zone packages and prices, the Dubai mainland licence route, business
activities by free zone, and setup cost estimates.

[Dubai Setup Index](https://dubaisetupindex.com) publishes sourced, dated
guides to 40+ UAE free zones and the Dubai mainland (DET) route. Every figure
carries its source and the date it was checked. Facts that are not published
are marked as such and never estimated, and cost estimates list what they
leave out instead of hiding it in a total.

This plugin connects your AI assistant to that data over MCP and adds skills
that tell it how to quote the figures correctly.

## What you can ask

- "What does an IFZA licence with one visa cost, and what isn't included?"
- "Which UAE free zones can license an accounting and bookkeeping business?"
- "Free zone or Dubai mainland for a software company that needs two visas?"
- "Compare IFZA and Ajman Free Zone for a company with two visas."
- "I'm a UK founder. Which documents should I prepare?"

## What is in here

| Path | |
| --- | --- |
| `.claude-plugin/plugin.json` | Claude plugin manifest |
| `.claude-plugin/marketplace.json` | Marketplace entry, so this repo can be added as a Claude Code marketplace |
| `.mcp.json` | The remote MCP server, `https://dubaisetupindex.com/api/mcp` |
| `skills/` | Five skills: get started, choose a setup route, estimate a setup cost, find an activity, cite a figure |
| `plugin.json`, `mcp.json` | The same plugin in the [Agent Plugins](https://agent-plugins.org) format, for ChatGPT, Codex and other clients |
| `.cursor-plugin/` | Cursor manifest and marketplace entry |
| `.grok-plugin/` | Grok manifest |
| `assets/` | Icon |

The skills are plain Markdown instructions. The plugin ships no scripts, hooks
or executables and installs no packages.

## Install

**Claude Code**

```bash
claude plugin marketplace add dubaisetupindex/dubaisetupindex-plugin
claude plugin install dubai-setup-index@dubai-setup-index
```

**Cursor** — add this repository from the Cursor plugin marketplace, or point
Cursor at it as a plugin repository.

**Grok** — `grok` loads it from `~/.grok/plugins/`, or pass the cloned
repository with `--plugin-dir`.

**ChatGPT and Codex** — use the root `plugin.json` and `mcp.json`.

**Any MCP client, without the skills**

```bash
claude mcp add --transport http dubai-setup-index https://dubaisetupindex.com/api/mcp
```

On claude.ai, add `https://dubaisetupindex.com/api/mcp` as a custom connector.

## Sign-in and the data it sends

Connecting opens a browser sign-in to a free Dubai Setup Index account (OAuth
2.1): an email address and a sign-in link or code, no password and no API key.
The plugin requests read access to published setup data. Every tool is
read-only.

The plugin talks to one server, `dubaisetupindex.com`. When the assistant calls
a tool, the tool's arguments, such as a free zone, an activity, a visa count or
a rent figure, are sent to that server. Dubai Setup Index records each tool
call in its product analytics (PostHog): the tool name, its arguments, timing,
errors, the AI client's name and your account identifier. It does not record
its answers. Nothing else from your conversation or your machine is sent. See
the [privacy policy](https://dubaisetupindex.com/privacy).

## Scope

UAE only. Published prices and fees change; confirm with the authority before
you file or pay. The plugin cannot register a company, submit applications or
take payments, and it does not give legal, tax or immigration advice.

## Support

[dubaisetupindex.com/contact](https://dubaisetupindex.com/contact) or
hello@dubaisetupindex.com.
