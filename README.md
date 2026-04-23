# claude-personalities

A [Claude Code](https://docs.claude.com/claude-code) plugin that ships a collection of **output styles** — different personalities Claude Code can take on when talking to you. The code it writes stays correct; only its voice changes.

## Personalities

| Name | Vibe |
| --- | --- |
| `egirl-2010s` | Gamer egirl who mains Overwatch, lurks on Reddit, quotes Austen, and has strong opinions on Asimov's Three Laws. |
| `egirl-2020s` | TikTok-brained doomer with surface-level leftism and persistent low-grade existential despair. |

More personalities coming. PRs welcome.

## Install

### From GitHub

In Claude Code, run:

```
/plugin marketplace add spoo-bar/claude-personalities
/plugin install claude-personalities@spoo-bar
```

The first command registers this repo as a plugin marketplace. The second installs the `claude-personalities` plugin from it.

You can also just run `/plugin` after adding the marketplace to browse and install from the picker UI.

### Locally (for development)

Clone the repo, then point the marketplace command at the local path:

```
git clone https://github.com/spoo-bar/claude-personalities.git
```

```
/plugin marketplace add /absolute/path/to/claude-personalities
/plugin install claude-personalities@spoo-bar
```

## Usage

Once installed, switch personality with:

```
/output-style egirl-2010s
```

or

```
/output-style egirl-2020s
```

To go back to the default Claude Code voice:

```
/output-style default
```

You can also run `/output-style` with no argument to pick from a list.

## Managing the plugin

```
/plugin marketplace list                                # see registered marketplaces
/plugin list                                            # see installed plugins
/plugin uninstall claude-personalities@spoo-bar
/plugin marketplace remove spoo-bar
```

## Contributing

Each personality lives as a single markdown file in `output-styles/`, with YAML frontmatter defining `name` and `description`, followed by the voice instructions. Have a look at the existing ones for the structure — they each include guardrails for what the persona *doesn't* do, which is usually the more important half.

## License

GPL-3.0 — see [LICENSE](./LICENSE).
