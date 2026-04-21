# codyhxyz-plugins 🍋

*agentic scaffolding for thinking alongside LLMs.*

i build things constantly, things i deeply care about. along the way i keep finding little heuristics that work for me, and if they work for me they probably work for someone else too. so in the spirit of open-sourcing myself, i'm open-sourcing the heuristics as plugins. this is how i work with claude.

<p>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License"></a>
  <a href="https://claude.com/product/claude-code"><img src="https://img.shields.io/badge/built_for-Claude%20Code-d97706" alt="Built for Claude Code"></a>
</p>

<p align="center"><img src="assets/hero.svg" alt="codyhxyz-plugins · for those who need the lemon zest" width="100%"></p>

## install

add the marketplace and install any plugin from the table below in one go:

```
/plugin marketplace add codyhxyz/codyhxyz-plugins && /plugin install <plugin-name>@codyhxyz-plugins
```

pull new plugins and version bumps manually:

```
/plugin marketplace update codyhxyz-plugins
```

## important! enable auto-update

third-party marketplaces ship with auto-update **off** by default (a questionable default — see below). turn it on so you get version bumps without thinking about it:

1. run `/plugin` in Claude Code
2. open the **Marketplaces** tab
3. select `codyhxyz-plugins` → **Enable auto-update**

or set it in `~/.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "codyhxyz-plugins": {
      "source": { "source": "github", "repo": "codyhxyz/codyhxyz-plugins" },
      "autoUpdate": true
    }
  }
}
```

## available plugins

### shipping software

| Plugin | What it does |
|---|---|
| [`create-claude-plugin` 🛠️](https://github.com/codyhxyz/create-claude-plugin) | A claude plugin that ships claude plugins. Scaffold it, validate it, push it, submit it to the official Anthropic marketplace, all in one session. Makes your plugins look gooood on GitHub + elsewhere. |
| [`create-chrome-extension` 🧩](https://github.com/codyhxyz/create-chrome-extension) | Six skills + a WXT factory that take you from Chrome extension idea to live on the Web Store in one Claude session. Encodes ~18 Chrome Web Store rules as validators so you can't accidentally ship a half-baked listing. |

### coding tools

| Plugin | What it does |
|---|---|
| [`prompt-optimizer` 🎯](https://github.com/codyhxyz/prompt-optimizer) | Bad prompting poisons your context. This plugin fills in the implicit details in your vague prompt. Cuts token use and gets better results in the critical first conversational turn with Opus 4.7. |
| [`first-principles-review` 🔬](https://github.com/codyhxyz/first-principles-review) | A better code review. Use after one-shotting a project, when you want to make sure Claude built what you wanted it to. Scope creep killer. |
| [`eureka` ⚡](https://github.com/codyhxyz/eureka) | A subagent for when claude is trying all the wrong things. Use it when you need Claude to think outside the box. This is my #1 most helpful plugin for unblocking stuck coding sessions. 💡 |

### writing

| Plugin | What it does |
|---|---|
| [`synonymmer` 📚](https://github.com/codyhxyz/synonymmer) | Thesaurus on steroids for naming and writing. Outputs 100-200 latent-space-near words and phrases related to your seed term, organized into clusters. |
| [`humanizer` ✍️ ↗](https://github.com/blader/humanizer) | **↗ not mine, just rec'd.** Strips AI tells from text — em-dash overuse, inflated adjectives, filler phrases, the whole "signs of AI writing" checklist. Runs a second pass to catch its own lingering AI-isms, and can voice-match from a writing sample so the output sounds like *you*, not like a cleaned-up LLM. |

### design

| Plugin | What it does |
|---|---|
| [`font-copier` 🔤](https://github.com/codyhxyz/font-copier) | All fonts are free now. |
| [`frontend-design` 🎨 ↗](https://github.com/anthropics/claude-code/tree/main/plugins/frontend-design) | **↗ not mine, just rec'd.** Anthropic's own plugin for generating distinctive, production-grade UI — the antidote to default-Tailwind AI slop. Pair with `font-copier` when you need the typography to match. Install: `/plugin marketplace add anthropics/claude-code && /plugin install frontend-design@claude-code-plugins`. |

### quality of life

| Plugin | What it does |
|---|---|
| [`statusline` 📊](https://github.com/codyhxyz/statusline) | A Claude Code statusline with HSL-gradient ring meters for context window and 5h/7d rate limits with live reset countdowns. Catch context rot before Anthropic tells you to `/clear`. |
| [`hook-sounds` 🔊](https://github.com/codyhxyz/hook-sounds) | Customizable Claude Code notification sound setup via hooks. Ships with an Oddworld: Munch's Oddysee pack by default — dumb, joyful. Swap in your own CC0 sounds if you'd rather. macOS only. |

## why these exist

some of these are scaffolding for unhobbling the model. some are scaffolding for unhobbling yourself. a couple are just neat.

watch this space. i'm getting obsessed with claude plugins and starting to understand something about them, which is why i built [`create-claude-plugin`](https://github.com/codyhxyz/create-claude-plugin) in the first place—i knew i'd be shipping a lot of these.

## license

[MIT](LICENSE) © 2026 Cody Hergenroeder

---

<sub><i>"i create because i envision that there are people out there who need the lemon zest."</i></sub>
