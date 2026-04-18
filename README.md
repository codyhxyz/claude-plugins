<h1 align="center">codyhxyz-plugins</h1>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License"></a>
  <a href="https://claude.com/product/claude-code"><img src="https://img.shields.io/badge/built_for-Claude%20Code-d97706" alt="Built for Claude Code"></a>
</p>

<p align="center"><b>One marketplace. Every plugin I ship. Add it once.</b></p>

A Claude Code plugin marketplace. Users add this repo once and then install any plugin I publish without chasing individual `/plugin marketplace add` commands.

## Quick Start

### Add the marketplace

```
/plugin marketplace add codyhxyz/claude-plugins
```

### Install any plugin

```
/plugin install prompt-optimizer@codyhxyz-plugins
```

Refresh to pick up new plugins and version changes:

```
/plugin marketplace update codyhxyz-plugins
```

## Available plugins

| Plugin | Description |
|---|---|
| [`prompt-optimizer`](https://github.com/codyhxyz/prompt-optimizer) | Turns vague task requests into grounded, structured specs before your implementation agent runs. |

## For plugin authors

This is a single-author registry. Each entry in [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json) points at an external plugin repo via `{"source": "github", "repo": "..."}`. Plugin versions are pinned in each plugin's own `plugin.json` — not here — per the official recommendation for non-relative sources.

Adding a new plugin = append one entry to `marketplace.json`, commit, push. Subscribers pick it up on the next `/plugin marketplace update`.

## License

[MIT](LICENSE) © 2026 Cody Hergenroeder
