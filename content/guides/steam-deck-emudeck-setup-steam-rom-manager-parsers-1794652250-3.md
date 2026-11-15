---
title: "Steam ROM Manager Parsers: Fix Shortcuts Missing in Gaming Mode"
description: "Fix Steam ROM Manager parsers that see ROMs but fail to add Gaming Mode shortcuts on Steam Deck. Step-by-step diagnosis and recovery."
seo_title: "Steam ROM Manager Parsers Not Adding Gaming Mode Shortcuts"
seo_description: "Fix Steam ROM Manager parsers that see ROMs but fail to add Gaming Mode shortcuts on Steam Deck. Step-by-step diagnosis and recovery."
keywords:
  - "steam rom manager parsers"
date: 2026-11-15T18:57:30+08:00
publishDate: 2026-11-15T18:57:30+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You're in Gaming Mode on your Steam Deck, EmuDeck is set up, and Steam ROM Manager clearly lists your ROMs, but no shortcuts appear in your library.

## Check the parser output before saving

Open Steam ROM Manager and click the **steam rom manager parsers** tab. Each enabled parser should show a count next to it. If the count is zero for the system you care about, that parser is not matching your ROM folder. Click the parser and confirm the ROM directory points to the folder where your files actually live, not a parent or empty subfolder. A correct parser shows a non-zero count and lists individual game names in the preview panel.

## Confirm you saved, not just previewed

Parsers populate the preview only. You must click Save to Steam to write shortcuts. After saving, watch for a success message. If you see an error about Steam being closed or a path issue, the shortcuts were not written. Also verify you are saving to the same Steam user profile you use in Gaming Mode.

## Verification test

Return to Gaming Mode, open your library, and filter by the emulator category or search for one known game title. If it appears, launch it once. If it still does not appear, restart the Deck fully, then reopen Steam ROM Manager and save again.

## Rollback note

If a parser change makes things worse, remove the affected parser, re-add it with the default EmuDeck settings, and save. You can also delete generated shortcuts from Steam ROM Manager's remove option and regenerate them.

If these checks do not restore your shortcuts,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) with your parser counts and save messages.
