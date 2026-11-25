---
title: "EmuDeck Saves Not Syncing: Why the Emulator Starts with an Empty Slot"
description: "Troubleshoot EmuDeck saves not syncing on Steam Deck. Check save paths, verify migration, and recover your old save before the emulator overwrites it."
seo_title: "EmuDeck Saves Not Syncing: Fix the Empty Slot in Gaming Mode"
seo_description: "Troubleshoot EmuDeck saves not syncing on Steam Deck. Check save paths, verify migration, and recover your old save before the emulator overwrites it."
keywords:
  - "emudeck saves not syncing"
date: 2026-11-25T10:06:00+08:00
publishDate: 2026-11-25T10:06:00+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You are in Gaming Mode on your Steam Deck, you open an emulator through EmuDeck, and the game starts with an empty save slot even though you know a save file exists in the old location.

## Confirm Where the Save Actually Lives

Before changing anything, open the emulator's save folder in Desktop Mode. For most EmuDeck setups, saves live under `Emulation/saves/<system>/`. Check the file's modified date and size. If the file is there but the emulator ignores it, the emulator is likely reading a different path, such as a per-game folder or a portable config directory. Note the exact path the emulator expects in its settings.

## Check the Migration Step

EmuDeck's save migration only runs when it detects a supported old location. If you moved ROMs or saves manually, the migration step may have been skipped. Compare the old save filename with the expected name in the new folder. A mismatch, such as a different region tag or extension, will cause an empty slot. Rename a copy to match exactly, then relaunch.

## Verification Test

Create a new in-game save, exit fully, and check whether a new file appears in the expected folder. If it does, your old save is simply in the wrong place. Copy it beside the new file using the same naming pattern, relaunch, and confirm the slot loads.

## Rollback and Recovery

Keep a backup of the original save before renaming or copying. If the emulator overwrites the slot, restore your backup and repeat the path check. This is the most common cause of **emudeck saves not syncing** and is usually resolved by aligning the filename and folder.

If the path still does not match after these checks,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) with your folder listing and emulator settings.
