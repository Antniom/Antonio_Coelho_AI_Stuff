# António Coelho's AI stuff

A Claude Code plugin marketplace for my CAD and mechanical-engineering plugins, skills and MCP servers.

## Install

In Claude Code:

```
/plugin marketplace add Antniom/Antonio_Coelho_AI_Stuff
/plugin install solidcadworks@antonio-coelho-ai-stuff
/plugin install inventor-mcp@antonio-coelho-ai-stuff
```

## Plugins

| Plugin | What it does | Source |
|---|---|---|
| `solidcadworks` | Model parts, build assemblies, make drawings and run stress analysis in SolidWorks, with an interactive studio for adjusting dimensions. | [Antniom/Solidworks-MCP](https://github.com/Antniom/Solidworks-MCP) |
| `inventor-mcp` | Model parts, assemblies and mechanisms in Autodesk Inventor 2026/2027, and learn your company's modeling and drawing conventions. | [Antniom/Inventor-PluginV2](https://github.com/Antniom/Inventor-PluginV2) |

Both need Windows and a local install of the CAD program. See each repository's README for requirements.

## Staying up to date

This repository only lists the plugins; each one is fetched straight from its own repository, so a push there is the update.

- Run `/plugin marketplace update antonio-coelho-ai-stuff` to fetch the latest, then `/reload-plugins`.
- Or turn on auto-update once: `/plugin` → Marketplaces → `antonio-coelho-ai-stuff` → Enable auto-update.

## Adding a plugin

Add an entry to `.claude-plugin/marketplace.json`:

```json
{
  "name": "my-plugin",
  "source": { "source": "github", "repo": "Antniom/my-plugin-repo" },
  "description": "What it does."
}
```

The entry `name` must match the `name` in the plugin's own `.claude-plugin/plugin.json`. Leave `version` out of `plugin.json` so every push reaches users; with a `version` set, users only get an update when that string changes.
