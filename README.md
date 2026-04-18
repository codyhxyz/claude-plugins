# codyhxyz-plugins 🍋

*agentic scaffolding for thinking alongside LLMs.*

i build things constantly, things i deeply care about. along the way i keep finding little heuristics that work for me, and if they work for me they probably work for someone else too. so in the spirit of open-sourcing myself, i'm open-sourcing the heuristics as plugins. this is how i work with claude.

<p>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License"></a>
  <a href="https://claude.com/product/claude-code"><img src="https://img.shields.io/badge/built_for-Claude%20Code-d97706" alt="Built for Claude Code"></a>
</p>

## install

```
/plugin marketplace add codyhxyz/codyhxyz-plugins
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
| [`create-claude-plugin` 🛠️](https://github.com/codyhxyz/create-claude-plugin) | A claude plugin that ships claude plugins. Scaffold it, validate it, push it, submit it to the official Anthropic marketplace, all in one session. |
| [`prompt-optimizer` 🎯](https://github.com/codyhxyz/prompt-optimizer) | Fills in the implicit details in your vague prompt. Cuts token use and gets better results in the critical first conversational turn with Opus 4.7. |
| [`first-principles-review` 🔬](https://github.com/codyhxyz/first-principles-review) | A better code review. Less over-building, more delivering what you asked for. |
| [`eureka` ⚡](https://github.com/codyhxyz/eureka) | A subagent for when claude is trying all the wrong things. Use it when you need Claude to think outside the box. This is my "eureka" plugin, my #1 most helpful plugin in daily use. |
| [`synonymmer` 📚](https://github.com/codyhxyz/synonymmer) | Thesaurus on steroids for naming and brainstorming. Outputs 100-200 latent-space-near words and phrases related to your seed term, organized into vibe-based clusters. |

## why these exist

some of these are scaffolding for unhobbling the model. some are scaffolding for unhobbling yourself. a couple are just neat.

watch this space. i'm getting obsessed with claude plugins and starting to understand something about them, which is why i built [`create-claude-plugin`](https://github.com/codyhxyz/create-claude-plugin) in the first place — i knew i'd be shipping a lot of these.

Because it breaks the “normal” repository pattern on purpose.

- This repo is not a single app; it’s a **control plane + catalog** for many independent plugins.
- Discovery is separated from implementation: users consume from this index, while plugin behavior lives in other repos.
- It is **single-source indexing** (`repo` pointers only) plus **distributed ownership** (each plugin owns its own version/behavior), which keeps the registry thin and mutable.
- That design is “weird” in a good way: less central control, less duplication, and less risk that the catalog becomes a giant monorepo of unrelated code.

## license

[MIT](LICENSE) © 2026 Cody Hergenroeder

---

<sub><i>"i create because i envision that there are people out there who need the lemon zest."</i></sub>
