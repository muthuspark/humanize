# Humanize

A Codex plugin that rewrites AI-sounding text into natural prose while preserving meaning, structure, and voice.

It adds the `humanizer` skill, adapted from [`blader/humanizer`](https://github.com/blader/humanizer), and targets common AI writing tells such as inflated significance, promotional phrasing, vague attribution, rule-of-three padding, generic conclusions, excessive hedging, chatbot artifacts, and em dashes.

## Install in Codex

Add the GitHub repo as a Codex marketplace:

```bash
codex plugin marketplace add muthuspark/humanize
```

Install the plugin:

```bash
codex plugin add humanize@humanize
```

Start a new Codex thread after installing so Codex picks up the new skill.

## Local development install

Use this path only if you want to edit the plugin locally.

```bash
git clone https://github.com/muthuspark/humanize.git
cd humanize
codex plugin marketplace add "$(pwd)/.agents/plugins"
codex plugin add humanize@humanize
```

After changing the plugin, refresh the marketplace or restart Codex before testing in a new thread.

## Sparse install

If you want Codex to fetch only the marketplace and plugin package from the repo:

```bash
codex plugin marketplace add muthuspark/humanize \
  --sparse .agents/plugins \
  --sparse plugins/humanize
codex plugin add humanize@humanize
```

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
