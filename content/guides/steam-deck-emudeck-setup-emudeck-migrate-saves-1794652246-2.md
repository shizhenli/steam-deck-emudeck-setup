---
title: "EmuDeck Saves Not Migrating: Fix the Empty Slot"
description: "Troubleshoot EmuDeck saves that fail to migrate on Steam Deck by verifying folder paths, checking emulator save directories, and testing with a manual copy."
seo_title: "EmuDeck Migrate Saves Not Working: Fix Empty Save Slot"
seo_description: "Troubleshoot EmuDeck saves that fail to migrate on Steam Deck by verifying folder paths, checking emulator save directories, and testing with a manual copy."
keywords:
  - "emudeck migrate saves"
date: 2026-11-15T18:57:30+08:00
publishDate: 2026-11-15T18:57:30+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You are in Gaming Mode on your Steam Deck, and after running the EmuDeck migration, a game still starts with an empty save slot even though the save file exists in the old location.

## Confirm the source and destination paths

First, open the emulator directly and check its save directory. In EmuDeck, saves are normally expected under `/home/deck/Emulation/saves/<system>/`. Compare that with where the save actually sits, often in a flatpak or legacy path such as `~/.var/app/<emulator>/config/`. If the save is not inside the EmuDeck saves folder, the migration had nothing to move. If it is there but the emulator reads a different path, the emulator is pointed at the old location.

## Check the emulator's configured save path

Launch the emulator in Desktop Mode and open its settings. Confirm the save directory matches the EmuDeck path. If it still points to the old folder, the emulator will ignore the migrated copy. Note the exact folder name and file extension; a mismatched extension or region code will also cause an empty slot.

## Verification test

Copy one save file manually into the emulator's active save folder, launch the game, and load the slot. If it appears, the migration step did not complete for that system. If it still does not appear, the emulator is reading a different directory than you expect.

## Rollback and recovery

Before changing paths, back up the save folder to your SD card or a PC. If a manual copy causes conflicts, restore the backup and retry the **emudeck migrate saves** step after correcting the emulator path.

If the path still will not resolve,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) with your folder listing and emulator settings.
