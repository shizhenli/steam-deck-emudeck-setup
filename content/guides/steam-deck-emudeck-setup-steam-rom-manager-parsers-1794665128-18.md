---
title: "Steam ROM Manager Parsers: Why Parsed ROMs Don't Appear in Gaming Mode"
description: "Steam Deck in Gaming Mode with EmuDeck: SRM shows parsed ROMs but no shortcuts appear. Diagnose parser output, save, and Steam library sync without guesswork."
seo_title: "Steam ROM Manager Parsers: Fix Parsed ROMs Missing in Gaming Mode"
seo_description: "Steam Deck in Gaming Mode with EmuDeck: SRM shows parsed ROMs but no shortcuts appear. Diagnose parser output, save, and Steam library sync without guesswork."
keywords:
  - "steam rom manager parsers"
date: 2026-11-22T11:06:09+08:00
publishDate: 2026-11-22T11:06:09+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You're in Gaming Mode on your Steam Deck, EmuDeck is set up, your own ROMs are on the SD card, and Steam ROM Manager clearly lists them—yet no shortcuts show up in your Steam library. That points to a parser output or save step, not a missing ROM.

## Check what the parsers actually produce

Open Steam ROM Manager and go to the Parsers tab. Run only the parser for the system you care about, then read the preview list. If games appear there, the **steam rom manager parsers** are reading the ROM path correctly. If the preview is empty, the parser's ROM directory is wrong—fix that path first, because nothing downstream can work.

Next, look at the parser's title and executable fields. A parser that points to a missing emulator or a stale AppImage path will still list games but fail to generate usable shortcuts. Confirm the executable path matches the emulator EmuDeck installed.

## Save and confirm the handoff

After a successful preview, click Save to Steam. Watch for an error banner; a permissions or Steam-not-running message means the save never completed. Then return to Gaming Mode and check the non-Steam section of your library, not just the recent list.

## Verification test

Pick one game, add it manually through SRM's save again, then fully restart Steam (power menu, restart) rather than just switching modes. If that single shortcut appears, your parser config is sound and the earlier save was incomplete.

## Rollback note

Before changing parser paths, export your SRM configuration. If shortcuts disappear entirely after an edit, re-import the previous config and re-save.

If the preview stays correct but Gaming Mode still shows nothing after a restart, stop repeating saves and

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) with your parser preview and save log.
