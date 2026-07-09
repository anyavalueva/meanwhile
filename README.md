# Meanwhile

A tiny macOS menu bar app for people who run long Claude Code tasks. When a
task starts, one small thing appears — a word to learn, a flag to name, a
game of snake — and the moment the task finishes, it clears and puts your
terminal back. It only ever knows *that* a task started or stopped, never
what the task was.

**Free while in beta.**

## Download

Grab the latest **[Meanwhile.dmg from Releases](../../releases/latest)**,
open it, and drag Meanwhile into Applications.

**First launch:** because this beta isn't notarized by Apple yet, macOS will
block it the first time. Click **Done** on the warning, then open **System
Settings → Privacy & Security**, scroll to Security, and click **Open Anyway**.
You only do this once.

(Terminal shortcut, if you prefer: `xattr -dr com.apple.quarantine /Applications/Meanwhile.app`)

## Connect Claude

On first launch Meanwhile offers to connect. One click wires up both Claude
Code (CLI) and the Claude desktop app so it can tell when a task starts and
stops. It writes a couple of hook lines to `~/.claude/settings.json` that
carry only a session id — never your prompts or Claude's output — and you
can disconnect any time from Settings. Restart any open Claude sessions
afterwards so they pick it up.

## What it does

- **Notices** a task is taking a while (a few seconds' debounce, and only if
  you're still in the app you launched it from).
- **Offers one thing** — a Spanish flashcard, a world flag, a word origin, a
  piece of public-domain art, a thirty-second breath, or a game of snake.
- **Puts you back** the instant the task finishes, with a quiet tally of what
  you did. It never yanks you out of another app you switched to.

Everything runs locally. No account, no telemetry, nothing leaves your Mac.

## Requirements

macOS 14 or later · Apple Silicon or Intel

---

*Editions — deeper themed sets that load into an activity — are coming soon.
The site: [anyavalueva.github.io/meanwhile](https://anyavalueva.github.io/meanwhile)*
