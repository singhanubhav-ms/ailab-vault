---
type: meta
title: "Hot Cache"
updated: 2026-04-26T16:05:00+05:30
tags:
  - meta
  - hot-cache
  - lighthouse
status: current
related:
  - "[[index]]"
  - "[[log]]"
  - "[[overview]]"
---

# Recent Context

Navigation: [[index]] | [[log]] | [[overview]]

## Current Focus

This vault is currently being used for the Lighthouse AI lab runtime. Treat older DragonScale and claude-obsidian release-note content as historical context, not the active operating context for current questions.

## Live Runtime

- Lighthouse runs through OpenClaw on the Azure VM inside WSL Ubuntu 24.04.
- The OpenClaw gateway is the main runtime process and is managed by the user systemd service.
- Human entrypoints for v1 are Discord and the CLI.
- The currently validated agent path is `researcher` on `azure/gpt-5.4-mini`.
- For cached context, read `wiki/hot.md` first. If it answers the question, answer immediately.

## Vault Topology

- The Mac clone of `ailab-vault` is for Obsidian and human editing.
- The VM clone of `ailab-vault` is the working copy used by agents.
- GitHub is the sync point between the Mac clone and the VM clone.
- Obsidian is the human UI for the vault. It does not run the agents.

## Current Verified State

- Discord is configured and paired for Lighthouse Control.
- The researcher path is working again and correctly uses the hot-cache-first flow.
- The stale researcher-session issue was fixed by resetting the affected session state.
- The top-level `openclaw health` mismatch was identified as an upstream product bug, not just local drift.
- The upstream bug is filed as `openclaw/openclaw#72079`.

## Open Operational Items

- `wiki-lint-weekly` cron is installed and enabled. The current schedule is Sunday 08:00 Asia/Kolkata.
- `vm-ailab` now supports key-based SSH via the dedicated local key alias. Password fallback is no longer needed for normal operator access.
- Older claude-obsidian and DragonScale material remains in the vault as historical archive and should not be treated as the default project focus.

## Working Rules

- Prefer Lighthouse-specific context over older plugin-development context.
- Do not assume DragonScale release work is the current project focus.
- Use the vault for durable notes and reports, not this cockpit repo.
