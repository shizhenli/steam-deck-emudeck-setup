---
title: "Steam ROM Manager Parsers Not Adding Shortcuts to Gaming Mode: A Step-by-Step Fix"
description: "Steam ROM Manager sees your ROMs but Gaming Mode shows no shortcuts. Follow these checks to diagnose parser output and restore your Steam Deck shortcuts."
seo_title: "Steam ROM Manager Parsers Not Adding Shortcuts to Gaming Mode: Fix"
seo_description: "Steam ROM Manager sees your ROMs but Gaming Mode shows no shortcuts. Follow these checks to diagnose parser output and restore your Steam Deck shortcuts."
keywords:
  - "steam rom manager parsers"
date: 2026-11-24T12:08:22+08:00
publishDate: 2026-11-24T12:08:22+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You've added your own ROMs to EmuDeck and Steam ROM Manager shows them in the list, but after saving, Gaming Mode still has no shortcuts. Let's walk through this together.

## Check What SRM Actually Wrote

Open Steam ROM Manager and click the Parsers tab. Confirm the parsers you enabled are toggled on and that each one points to the correct ROM folder. Then click Preview. If games appear, the **steam rom manager parsers** are reading files correctly. Now click Save to Steam. Watch for an error toast. If none appears, SRM believes it wrote shortcuts.

## Verify the Shortcuts File

Switch to Desktop Mode. Open the file manager and go to /home/deck/.steam/steam/userdata. Open the folder with the longest number, then config, then shortcuts.vdf. Check the modified timestamp. If it didn't update after your save, SRM is writing to a different Steam user or the file is locked. Close Steam completely, reopen SRM, and save again.

## Test in Gaming Mode

Return to Gaming Mode and open the library. Filter by the emulator category or search for one game by name. If it appears, the fix worked. If not, restart the Deck once to force Steam to reload shortcuts.vdf.

## Rollback Note

Before retrying, back up shortcuts.vdf so you can restore it if a save corrupts the list. If shortcuts still don't appear after these checks, the parser output may be mismatched with your Steam user profile.

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) and we'll review your setup together.
