---
title: "EmuDeck Saves Not Migrating: Why the Emulator Starts Empty and How to Fix It"
description: "A save exists in the old location but the emulator starts with an empty slot. Follow these checks to diagnose why saves fail to migrate in EmuDeck on Steam Deck."
seo_title: "Fix EmuDeck Saves Not Migrating on Steam Deck (Empty Slot)"
seo_description: "A save exists in the old location but the emulator starts with an empty slot. Follow these checks to diagnose why saves fail to migrate in EmuDeck on Steam Deck."
keywords:
  - "emudeck migrate saves"
date: 2026-11-28T21:51:33+08:00
publishDate: 2026-11-28T21:51:33+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You are in Gaming Mode on your Steam Deck, you have EmuDeck set up with your own ROMs, and a save file clearly exists in the old location, yet the emulator opens with an empty slot. That usually means the migration step has not actually completed, not that the save is gone.

## Confirm the save location and emulator path

First, open the emulator's save folder in Desktop Mode and note the exact file name and extension. Then check the emulator's configured save directory. If the emulator is pointed at a different folder than the one holding your save, it will always show an empty slot. Result interpretation: if the paths differ, the save was never in the location the emulator reads.

## Check whether the migration ran to completion

Open EmuDeck and look at the save migration status. If it reports pending or skipped, the **emudeck migrate saves** step did not finish. Do not re-run it blindly; instead confirm the source folder is readable and the target folder exists. If the target folder is missing, create it and run the migration again.

## Verification test

Copy one save file manually into the emulator's active save directory, launch the game, and load the slot. If the save appears, the emulator path is correct and the migration is the failing part. If it still shows empty, the file name or extension does not match what the emulator expects.

## Rollback and recovery

Before changing anything, back up the original save folder to a separate location. If a migration attempt leaves duplicates or partial files, restore that backup and start the diagnosis again from the confirmed path.

If the paths match and the file is valid but the slot stays empty,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult).
