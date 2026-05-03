# Installing idv-agents

The primary install path is the **Claude Cowork UI** in the Claude desktop app. There's an offline backup if WiFi flakes, and a Claude Code CLI alternative if that's how you run Claude.

## Prerequisites

- **Claude desktop app installed**, with the **Cowork** tab available. Get it from [claude.ai](https://claude.ai) if you don't have it.
- **A paid Claude account.** This plugin runs on your tokens, not IDV's.

---

## Install (Cowork UI — recommended, ~1 minute)

1. Open the Claude desktop app and switch to the **Cowork** tab.
2. Click **Customize** in the left sidebar.
3. Under **Personal plugins**, click the **+** (Add plugin) button.
4. Choose **Create plugin**, then **Add marketplace**.
5. In the **Add marketplace** modal, enter `atomicobject/idv-agents` and click **Sync**. (The repo is public on GitHub.)
6. The **Directory** modal opens automatically once Sync succeeds. In the left sidebar, select **Plugins** → the **Personal** tab → the **idv-agents** sub-tab.
7. Click the **+** next to **Idv agents** to install. You should see a confirmation that the plugin is installed.

That's it. Skip to **Verifying it worked** below.

---

## Offline install (backup for flaky WiFi)

If venue WiFi is dead or you want to install from a pre-downloaded release:

1. Before the workshop, download the latest release zip from [github.com/atomicobject/idv-agents/releases](https://github.com/atomicobject/idv-agents/releases).
2. In Cowork → **Customize** → **Personal plugins**, use the **upload a custom plugin file** option (per Anthropic's [Use plugins in Claude Cowork](https://support.claude.com/en/articles/13837440-use-plugins-in-claude-cowork) support article) and select the downloaded file.

If the upload entry point isn't accepting the release zip, fall back to adding the unzipped folder as a local marketplace via the same **Add marketplace** modal in the online flow above (paste the local filesystem path instead of `atomicobject/idv-agents`). On Mac you can drag a folder into Terminal to get its path.

---

## Verifying it worked

In any Cowork chat, type `/` and start typing `pitch` — you should see `/pitch-deck-review` in the autocomplete. The same goes for `/kpi-recommendations`, `/diligence-gaps`, and `/meeting-prep`.

For natural-language triggering: try saying *"Claude, can you review my pitch deck?"* — Claude should offer to use the `pitch-deck-review` skill.

---

## Alternative: Claude Code CLI

If you're using the Claude Code CLI rather than the desktop app's Cowork tab, install via slash commands instead:

```
/plugin marketplace add atomicobject/idv-agents
/plugin install idv-agents@idv-agents
```

Verify with:

```
/plugin list
```

You should see `idv-agents` in the active list. Same `/`-autocomplete check applies.

---

## Troubleshooting

**"Sync failed" or marketplace doesn't appear after entering `atomicobject/idv-agents`:**
- Double-check the spelling — it's `atomicobject/idv-agents` (no typo).
- Confirm you have network access; the Sync step pulls from GitHub.
- Make sure the Claude desktop app is updated to a recent version.

**Plugin installed but `/pitch-deck-review` etc. don't appear in `/` autocomplete:**
- Open a fresh Cowork chat — some plugin loads need a new session to register commands.
- Re-open the Customize panel and confirm **Idv agents** still shows as installed.

**WebFetch errors when running `/meeting-prep`:**
- The skill asks before fetching public sources. If a fetch fails (paywall, login wall, JS-heavy site), the skill falls back to "FOUNDER TO RESEARCH" markers. That's expected — paste the content yourself or skip that section.

**For general Cowork-plugin issues outside the IDV-specific install:** see Anthropic's [Use plugins in Claude Cowork](https://support.claude.com/en/articles/13837440-use-plugins-in-claude-cowork) support article.

**Still stuck:** during the May 13 workshop, flag down anyone with an Atomic Object name tag. Outside of that, file an issue at [github.com/atomicobject/idv-agents/issues](https://github.com/atomicobject/idv-agents/issues).

---

## Uninstalling

If you ever want to remove the plugin: in Cowork → **Customize** → **Personal plugins**, find **Idv agents** and uninstall it from the Directory. To also remove the marketplace, remove the **idv-agents** entry from the same Directory view.

If you installed via the Claude Code CLI instead:

```
/plugin uninstall idv-agents
/plugin marketplace remove idv-agents
```
