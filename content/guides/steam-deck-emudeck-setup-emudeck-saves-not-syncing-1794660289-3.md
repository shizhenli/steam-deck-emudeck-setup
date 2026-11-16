---
title: "EmuDeck Saves Not Syncing: Fix the Empty Slot Before Migration"
description: "Troubleshoot EmuDeck saves not syncing on Steam Deck Gaming Mode when a save exists in the old location but the emulator starts with an empty slot."
seo_title: "EmuDeck Saves Not Syncing: Fix the Empty Slot Before Migration"
seo_description: "Troubleshoot EmuDeck saves not syncing on Steam Deck Gaming Mode when a save exists in the old location but the emulator starts with an empty slot."
keywords:
  - "emudeck saves not syncing"
date: 2026-11-16T08:05:49+08:00
publishDate: 2026-11-16T08:05:49+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You are in Gaming Mode on your Steam Deck, using EmuDeck with self-owned ROMs, and the emulator opens with an empty save slot even though the save file still sits in the old location. This is the moment before a controlled diagnosis, so we will verify the save path and emulator config rather than move files blindly.

## Confirm the save file and expected path

Open the emulator's save folder in Desktop Mode or a file manager. For most EmuDeck setups, saves live under Emulation/saves/<system>/, while some emulators use Emulation/storage/<emulator>/. Note the exact filename and extension. Then check the emulator's save directory setting: it must point to that same folder. If the file is present but the emulator points elsewhere, the slot will appear empty. Also confirm the ROM name matches the save name exactly, including region tags.

## Check the migration state

Look for a pending migration marker or a backup folder created by EmuDeck. If a backup exists but the active save folder is empty, the migration did not complete. Do not delete the backup. This is the usual cause of **emudeck saves not syncing** in Gaming Mode.

## Verification test

Copy the save file into the emulator's configured save directory, launch the game, and load the slot. If the save appears, the path was the issue. If it still fails, rename the save to match the ROM exactly and retest.

## Rollback and recovery

Before changing anything, copy the original save to a safe folder outside Emulation. If the emulator creates a new empty save, restore your backup over it and recheck the path setting.

If the slot remains empty after these checks,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) with your folder listing and emulator path.
