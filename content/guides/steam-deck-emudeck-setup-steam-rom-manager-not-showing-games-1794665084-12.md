---
title: "Steam ROM Manager Not Showing Games: Fix the Empty Gaming Mode Library"
description: "Steam ROM Manager parses ROMs but no shortcuts appear in Gaming Mode. Follow these checks to diagnose and fix the missing shortcuts."
seo_title: "Steam ROM Manager Not Showing Games: Fix Gaming Mode Shortcuts"
seo_description: "Steam ROM Manager parses ROMs but no shortcuts appear in Gaming Mode. Follow these checks to diagnose and fix the missing shortcuts."
keywords:
  - "steam rom manager not showing games"
date: 2026-11-21T15:49:53+08:00
publishDate: 2026-11-21T15:49:53+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You have parsed your ROMs in Steam ROM Manager (SRM) and they appear in the preview, but after saving, Gaming Mode shows no shortcuts. This is a common **steam rom manager not showing games** issue, and it usually means the shortcuts were not written to Steam's configuration or Gaming Mode has not refreshed its library.

## Check the SRM Save Step

First, confirm you clicked Save to Steam after parsing. In SRM, the preview list must be populated, then you must click the Save to Steam button. If you only parsed and closed SRM, nothing is written. After saving, SRM should show a confirmation. If it does not, the save failed.

## Verify Steam's Shortcuts File

Switch to Desktop Mode. Open the file manager and navigate to `/home/deck/.steam/steam/userdata/<your user ID>/config/`. Look for `shortcuts.vdf`. Check its modified timestamp—it should be recent. If the file is missing or old, SRM did not write shortcuts. This is a key diagnostic: a missing or stale file confirms the save step failed.

## Restart Steam and Check Gaming Mode

If `shortcuts.vdf` is recent, restart Steam completely: exit to Desktop, then quit Steam from the tray, and relaunch. Return to Gaming Mode. If shortcuts still do not appear, check the Non-Steam tab in your library. If they are there but not in the main library, your filters may hide them.

## Verification Test

After restarting Steam, open Gaming Mode and go to your library. Select the Non-Steam tab. If your ROM shortcuts appear there, the issue is display filtering, not SRM. If they do not appear, re-run SRM and save again.

## Rollback and Recovery

Before making changes, back up your `shortcuts.vdf` file. If you accidentally clear shortcuts, restore the backup and restart Steam. For persistent issues,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) to diagnose your specific configuration.
