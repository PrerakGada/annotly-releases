# Annotly

A menu-bar app for drawing on top of the live screen while you present, teach or explain. Mark up whatever is
showing with a pen, arrows, shapes, number badges and Markdown text, click through to the apps underneath while the
marks stay, and save the marked-up screen to a library you can reopen later with the marks still editable. Also has a
whiteboard, a cursor highlight, a spotlight and a zoom lens, and an `annotly` command for scripts.

This repository only holds the signed downloads. Website: <https://annotly.prerakgada.in/>

## This is an alpha

Annotly 0.1.1 remains an alpha. It is signed and notarized by Apple and passes its own automated checks, but those
run against stand-ins for the screen: drawing over the real screen, clicking through, the global shortcuts and the
cursor effects have not yet had real use. Expect rough edges, and keep another way to present at hand until Annotly
has earned its place. There is no in-app updater: update with `brew upgrade --cask annotly` or the newest disk image.

The known gaps are listed in each [release](https://github.com/PrerakGada/annotly-releases/releases).

## Requirements

- A Mac with Apple Silicon (M1 or later)
- macOS 26 or newer

## Install

With Homebrew:

```sh
brew install --cask prerakgada/tap/annotly
open -a Annotly
```

Homebrew also links the `annotly` command-line tool.

Or [download the DMG](https://github.com/PrerakGada/annotly-releases/releases/download/v0.1.1/Annotly-0.1.1.dmg):

1. Open the downloaded disk image.
2. Drag **Annotly** onto the **Applications** shortcut.
3. Open Annotly from Applications, then eject the disk image.

Annotly lives in the menu bar. Press ⌃⌥D to start drawing; Esc stops. Every shortcut can be changed in Settings.

Checksums (SHA-256) are attached to every [release](https://github.com/PrerakGada/annotly-releases/releases).

## Permissions

Annotly asks for nothing when it starts, and never needs Accessibility.

- **Screen Recording** is needed only to save the screen under your marks (Save snap) and for the zoom lens. It is
  requested when you press its button in the welcome window, the snap explainer or Settings. Without it, Save snap
  keeps your marks on a transparent background.
- **Pictures, Desktop, Documents or Downloads**: macOS asks once if you choose to also save snaps to one of those
  folders.
- **Launch at login** is off until you turn it on in Settings.

## Privacy

Your marks and snaps stay on your Mac, in `~/Library/Application Support/Annotly` (and in a folder you choose, if you
turn that on). Nothing is uploaded. Annotly has no account, no analytics and no telemetry, and does not check for
updates. Its only network request is the feedback you send from Report a Problem… or Send Feedback…, and only when you
press Send: your message, the name and email if you added them, and the Annotly version, macOS version and Mac model.
The server notes a rough location (country, region and city) from your connection and stores no IP address.

## Uninstall

```sh
brew uninstall --cask annotly          # or quit Annotly and drag Annotly.app to the Bin
brew uninstall --zap --cask annotly    # also removes its library and settings (never snaps saved to your folders)
```

---

© 2026 Engaze
