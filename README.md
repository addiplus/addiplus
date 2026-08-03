# Joe Smith

AI-native engineer in Seattle. I build MCP servers, agent tooling, and test harnesses for
systems that are hard to test.

Everything below is public and checkable: test counts, CI runs, registry entries, and commits
in other people's repositories.

## What is worth your time

**[vercel-deployment-mcp](https://github.com/addiplus/vercel-deployment-mcp)**
Stateless stdio MCP server, four read-only tools for observing Vercel deployments.
66 tests, CI green, MIT. Published on npm as
[`@addiplus/vercel-deployment-mcp`](https://www.npmjs.com/package/@addiplus/vercel-deployment-mcp)
and listed in the MCP registry as `io.github.addiplus/vercel-deployment-mcp`.

**[k8s-toolhive-lab](https://github.com/addiplus/k8s-toolhive-lab)**
First hands-on Kubernetes day, publicly transcribed: a single-node kind cluster, the core
vocabulary exercised against live workloads, then Stacklok's ToolHive operator running
vercel-deployment-mcp, the server above, as an MCPServer custom resource. Real MCP handshake
end to end from the host: initialize, initialized, tools/list with all 4 tools, and a tools/call
surfacing a designed dummy-token Vercel 403 as a structured MCP error. Stretch goal landed: a
second MCPServer alongside, two workloads in separate pods, each behind its own proxy Service,
one operator. A guided session with Claude Code, disclosed in the README, with full command
transcripts and unsquashed history.

**[llamacpp-batch-invariance](https://github.com/addiplus/llamacpp-batch-invariance)**
Batch-invariance verifier for llama.cpp continuous batching. Per-cell diffing, a five-verdict
output contract, and signed GREEN or RED certificates. Mock-sourced passes are non-promotable
by construction, so the gate cannot rubber-stamp itself. 138 tests across 8 files, CI green,
Apache 2.0. Ships a real Phi-4 RED divergence certificate so you can watch the gate bite.

**[registry-radar](https://github.com/addiplus/registry-radar)**
Next.js 16 App Router app for tracking npm and MCP registry packages: download sparklines,
server-paginated version history, a watchlist, markdown export, and explicit failure states
including a rate-limit banner with reset countdown and stale-while-error handling.
142 tests across 16 files, CI green, MIT. Live at https://registry-radar.vercel.app

**[mcp-cookie-auth-reference](https://github.com/addiplus/mcp-cookie-auth-reference)**
Reference MCP server for cookie-session systems that expose no public API, with a Hono mock
target and fixtures so the suite runs offline. 24 tests, MIT.
Writeup: [How I built MCP servers for systems that have no API](https://mcp-cookie-auth-blog.vercel.app)

## Upstream

- [BoundaryML/baml#4070](https://github.com/BoundaryML/baml/pull/4070), escape Python reserved
  words in generated SDK identifiers. **Open.** +3,592 / -140 across 13 files, covering every
  identifier site in the Python generator plus a bridge fix, preserving BAML wire identity while
  changing host-language spelling.
- [vercel/ai#15568](https://github.com/vercel/ai/pull/15568), resolve npx and uv ENOENT on
  Windows via shell spawn. **Open.** +95 / -9, with two platform-mocked tests.
- [mbachaud/Cymatix-Context#190](https://github.com/mbachaud/Cymatix-Context/pull/190), a
  Grace Blackwell aarch64 launch-blocking shim, shipped default off so x86_64 does not pay the
  sync tax. **Merged 2026-06-09.** I am one of two contributors to that project.

## Smaller things

- [prd-engine](https://github.com/addiplus/prd-engine), multi-agent PRD pipeline, 10 agents and
  4 intensity tiers.
- [safe-rm-guard](https://github.com/addiplus/safe-rm-guard), a Claude Code hook that blocks
  recursive deletes, including the false-positive case the obvious regex gets wrong.
- [claude-skill-pack](https://github.com/addiplus/claude-skill-pack), four Bun-native Claude Code
  skills.
- [mcp-builder](https://github.com/addiplus/mcp-builder), notes on dual-transport MCP servers and
  the OAuth 2.1 ceremony.

Seattle. Open to AI-native engineering work.
