# codyhxyz-plugins 🍋

*agentic scaffolding for thinking alongside LLMs.*

i build things constantly, things i deeply care about. i keep finding heuristics that work for me, and if they work for me they probably work for someone else too. so in the spirit of open-sourcing myself, i'm open-sourcing the heuristics as plugins. these are ways i work with claude.

<p>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License"></a>
  <a href="https://claude.com/product/claude-code"><img src="https://img.shields.io/badge/built_for-Claude%20Code-d97706" alt="Built for Claude Code"></a>
</p>

## install

```
/plugin marketplace add codyhxyz/claude-plugins
```

then install any plugin from the table below:

```
/plugin install <plugin-name>@codyhxyz-plugins
```

pull new plugins and version bumps:

```
/plugin marketplace update codyhxyz-plugins
```

## available plugins

| Plugin | What it does |
|---|---|
| [`create-claude-plugin`](https://github.com/codyhxyz/create-claude-plugin) | A Claude plugin that ships Claude plugins. Scaffold, validate, push, and submit to the official Anthropic marketplace in one session. |
| [`prompt-optimizer`](https://github.com/codyhxyz/prompt-optimizer) | Turns vague task requests into grounded, structured specs before your implementation agent runs. |
| [`first-principles-review`](https://github.com/codyhxyz/first-principles-review) | Reviews codebases top-down: WHY (goal) → WHAT (architecture) → HOW (implementation) → improvements ranked by leverage. Questions the premise, not the semicolons. |
| [`iconoclast`](https://github.com/codyhxyz/iconoclast) | A subagent for when Claude is trying all the wrong things. Drops the safe answer and reaches for the edge of its training data. |
| [`synonymmer`](https://github.com/codyhxyz/synonymmer) | 100–200 wide-net related words for a seed term, organized into vibe-based clusters. Thesaurus-on-steroids for naming and brainstorming. |

## why these exist

some are cognitive scaffolding for unhobbling LLMs. some are cognitive scaffolding for unhobbling yourself. some are just neat tools and novelties.

watch this space. i'm getting obsessed with claude plugins and starting to understand something about them. that's why i built [`create-claude-plugin`](https://github.com/codyhxyz/create-claude-plugin) after all, because i knew i'd be shipping a ton of these.

## how this is wired

a single-author registry. each entry in [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json) points at an external plugin repo via `{"source": "github", "repo": "..."}`. plugin versions are pinned in each plugin's own `plugin.json` (not here), per the official recommendation for non-relative sources.

adding a new plugin = append one entry to `marketplace.json`, commit, push. subscribers pick it up on the next `/plugin marketplace update`.

## license

[MIT](LICENSE) © 2026 Cody Hergenroeder

---

<sub><i>"i create because i envision that there are people out there who need the lemon zest."</i></sub>
