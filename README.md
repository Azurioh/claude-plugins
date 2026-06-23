# claude-plugins

A personal marketplace of [Claude Code](https://docs.claude.com/en/docs/claude-code) plugins by Azurioh.

Each plugin lives in **its own repository** and is versioned independently — this repo is just the catalog that ties them together so you only add one marketplace.

## Add the marketplace

```
/plugin marketplace add Azurioh/claude-plugins
```

## Plugins

| Plugin | Install | What it does |
|---|---|---|
| [speckit-brainstorm](https://github.com/Azurioh/speckit-brainstorm) | `/plugin install speckit-brainstorm@azurioh-plugins` | Conversational guide through the full [GitHub Spec Kit](https://github.com/github/spec-kit) workflow — challenges your idea, then runs each speckit step behind a preview-and-confirm gate. Installs speckit (latest release) if it's missing. |
| [git-recap](https://github.com/Azurioh/git-recap) | `/plugin install git-recap@azurioh-plugins` | `/git-recap` recaps your repo's changes over any time window you describe in plain language ("les 2 derniers jours", "2 weeks", "1 mois") — a detailed technical section plus a plain-language summary for non-technical readers. Optional GitHub PR enrichment (`--prs`, needs `gh`) and markdown export (`--save`). |

## Adding a new plugin to this marketplace

1. Build the plugin in its own repo (with `.claude-plugin/plugin.json` at the root).
2. Add an entry to `.claude-plugin/marketplace.json`:
   ```json
   {
     "name": "<plugin-name>",
     "source": { "source": "github", "repo": "Azurioh/<plugin-repo>" },
     "description": "<one line>"
   }
   ```
3. Commit, push, and add the row above.
