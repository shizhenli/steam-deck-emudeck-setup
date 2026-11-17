---
title: "Steam Deck SD Card Not Detected or Read-Only: A Controlled Diagnosis"
description: "Step-by-step diagnosis for when your Steam Deck cannot see the SD card or mounts it read-only in Gaming Mode with EmuDeck. Includes checks, verification, and recovery."
seo_title: "Steam Deck SD Card Not Detected or Read-Only: Fix in Gaming Mode"
seo_description: "Step-by-step diagnosis for when your Steam Deck cannot see the SD card or mounts it read-only in Gaming Mode with EmuDeck. Includes checks, verification, and recovery."
keywords:
  - "steam deck sd card not detected"
date: 2026-11-17T10:05:52+08:00
publishDate: 2026-11-17T10:05:52+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You're in Gaming Mode with EmuDeck and your ROMs on a microSD card, but the Deck either ignores the card or mounts it read-only, and you want to restore normal read-write access before touching your library.

## First, confirm what the Deck actually sees

Insert the card, then open Settings > System > Storage. Under the microSD section, note whether it shows a capacity and a mount state, or says "Not detected." If it shows a size but the state is read-only, the card is recognized but the filesystem or lock switch is the problem. If it shows nothing, the card is not being enumerated at all.

## Check the physical and filesystem basics

Power off, remove the card, and inspect the contacts and the write-protect notch on the adapter if you use one. Reinsert until it clicks. Boot and check Storage again. If still read-only, the filesystem may be dirty or unsupported; back up what you can from a PC, then format the card from the Deck's Storage menu (this erases it). If the Deck still reports nothing, test the card in a PC reader to separate a card fault from a Deck slot fault.

## Verification test

After formatting or reseating, copy a small ROM to the card from Desktop Mode, eject safely, and confirm it appears in EmuDeck's ROM folder in Gaming Mode. If the copy succeeds and the file is visible, read-write access is restored.

## Rollback and recovery

If formatting fails or the card disappears again, stop and do not reformat repeatedly. Keep your original ROM backup intact, and if the card is readable on a PC, copy your EmuDeck saves and ROMs off before any further steps. A card that mounts read-only on two different devices is failing and should be replaced.

If the **steam deck sd card not detected** state persists after these checks,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) with your Storage screen details and whether a PC can read the card.
