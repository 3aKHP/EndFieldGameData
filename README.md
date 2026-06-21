# EndFieldGameData

Self-hosted mirror of **text-only JSON game data tables** from *Arknights: Endfield*, consumed by [EndField-MCP](https://github.com/3aKHP/EndFiled-MCP) via GitHub Releases.

## What this is

This repository publishes **structured JSON tables** (character stats, enemy data, equipment, items, localization) extracted from the game client. It contains **no binary assets** — no images, audio, models, or raw game files. The data is the minimum needed for fan-creation tools (MCP servers, wikis, lookup apps) to query game mechanics.

## Data source

Tables are extracted by [`Variante/endfield_research_kit`](https://github.com/Variante/endfield_research_kit), a local export toolkit that reads a legally-obtained Endfield installation. This repository then post-processes the export into the compact layout below and publishes it as Release assets.

## Release asset layout

Each Release ships one asset: `endfield-tables.zip`. Internal structure:

```
endfield-tables.zip
├── tables/                          # 10 core game tables
│   ├── CharacterTable.json          # playable characters
│   ├── EnemyTable.json              # enemy instances
│   ├── EnemyTemplateTable.json      # enemy stat templates
│   ├── EnemyDisplayInfoTable.json   # enemy display metadata
│   ├── EquipTable.json              # equipment stats
│   ├── EquipItemTable.json          # equipment item entries
│   ├── CharProfessionTable.json     # profession enum (近卫/重装/...)
│   ├── CharTypeTable.json           # element type enum
│   ├── CharacterTagTable.json       # character tags
│   └── ItemTable.json               # items & materials
└── i18n/                            # 5 localization tables
    ├── CN.json                      # Simplified Chinese
    ├── EN.json                      # English
    ├── JP.json                      # Japanese
    ├── TC.json                      # Traditional Chinese
    └── KR.json                      # Korean
```

Tables store localization keys (int64 hashes) in `{id, text}` objects where `text` is empty. The actual strings live in the i18n files keyed by those hashes as strings.

## Versioning

Tags follow SemVer. Minor version tracks the EndField-MCP consumer version (v0.2.x mirror ↔ EndField-MCP 0.2.x). Patch bumps when the game updates without schema changes.

## License

- **Wrapper code** (build scripts, CI, this README): MIT
- **Game data** (the JSON tables themselves): © Hypergryph / Gryphline. This mirror exists to support fan creation; it does not claim ownership of game content. If you are Hypergryph and want this data removed, open an issue.

## Related

- [EndField-MCP](https://github.com/3aKHP/EndFiled-MCP) — MCP server that consumes these releases
- [endfield_research_kit](https://github.com/Variante/endfield_research_kit) — extraction toolkit
