# Project Codex foundation

This directory contains the versioned Codex operating model for the **Friday Infrastructure Support Agent**.

## Layout

- `agents/` — role-specific instructions for the orchestrator and specialist subagents.
- `skills/` — reusable support workflows and domain knowledge.
- `mcp/` — project documentation for external MCP dependencies; secrets stay outside the repository.

## Runtime dependencies

Engram and Context7 are configured as user-level MCP servers in Codex. This repository keeps only their project contract and usage guidance. Do not add tokens, local machine paths, or generated MCP state here.

## Operating principles

1. Read-only discovery before mutation.
2. Ask for explicit approval before disruptive infrastructure actions.
3. Prefer reversible, observable changes with a rollback plan.
4. Treat Linux hosts as infrastructure targets and Windows devices as client targets.
5. Record decisions, incidents, and non-obvious discoveries in Engram.
