---
title: "EmuDeck Migrate Saves: When a Save Exists but the Emulator Loads an Empty Slot"
description: "Troubleshoot emudeck migrate saves when a save file exists in the old location but the emulator starts with an empty slot on Steam Deck Gaming Mode."
seo_title: "Fix emudeck migrate saves: Save Exists but Emulator Loads Empty Slot"
seo_description: "Troubleshoot emudeck migrate saves when a save file exists in the old location but the emulator starts with an empty slot on Steam Deck Gaming Mode."
keywords:
  - "emudeck migrate saves"
date: 2026-11-17T11:05:53+08:00
publishDate: 2026-11-17T11:05:53+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You are in Gaming Mode on your Steam Deck, EmuDeck is set up with your own ROMs, and you have reached the saves do not migrate step: a save file clearly exists in the old location, yet the emulator opens with an empty slot.

## Confirm the save file and expected path

First, verify the save exists and note its exact filename and folder. In Desktop Mode, open the file manager and navigate to the emulator's save directory under EmuDeck. Check that the file is not zero bytes and that its extension matches the emulator's expected format. If the file is present but the emulator shows an empty slot, the emulator is likely reading a different path than the one you inspected.

## Check where the emulator actually reads saves

Launch the emulator directly in Desktop Mode, not through Gaming Mode. Open its settings and locate the configured save directory. Compare that path character by character with the folder containing your save. A common cause is a mismatch between the portable and standard save folders, or a per-game save subfolder the emulator expects but does not find. If the paths differ, that explains why **emudeck migrate saves** appears to fail: the migration may have completed, but the emulator is pointed elsewhere.

## Verification test

Copy the save into the path the emulator reports, then launch the same game and load the slot. If the save appears, the original location was wrong. Remove the copy afterward to avoid duplicates.

## Rollback note

Before changing paths, back up the save folder. If the emulator still shows an empty slot, restore the backup and

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) with both paths and the filename.
