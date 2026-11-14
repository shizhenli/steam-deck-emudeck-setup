---
title: "Steam Deck SD Card Not Detected: Diagnose Gaming Mode Mount Issues"
description: "Troubleshoot a Steam Deck SD card that is not detected or mounts read-only in Gaming Mode with EmuDeck. Step-by-step checks, verification, and recovery."
seo_title: "Steam Deck SD Card Not Detected: Fix Read-Only or Missing Card"
seo_description: "Troubleshoot a Steam Deck SD card that is not detected or mounts read-only in Gaming Mode with EmuDeck. Step-by-step checks, verification, and recovery."
keywords:
  - "steam deck sd card not detected"
date: 2026-11-14T19:38:39+08:00
publishDate: 2026-11-14T19:38:39+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You're in Gaming Mode, EmuDeck is set up, your ROMs are on a microSD card, and the Deck either ignores the card or mounts it read-only, blocking your setup.

## Confirm the card is seen at the hardware level

Power off, remove the microSD, and inspect the slot for dust or a bent pin. Reinsert until it clicks. Boot into Desktop Mode and open the file manager: if the card appears but is read-only, the filesystem is likely dirty or corrupted; if it never appears, suspect the card or slot. In Gaming Mode, open Settings > Storage and check whether the card is listed.

## Check the filesystem and lock state

The microSD's physical lock switch (on the adapter, if used) must be off. In Desktop Mode, open KDE Partition Manager and look at the card's partition table. A card formatted exFAT or ext4 should mount read-write; if it shows read-only, unmount it, then run a filesystem check. For exFAT, use the terminal command sudo fsck.exfat /dev/mmcblk0p1 (confirm the device name first). For ext4, use sudo e2fsck -f /dev/mmcblk0p1. If errors are repaired, remount and confirm write access by creating a test folder.

## Verification test

Copy a small file to the card, eject safely, reinsert, and confirm the file persists. Then launch EmuDeck and check that your ROM path is visible. If the card still does not appear, try a different known-good microSD; if that also fails, the slot needs service.

## Recovery note

If a repair makes things worse, back up what you can first. Reformatting erases data, so restore ROMs from your own backup afterward. For a second opinion on this **steam deck sd card not detected** issue,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult).
