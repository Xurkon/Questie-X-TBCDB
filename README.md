# Questie-X-TBCDB

A [Questie-X](https://github.com/Xurkon/Questie-X) database plugin providing the full **The Burning Crusade (2.5.x)** quest, NPC, object, and item database — including Classic baseline corrections.

---

## Requirements

- [Questie-X](https://github.com/Xurkon/Questie-X) must be installed. This plugin will not load without it.
- WoW client: 2.5.x (TBC Classic)

---

## Installation

1. Download the latest release archive from the [Releases](https://github.com/Xurkon/Questie-X-TBCDB/releases) page.
2. Extract it into your `Interface/AddOns/` directory.
3. The extracted folder **must** be named `Questie-X-TBCDB`.
4. Ensure `Questie-X` is also present in `Interface/AddOns/`.
5. Reload your UI or restart the client.

Your addon list should look like:
```
Interface/AddOns/
  Questie-X/
  Questie-X-TBCDB/
```

---

## What is Included

| Path | Contents |
|------|----------|
| `Database/TBC/` | Quest, NPC, object, and item tables for TBC content |
| `Database/QuestXP/xpDB-tbc.lua` | Quest XP reward data |
| `Database/Corrections/` | TBC quest/NPC/item/object corrections and Classic reputation fixes |
| `Loader.lua` | Plugin entry point — registers data via `QuestiePluginAPI` |

---

## How It Works

`Loader.lua` fires on `PLAYER_LOGIN` and registers the full TBC dataset with `QuestiePluginAPI`. Questie-X merges this data into its runtime database at init time, enabling full quest tracking, map pins, and tooltip support for all TBC content.

---

## Contributing

Submit quest data corrections, NPC fixes, or missing entries via pull request. See the existing correction files under `Database/Corrections/` for the expected format.

---

## License

MIT License