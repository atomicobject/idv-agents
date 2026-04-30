# Installing idv-agents

Two paths: **online** (recommended) and **offline** (backup if WiFi flakes).

## Prerequisites

Both paths assume:

- **Claude Cowork is installed.** Get it from claude.ai if you don't have it.
- **You have a paid Claude account.** This plugin runs on your tokens, not IDV's.
- **You're starting Claude Cowork in a folder of your choice** (your projects directory, or a fresh folder for the workshop — either is fine).

---

## Online install (recommended — ~1 minute)

In Claude Cowork, run these two slash commands in order:

```
/plugin marketplace add atomicobject/idv-agents
```

You should see something like *"Marketplace `idv-agents` added."* Then:

```
/plugin install idv-agents@idv-agents
```

You should see *"Plugin `idv-agents` installed."*

That's it. To verify:

```
/plugin list
```

You should see `idv-agents` in the active list.

---

## Offline install (backup)

If venue WiFi is dead or you want to install from a pre-downloaded zip:

1. Download the latest zip from [github.com/atomicobject/idv-agents/releases](https://github.com/atomicobject/idv-agents/releases) (download to your Downloads folder, or wherever).
2. Unzip it. You'll get a folder named something like `idv-agents-1.0.0/`.
3. In Claude Cowork:
   ```
   /plugin marketplace add /path/to/idv-agents-1.0.0
   /plugin install idv-agents@idv-agents
   ```
   (Use the actual path to the unzipped folder. On Mac you can drag the folder into Terminal to get the path, then copy it.)

Verify the same way: `/plugin list` should show `idv-agents`.

---

## Verifying the skills work

Type a slash and start typing `pitch` — you should see `/pitch-deck-review` in the autocomplete. Same for `/kpi-recommendations`, `/diligence-gaps`, `/meeting-prep`.

For natural-language triggering: try saying *"Claude, can you review my pitch deck?"* — Claude should offer to use the `pitch-deck-review` skill.

---

## Troubleshooting

**"Marketplace not found" after `marketplace add`:**
- Double-check the spelling — it's `atomicobject/idv-agents` (no typo).
- Make sure your Claude Cowork is updated to a version that supports plugin marketplaces.

**`/plugin list` doesn't show idv-agents after install:**
- Try `/reload-plugins` (re-scans all installed plugins from their source directories without restarting Claude Code).
- If that doesn't work, restart Claude Cowork.

**Slash commands don't appear in autocomplete:**
- After install, try restarting Claude Cowork once. Some plugin loads need a fresh session to register commands.

**WebFetch errors when running meeting-prep:**
- The skill will ask before fetching public sources. If a fetch fails (paywall, login wall, JS-heavy site), the skill falls back to "FOUNDER TO RESEARCH" markers. That's expected — paste the content yourself or skip that section.

**Still stuck:** during the May 13 workshop, flag down anyone with an Atomic Object name tag. Outside of that, file an issue at [github.com/atomicobject/idv-agents/issues](https://github.com/atomicobject/idv-agents/issues).

---

## Uninstalling

If you ever want to remove the plugin:

```
/plugin uninstall idv-agents
/plugin marketplace remove idv-agents
```
