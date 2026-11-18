---
title: "EmuDeck Saves Not Syncing: Fix the Empty Slot After Migration"
description: "Troubleshoot EmuDeck saves not syncing on Steam Deck Gaming Mode: verify save paths, fix migration, and test with a known save."
seo_title: "EmuDeck Saves Not Syncing: Fix Empty Slot After Migration"
seo_description: "Troubleshoot EmuDeck saves not syncing on Steam Deck Gaming Mode: verify save paths, fix migration, and test with a known save."
keywords:
  - "emudeck saves not syncing"
date: 2026-11-18T11:13:05+08:00
publishDate: 2026-11-18T11:13:05+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You copied your old save into EmuDeck's save folder, but the emulator still boots to an empty slot, and you are stuck at the saves do not migrate step before running a controlled diagnosis.

## Check the emulator's actual save path

In Gaming Mode, open the emulator and load the game. Then use its in-game save menu to create a new save, note the filename, and exit. Switch to Desktop Mode and compare that filename with the file you placed in EmuDeck's saves directory. If the names differ, the emulator is writing to a different path than you assumed, which explains why **emudeck saves not syncing** appears as an empty slot.

## Confirm the file is in the right folder

EmuDeck stores saves under its own directory, not the emulator's default. Verify the file sits in the EmuDeck saves folder for that system, not in a backup or ROM folder. If it is misplaced, move it into the correct EmuDeck saves subfolder and keep a copy of the original.

## Verification test

Relaunch the game in Gaming Mode and check the load menu. If the save now appears, the path was the issue. If it still does not, rename the file to match the emulator's new save exactly and retest once.

## Rollback note

Before renaming or moving anything, copy the original save to a separate backup folder. If the emulator fails to read it, restore that backup and stop editing until you confirm the correct path.

If the slot remains empty after these checks,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) with your folder listing and the save filename.
