---
title: "Steam Deck SD Card Not Detected: Fix Read-Only or Missing Mount"
description: "Troubleshoot a Steam Deck SD card that is not detected or mounts read-only in Gaming Mode with EmuDeck. Step-by-step checks and a verification test."
seo_title: "Steam Deck SD Card Not Detected: Fix Read-Only Mount"
seo_description: "Troubleshoot a Steam Deck SD card that is not detected or mounts read-only in Gaming Mode with EmuDeck. Step-by-step checks and a verification test."
keywords:
  - "steam deck sd card not detected"
date: 2026-11-21T15:46:48+08:00
publishDate: 2026-11-21T15:46:48+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You're in Gaming Mode with EmuDeck, your ROMs are on a self-owned SD card, and the Deck either can't see the card or mounts it read-only, blocking your setup.

## Confirm the card is seated and recognized
Power off fully, then reinsert the SD card until it clicks. Boot into Gaming Mode and open Settings > Storage. If the card appears but shows read-only, skip to the next section. If it doesn't appear at all, remove it and check the contacts for dust or damage. Reinsert and check Storage again. A card that never appears here is not being detected at the hardware level, so EmuDeck cannot use it.

## Rule out a read-only filesystem
If the card appears but is read-only, the filesystem may have been mounted with write protection after an unsafe removal. In Desktop Mode, open a terminal and run `sudo dmesg | grep mmc` to see mount errors. Then run `sudo fsck /dev/mmcblk0p1` and answer yes to repairs. Reboot into Gaming Mode and check Storage. If it still mounts read-only, back up your ROMs and saves to internal storage or a PC, then reformat the card from Settings > Storage. Reformatting erases the card, so this is your rollback point: restore your backup afterward.

## Verification test
Create a test folder on the SD card in Desktop Mode, then return to Gaming Mode and confirm it appears in Storage. Launch one EmuDeck game from the card. If the folder persists and the game loads, the mount is writable and stable. If the folder disappears or the game fails, the card is failing and should be replaced.

If these steps don't resolve your **steam deck sd card not detected** issue,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) before reformatting again.
