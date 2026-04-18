<h1 align="center">codyhxyz-plugins</h1>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License"></a>
  <a href="https://claude.com/product/claude-code"><img src="https://img.shields.io/badge/built_for-Claude%20Code-d97706" alt="Built for Claude Code"></a>
</p>

<p align="center"><b>One marketplace. Every plugin I ship. Add it once.</b></p>

A Claude Code plugin marketplace. Add this repo once and install any plugin I publish without chasing individual `/plugin marketplace add` commands.

## Install

```
/plugin marketplace add codyhxyz/claude-plugins
```

Then install any plugin from the table below:

```
/plugin install <plugin-name>@codyhxyz-plugins
```

Pull new plugins and version bumps:

```
/plugin marketplace update codyhxyz-plugins
```

## Available plugins

| Plugin | What it does |
|---|---|
| [`create-claude-plugin`](https://github.com/codyhxyz/create-claude-plugin) | A Claude plugin that ships Claude plugins — scaffold, validate, push, and submit to the official Anthropic marketplace in one session. |
| [`prompt-optimizer`](https://github.com/codyhxyz/prompt-optimizer) | Turns vague task requests into grounded, structured specs before your implementation agent runs. |
| [`first-principles-review`](https://github.com/codyhxyz/first-principles-review) | Reviews codebases top-down — WHY (goal) → WHAT (architecture) → HOW (implementation) → improvements ranked by leverage. The antidote to surface-level LLM nitpicks. |
| [`iconoclast`](https://github.com/codyhxyz/iconoclast) | A subagent for when Claude is trying all the wrong things — drops the safe answer and reaches for the edge of its training data. |
| [`synonymmer`](https://github.com/codyhxyz/synonymmer) | 100–200 wide-net related words for a seed term, organized into vibe-based clusters. Thesaurus-on-steroids for naming and brainstorming. |

## How this is wired

A single-author registry. Each entry in [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json) points at an external plugin repo via `{"source": "github", "repo": "..."}`. Plugin versions are pinned in each plugin's own `plugin.json` — not here — per the official recommendation for non-relative sources.

Adding a new plugin = append one entry to `marketplace.json`, commit, push. Subscribers pick it up on the next `/plugin marketplace update`.

## License

[MIT](LICENSE) © 2026 Cody Hergenroeder
