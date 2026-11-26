---
title: "Steam ROM Manager Parses ROMs but No Shortcuts Appear in Gaming Mode"
description: "ROMs parse in Steam ROM Manager but no shortcuts show in Gaming Mode. Follow these checks to diagnose the shortcut handoff and restore your games."
seo_title: "Steam ROM Manager Not Showing Games in Gaming Mode: Fix Parsed ROMs Missing Shortcuts"
seo_description: "ROMs parse in Steam ROM Manager but no shortcuts show in Gaming Mode. Follow these checks to diagnose the shortcut handoff and restore your games."
keywords:
  - "steam rom manager not showing games"
date: 2026-11-26T08:05:15+08:00
publishDate: 2026-11-26T08:05:15+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You're in Gaming Mode on your Steam Deck, EmuDeck has parsed your self-owned ROMs in Steam ROM Manager, but no game shortcuts appear in your library. This is a shortcut handoff failure, not a parsing failure.

## Confirm the parser output
Open Steam ROM Manager and check the Preview tab. If your games are listed there, parsing worked. The issue is that SRM is not writing those entries to Steam's shortcut file. Look at the top-right of the Preview tab: the Save to Steam button must be clicked after every parse. If you only parsed and closed the window, nothing was written.

## Check the shortcut file directly
In Desktop Mode, open the file manager and navigate to `/home/deck/.steam/steam/userdata/<your user ID>/config/shortcuts.vdf`. If this file is missing or its timestamp is older than your last parse, SRM never saved. Reopen SRM, parse again, and click Save to Steam. Wait for the confirmation message before closing.

## Verify Gaming Mode refresh
Return to Gaming Mode and open your library. If shortcuts still do not appear, restart the Steam client from the Power menu. This forces Steam to reload the shortcut file. After restart, check the Non-Steam tab in your library.

## Verification test
Launch one shortcut from the Non-Steam tab. If it starts the emulator with your ROM, the handoff is fixed. If it fails, the shortcut exists but points to a broken path.

## Rollback note
If you accidentally saved duplicate or broken shortcuts, delete them from the Non-Steam tab in Gaming Mode before re-parsing. This prevents clutter and repeated failures.

If these steps do not resolve your **steam rom manager not showing games** issue,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) with your shortcuts.vdf timestamp and SRM preview screenshot.
