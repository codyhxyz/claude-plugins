# codyhxyz-plugins 🍋

*agentic scaffolding for thinking alongside LLMs.*

i build things constantly, things i deeply care about. along the way i keep finding little heuristics that work for me, and if they work for me they probably work for someone else too. so in the spirit of open-sourcing myself, i'm open-sourcing the heuristics as plugins. this is how i work with claude.

<p>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License"></a>
  <a href="https://claude.com/product/claude-code"><img src="https://img.shields.io/badge/built_for-Claude%20Code-d97706" alt="Built for Claude Code"></a>
</p>

<p align="center"><img src="assets/hero.svg" alt="codyhxyz-plugins · for those who need the lemon zest" width="100%"></p>

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

clustered by what they're for. mine are marked with no badge; curated third-party picks get a ↗.

### build

| Plugin | What it does |
|---|---|
| [`create-claude-plugin` 🛠️](https://github.com/codyhxyz/create-claude-plugin) | A claude plugin that ships claude plugins. Scaffold it, validate it, push it, submit it to the official Anthropic marketplace, all in one session. Makes your plugins look gooood on GitHub + elsewhere. |

### engineering

| Plugin | What it does |
|---|---|
| [`prompt-optimizer` 🎯](https://github.com/codyhxyz/prompt-optimizer) | Bad prompting poisons your context. This plugin fills in the implicit details in your vague prompt. Cuts token use and gets better results in the critical first conversational turn with Opus 4.7. |
| [`first-principles-review` 🔬](https://github.com/codyhxyz/first-principles-review) | A better code review. Use after one-shotting a project, when you want to make sure Claude built what you wanted it to. Scope creep killer. |
| [`eureka` ⚡](https://github.com/codyhxyz/eureka) | A subagent for when claude is trying all the wrong things. Use it when you need Claude to think outside the box. This is my #1 most helpful plugin for unblocking stuck coding sessions. 💡 |

### writing

| Plugin | What it does |
|---|---|
| [`synonymmer` 📚](https://github.com/codyhxyz/synonymmer) | Thesaurus on steroids for naming and writing. Outputs 100-200 latent-space-near words and phrases related to your seed term, organized into clusters. |
| [`spotify-notes` 🎧](https://github.com/codyhxyz/spotify-notes-plugin) | A song-indexed journal for whatever Spotify is playing right now. Say "note: that piano at 2:14 is killing me" and it lands in a per-track markdown file with a timestamp. Zero OAuth — uses the desktop app's own IPC. |
| [`humanizer` ✍️ ↗](https://github.com/blader/humanizer) | **↗ not mine, just rec'd.** Strips AI tells from text — em-dash overuse, inflated adjectives, filler phrases, the whole "signs of AI writing" checklist. Runs a second pass to catch its own lingering AI-isms, and can voice-match from a writing sample so the output sounds like *you*, not like a cleaned-up LLM. |

### security

| Plugin | What it does |
|---|---|
| [`metapod-harden` 🛡️](https://github.com/codyhxyz/metapod-harden) | Multi-provider security audit + breach-response toolkit. Inventory your Vercel env-var/token surface, classify by risk, rotate creds with provider deep-links + automated platform-side swaps, install pre-emptive hardening hooks. Built in response to the April 2026 Vercel breach. When the next breach hits, your response time is 15 minutes, not 3 days. |

### claude code quality-of-life

| Plugin | What it does |
|---|---|
| [`statusline` 📊](https://github.com/codyhxyz/statusline) | A Claude Code statusline with HSL-gradient ring meters for context window and 5h/7d rate limits with live reset countdowns. Catch context rot before Anthropic tells you to `/clear`. |
| [`hook-sounds` 🔊](https://github.com/codyhxyz/hook-sounds) | Plays a random sound when Claude Code fires a lifecycle hook. Ships with an Oddworld: Munch's Oddysee pack by default — dumb, joyful. Swap in your own CC0 sounds if you'd rather. macOS only. |

## why these exist

some of these are scaffolding for unhobbling the model. some are scaffolding for unhobbling yourself. a couple are just neat.

watch this space. i'm getting obsessed with claude plugins and starting to understand something about them, which is why i built [`create-claude-plugin`](https://github.com/codyhxyz/create-claude-plugin) in the first place — i knew i'd be shipping a lot of these.

## license

[MIT](LICENSE) © 2026 Cody Hergenroeder

---

<sub><i>"i create because i envision that there are people out there who need the lemon zest."</i></sub>
