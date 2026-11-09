# AuraLab

AuraLab sets up your Mac for the AURA Lab's AI tools (Claude Code and DeepSeek Harness, running on the lab's GPU
servers) and then opens them for you every day.

This repository holds only the downloads and the update feed. The source code is private.

## Install (macOS 12 or later, Apple Silicon or Intel)

1. Download the `.dmg` from the [latest release](https://github.com/aura-lab-wm/auralab-releases/releases/latest).
2. Open it and drag **AuraLab v1** to **Applications**.
3. Open **AuraLab v1** from Applications. This build is not notarized by Apple yet, so macOS blocks the first open.
   Go to **System Settings → Privacy & Security**, find the line about AuraLab v1 and click **Open Anyway**.
   You do this once.
4. Follow the setup. Your instructor gives you the server address and your username. At the end the app shows an
   SSH key; send it to your instructor.

## Updates

AuraLab checks this repository for new versions and offers to install them. Every update is signed, and the app
refuses one whose signature does not match.

## Uninstall

In Terminal:

```
"/Applications/AuraLab v1.app/Contents/MacOS/auralab-app" uninstall
```

then drag AuraLab v1 from Applications to the Trash.
