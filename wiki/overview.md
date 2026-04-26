---
type: overview
title: "Wiki Overview"
created: 2026-04-07
updated: 2026-04-26
tags:
  - meta
  - overview
  - lighthouse
status: current
related:
  - "[[index]]"
  - "[[hot]]"
  - "[[log]]"
  - "[[dashboard]]"
  - "[[LLM Wiki Pattern]]"
sources:
---

# Wiki Overview

Navigation: [[index]] | [[hot]] | [[log]] | [[dashboard]]

---

## Purpose

This is the working vault for Lighthouse, Anubhav's personal AI lab. It is the shared memory layer used by OpenClaw agents on the VM and the human editing surface in Obsidian on the Mac.

## Current Operating Model


- The Mac clone of `ailab-vault` is opened in Obsidian for human editing and browsing.
- The VM clone of `ailab-vault` is the working copy used by OpenClaw agents.
- GitHub is the sync point between those two clones.
- Discord and the CLI are the active human entrypoints for v1.


## Current State

- OpenClaw is live on the Azure VM inside WSL Ubuntu 24.04.
- The current validated agent path is `researcher` on `azure/gpt-5.4-mini`.
- `wiki-lint-weekly` is installed as the weekly maintenance cron job.
- The hot cache has been refreshed for Lighthouse-specific runtime context.
- Older claude-obsidian and DragonScale material remains in the vault as archival history.


## Important Files

- [[hot]] — first-stop cached runtime context
- [[index]] — current map of the vault
- [[log]] — append-only operational history


## Key Themes

**The vault is the durable memory layer.** OpenClaw agents use it for persistent context, reports, and operational state.

**Obsidian is the human UI.** The Mac clone is for browsing, backlinks, graph view, and manual editing. It is not the agent runtime.

**Historical plugin-development content still exists.** Treat older claude-obsidian and DragonScale notes as archive unless a question explicitly asks for that history.
