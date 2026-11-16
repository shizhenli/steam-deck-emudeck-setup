---
title: "Steam ROM Manager Not Showing Games: Fix Shortcuts Missing in Gaming Mode"
description: "Steam ROM Manager sees your ROMs but Gaming Mode shows no shortcuts? Follow these checks to fix the steam rom manager not showing games issue on Steam Deck."
seo_title: "Steam ROM Manager Not Showing Games: Fix Shortcuts Missing in Gaming Mode"
seo_description: "Steam ROM Manager sees your ROMs but Gaming Mode shows no shortcuts? Follow these checks to fix the steam rom manager not showing games issue on Steam Deck."
keywords:
  - "steam rom manager not showing games"
date: 2026-11-16T11:05:53+08:00
publishDate: 2026-11-16T11:05:53+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You're in Gaming Mode on your Steam Deck, EmuDeck is set up, and Steam ROM Manager (SRM) clearly parses your ROMs, but no shortcuts appear in your Steam library. This is a common disconnect between SRM's preview and what Gaming Mode actually loads.

## Check the SRM Save Step

Open SRM and run a parse. After the preview list populates, look for the Save to Steam button (often labeled "Save App List" or "Add to Steam"). Clicking it is what writes shortcuts to Steam. If you only parsed and closed SRM, nothing was saved. After saving, SRM should show a confirmation. If it errors, note the message.

## Verify Steam Is Fully Closed

SRM writes to Steam's shortcut file, which Steam locks while running. In Gaming Mode, switch to Desktop Mode, fully exit Steam (right-click tray icon > Exit), then run SRM and save again. Reopen Steam and check your library.

## Confirm the Shortcut File

In Desktop Mode, navigate to ~/.steam/steam/userdata/[your ID]/config/shortcuts.vdf. If this file's timestamp doesn't update after saving in SRM, the save didn't reach Steam. Rename it to shortcuts.vdf.bak and re-save from SRM to regenerate it.

## Verification Test

Return to Gaming Mode and check the Non-Steam tab in your library. If shortcuts appear there but not in your main library, your collection filters may be hiding them. Clear filters and search for one ROM by name.

## Rollback Note

If shortcuts appear duplicated or broken after regenerating, restore your shortcuts.vdf.bak file and re-save from SRM with only the parsers you need enabled. This **steam rom manager not showing games** issue is usually a save or Steam-lock problem, not a parser failure. If the shortcut file never updates,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) before deleting anything else.
