---
title: CLAUDE.md
---

# CLAUDE.md


This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

This is Jack Walton's technical writing portfolio, built with Next.js and [Nextra](https://nextra.site/). It showcases technical writing samples including a user guide, a UX research paper, and an academic grant proposal. The audience of this portfolio consists of technical recruiters, founders, and people with technical interests. This portfolio is intended to be professional.

## About Jack

Jack is a technical writer with four years of experience at Oracle Health, where he documents revenue cycle management (RCM) software across the full product lifecycle: UX research, component design, UI copy, help documentation, and release notes. He has a background in English language and literature and medieval studies with peer-reviewed academic publications.

## Writing Preferences

- No em-dashes
- Direct, clear prose without filler phrases or self-deprecating qualifiers
- Tech industry conventions over academic style (e.g., *data* as a singular mass noun)
- Present tense for documentation; past tense for historical or completed work

## Commands

```bash
pnpm dev          # Start local dev server
pnpm build        # Build for production (runs pagefind search index afterward)
pnpm start        # Serve the production build
```

The `postbuild` script runs `pagefind` to generate the full-text search index from the built output. Search won't work locally unless you run `pnpm build && pnpm start` rather than `pnpm dev`.

## Project Structure

```
content/         ← MDX source files
  _meta.js       ← Top-level sidebar/nav order
  <section>/
    _meta.js     ← Section-level sidebar order and page titles
public/          ← Static assets
next.config.mjs  ← Nextra plugin config (search enabled, copy code enabled)
```

Navigation order and display titles are controlled entirely by `_meta.js` files — Nextra does not auto-discover pages. When adding a new page, register it in the nearest `_meta.js`.

## Slash Commands

Project-level slash commands live in `.claude/commands/` and are documented in `content/AI Tooling/commands/`.