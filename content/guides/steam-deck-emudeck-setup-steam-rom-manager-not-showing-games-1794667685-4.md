---
title: "Steam ROM Manager Not Showing Games: Fix Parsed ROMs Missing in Gaming Mode"
description: "Steam ROM Manager parses your ROMs but no shortcuts appear in Gaming Mode. Follow these checks to diagnose and fix the issue."
seo_title: "Steam ROM Manager Not Showing Games: Fix Parsed ROMs Missing in Gaming Mode"
seo_description: "Steam ROM Manager parses your ROMs but no shortcuts appear in Gaming Mode. Follow these checks to diagnose and fix the issue."
keywords:
  - "steam rom manager not showing games"
date: 2026-11-23T12:06:15+08:00
publishDate: 2026-11-23T12:06:15+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You've added your own ROMs to EmuDeck, and Steam ROM Manager (SRM) shows them parsed, but when you switch to Gaming Mode, no shortcuts appear—so you're stuck without a controlled diagnosis. Here's how to fix that specific failure.

## Check SRM's Save and Export

Open SRM in Desktop Mode. After parsing, click Save to Steam. Watch for a confirmation message. If you see an error like "Failed to save," SRM couldn't write to Steam's shortcuts file. Ensure you're running SRM as the deck user (not root) and that Steam is running in the background. Then click Export. A successful export shows no error and closes the window.

## Verify Steam's Shortcuts File

In Desktop Mode, open the file manager and navigate to `/home/deck/.steam/steam/userdata/<your_user_id>/config/`. Look for `shortcuts.vdf`. Check its modified timestamp—it should update after you click Save in SRM. If it doesn't, SRM isn't writing. Try deleting `shortcuts.vdf` (back it up first) and re-exporting from SRM.

## Restart Steam Completely

Gaming Mode caches shortcuts. After exporting, fully exit Steam (Steam menu > Exit) and relaunch it. Then switch to Gaming Mode. Your shortcuts should now appear. If they don't, the issue is likely that SRM is still not showing games in the Steam library—meaning the export didn't register. This is a common **steam rom manager not showing games** symptom that often stems from a permissions or path mismatch.

## Verification Test

Create a single test shortcut in SRM for one ROM. Export, restart Steam, and check Gaming Mode. If it appears, your bulk export had a parsing error—re-parse all ROMs and export again. If it doesn't, re-check the shortcuts file path and SRM's save location.

## Rollback Note

If you deleted `shortcuts.vdf`, restore your backup to revert changes. Always back up before modifying Steam's config.

Still stuck?

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) for a guided diagnosis.
