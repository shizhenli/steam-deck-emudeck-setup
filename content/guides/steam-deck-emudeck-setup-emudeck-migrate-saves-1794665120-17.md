---
title: "EmuDeck Migrate Saves Stuck: When the Emulator Opens an Empty Slot"
description: "Troubleshoot EmuDeck save migration on Steam Deck when a save exists in the old location but the emulator starts with an empty slot. Step-by-step checks and verification."
seo_title: "EmuDeck Migrate Saves Not Working: Fix Empty Save Slot on Steam Deck"
seo_description: "Troubleshoot EmuDeck save migration on Steam Deck when a save exists in the old location but the emulator starts with an empty slot. Step-by-step checks and verification."
keywords:
  - "emudeck migrate saves"
date: 2026-11-22T10:06:04+08:00
publishDate: 2026-11-22T10:06:04+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You are in Gaming Mode on your Steam Deck, you know a save file exists in the old EmuDeck folder, but the emulator opens to an empty slot.

## Confirm the save location and emulator path

First, switch to Desktop Mode and open the EmuDeck save folder. Locate the specific save file for the game and note its exact filename and extension. Then open the emulator's own save directory and compare. If the file is missing there, migration has not completed. If it exists but has a different name or extension, the emulator will not load it.

## Check the migration target

In EmuDeck, open the save migration tool and confirm the source and destination paths. A common cause is that the destination points to a different emulator profile or a folder the emulator does not read. Verify the destination matches the emulator's configured save path exactly, including case sensitivity.

## Run a controlled test

Copy one save file manually into the emulator's save folder, launch the game, and check whether it appears. If it loads, the file is valid and the issue is the migration step. If it does not, the emulator is reading a different directory.

## Verify and recover

After correcting the path, run **emudeck migrate saves** again, then launch the game and confirm the save appears. If migration still fails, restore your original save from backup before making further changes, so you do not lose progress.

If the empty slot persists after these checks,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) with your folder paths and filenames.
