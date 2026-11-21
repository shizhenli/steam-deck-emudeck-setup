---
title: "EmuDeck Migrate Saves: Fix the Empty Slot in Gaming Mode"
description: "Troubleshoot EmuDeck save migration on Steam Deck when a save exists in the old location but the emulator starts with an empty slot. Step-by-step checks and verification."
seo_title: "EmuDeck Migrate Saves Not Working: Fix Empty Save Slot"
seo_description: "Troubleshoot EmuDeck save migration on Steam Deck when a save exists in the old location but the emulator starts with an empty slot. Step-by-step checks and verification."
keywords:
  - "emudeck migrate saves"
date: 2026-11-21T15:46:48+08:00
publishDate: 2026-11-21T15:46:48+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You are in Gaming Mode on your Steam Deck, EmuDeck is set up with your own ROMs, and a save file clearly exists in the old location, yet the emulator opens with an empty slot.

## Confirm the emulator's actual save path

First, identify which emulator is launching from the shortcut. In Desktop Mode, open EmuDeck and check the emulator's configured save directory. Then compare it to where your save actually sits. A save in the old location but an empty slot usually means the emulator is reading a different folder than you expect. If the paths differ, that is your fault line: migration did not copy into the active path.

## Check the migration result, not just the source

Look inside the destination save folder for the same filename and extension. If the file is absent, the copy step did not complete. If it is present but the emulator still shows empty, confirm the filename matches the emulator's expected naming exactly, including region or revision tags. A renamed file will be ignored. This is the point where **emudeck migrate saves** should be re-run after you correct the path or filename, rather than manually guessing.

## Verification test

Launch the game, load the save slot, save a trivial change, then exit and relaunch. If the change persists, the active path is correct. If it resets, the emulator is still writing elsewhere.

## Rollback note

Before re-running migration, copy the original save folder to a backup location. If the re-run overwrites or duplicates files, restore from that backup and re-check the configured path.

If the path and filename both check out and the slot is still empty, stop repeating the migration and get a controlled diagnosis:

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult).
