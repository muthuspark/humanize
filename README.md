# Humanize

A Codex plugin that rewrites AI-sounding text into natural prose while preserving meaning, structure, and voice.

It adds the `humanizer` skill, adapted from [`blader/humanizer`](https://github.com/blader/humanizer), and targets common AI writing tells such as inflated significance, promotional phrasing, vague attribution, rule-of-three padding, generic conclusions, excessive hedging, chatbot artifacts, and em dashes.

## Install in Codex

Clone the repo:

```bash
git clone https://github.com/muthuspark/humanize.git
cd humanize
```

Register the local marketplace:

```bash
codex plugin marketplace add "$(pwd)/.agents/plugins"
```

Install the plugin:

```bash
codex plugin add humanize@humanize
```

Start a new Codex thread after installing so Codex picks up the new skill.

## Use

Ask Codex to humanize text:

```text
Humanize this text without changing its meaning:

<paste text here>
```

For voice matching, include a sample:

```text
Humanize this text in my style. Sample:

<paste writing sample>

Text:

<paste text>
```

## Layout

```text
.agents/plugins/marketplace.json  # Local Codex marketplace
plugins/humanize/                 # Marketplace plugin package
.codex-plugin/plugin.json         # Direct plugin manifest
skills/humanizer/SKILL.md         # Direct skill source
```

## License

MIT. The humanizer skill content is adapted from `blader/humanizer`.
