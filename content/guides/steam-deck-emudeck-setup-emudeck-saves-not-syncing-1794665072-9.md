---
title: "EmuDeck Saves Not Syncing: When the Save Exists but the Emulator Starts Empty"
description: "Troubleshooting guide for when EmuDeck saves do not migrate and an emulator starts with an empty slot despite the save existing in the old location."
seo_title: "Fix EmuDeck Saves Not Syncing on Steam Deck Gaming Mode"
seo_description: "Troubleshooting guide for when EmuDeck saves do not migrate and an emulator starts with an empty slot despite the save existing in the old location."
keywords:
  - "emudeck saves not syncing"
date: 2026-11-21T15:49:53+08:00
publishDate: 2026-11-21T15:49:53+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You are in Gaming Mode on your Steam Deck, EmuDeck is set up with your own ROMs, and a save file clearly exists in the old folder, yet the emulator opens to an empty slot. This is the classic **emudeck saves not syncing** symptom, and it almost always means the emulator is reading a different save directory than the one you are inspecting.

## Confirm where the emulator actually looks

Open EmuDeck and check the save path shown for the affected emulator. Then launch the emulator once, save nothing, and close it. Use a file manager in Desktop Mode to compare the modification timestamp of the save you found against the folder the emulator reports. If the timestamps differ, the emulator is not reading that file at all. If the file is present but named differently (for example a region or revision suffix), rename it to match the emulator's expected filename exactly.

## Check the sync layer

If you use a cloud or network sync tool, confirm it is not paused or pointing at the old path. A paused sync leaves the old file in place while the emulator reads an empty new directory. Resume it and let one full cycle finish before testing.

## Verification test

Create a throwaway in-game save in the emulator, close it, and locate that new file. If it appears in a different folder than your original save, move the original into that folder, keeping a backup copy. Relaunch and confirm the slot loads.

## Rollback note

Before moving anything, copy the original save to a separate backup folder. If the emulator still shows an empty slot, restore the backup and stop moving files until the path is confirmed. For a guided diagnosis,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult).
