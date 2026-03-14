# MarkpadPlus Project Instructions

## Overview

Fork of [alecdotdev/Markpad](https://github.com/alecdotdev/Markpad). Desktop markdown editor built with Tauri 2 + SvelteKit + TypeScript (frontend) and Rust (backend).

## Stack

- **Frontend:** SvelteKit 2 (SPA mode via adapter-static), Svelte 5, TypeScript 5.6, Vite 6
- **Editor:** Monaco Editor (with Vim bindings via monaco-vim)
- **Backend:** Tauri 2 (Rust), comrak for markdown parsing
- **Rendering:** DOMPurify, highlight.js, KaTeX, Mermaid
- **Build:** `npm run dev` (frontend), `npm run tauri dev` (full app), `npm run tauri build` (release)

## Project Structure

```
src/                    # SvelteKit frontend
  lib/
    components/         # Svelte components
    stores/             # Svelte stores
    MarkdownViewer.svelte  # Main markdown viewer
    Installer.svelte    # OS installer UI
    Uninstaller.svelte  # OS uninstaller UI
  routes/               # SvelteKit routes (SPA)
  styles.css            # Global styles
src-tauri/              # Tauri/Rust backend
  src/                  # Rust source
  Cargo.toml            # Rust dependencies
  tauri.conf.json       # Tauri config
static/                 # Static assets
```

## Development Workflow

Use `/workflow` for ALL coding tasks — bug fixes, features, refactors, migrations, scripts. No exceptions.

## Language Rules

Load rules from `~/.claude/rules/typescript/` before any frontend code work.

## Upstream

- Remote `upstream` points to `alecdotdev/Markpad`
- Keep our changes isolated (new files preferred) to minimize merge conflicts when syncing upstream
- Sync: `git fetch upstream && git merge upstream/master`

## Dev Server

- Frontend: port 1420 (strict)
- HMR: port 1421
