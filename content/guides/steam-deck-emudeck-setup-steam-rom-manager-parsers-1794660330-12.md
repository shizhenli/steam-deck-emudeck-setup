---
title: "Steam ROM Manager Parsers: Shortcuts Not Appearing in Gaming Mode"
description: "Steam ROM Manager sees your games but Gaming Mode shows no shortcuts? Follow these parser checks to restore your Steam Deck library."
seo_title: "Steam ROM Manager Parsers: Fix Shortcuts Missing in Gaming Mode"
seo_description: "Steam ROM Manager sees your games but Gaming Mode shows no shortcuts? Follow these parser checks to restore your Steam Deck library."
keywords:
  - "steam rom manager parsers"
date: 2026-11-17T12:05:52+08:00
publishDate: 2026-11-17T12:05:52+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You're in Gaming Mode on your Steam Deck, EmuDeck is set up, and Steam ROM Manager clearly lists your ROMs, yet no new shortcuts appear in your Steam library.

## Check the parser output first
Open Steam ROM Manager and click the **steam rom manager parsers** tab. Confirm the parsers you need are enabled and that each one shows a non-zero game count. If a parser shows zero, it isn't matching your ROM folder; re-point it to the correct path. If counts look right, click Preview and verify the games appear there. No games in Preview means the parser configuration is wrong, not Gaming Mode.

## Confirm you saved and added shortcuts
After Preview, click Save to Steam. Watch for a confirmation message. Then switch to Gaming Mode and check the Non-Steam tab, not just your recent games. If shortcuts are still absent, return to Desktop Mode, open Steam, and look under the Non-Steam section of your library. If they appear there but not in Gaming Mode, the issue is a Steam cache, not the parser.

## Verification test
In Desktop Mode, launch one shortcut directly from Steam. If it starts, the shortcut is valid. Restart the Steam Deck and re-check Gaming Mode. A clean restart often refreshes the library view.

## Rollback note
Before changing parser settings, note your current ROM paths. If a parser edit makes things worse, disable that parser, save, and re-enable it to restore the previous state.

If shortcuts still don't appear after these checks,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) with your parser list and Preview results.
