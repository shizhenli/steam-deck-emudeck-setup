---
title: "Steam ROM Manager Not Showing Games in Gaming Mode: A Targeted Fix"
description: "ROMs parsed in Steam ROM Manager but no shortcuts appear in Gaming Mode? Follow these checks to restore your Steam Deck shortcuts."
seo_title: "Steam ROM Manager Not Showing Games: Fix Missing Gaming Mode Shortcuts"
seo_description: "ROMs parsed in Steam ROM Manager but no shortcuts appear in Gaming Mode? Follow these checks to restore your Steam Deck shortcuts."
keywords:
  - "steam rom manager not showing games"
date: 2026-11-21T15:43:37+08:00
publishDate: 2026-11-21T15:43:37+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You've parsed your ROMs in Steam ROM Manager (SRM) and see them listed, but after saving, Gaming Mode shows no shortcuts—this guide targets that exact gap.

## Check SRM's Save and Steam Restart

First, confirm you clicked Save to Steam after parsing. In SRM, the Parsers tab should show your ROMs; if they're listed, parsing succeeded. Now check the Preview tab: do the generated shortcuts appear there? If yes, but Gaming Mode is empty, the issue is likely Steam not refreshing. Exit SRM completely, then restart Steam (Steam menu > Restart). In Gaming Mode, wait 10–15 seconds for the library to rebuild. If shortcuts still don't appear, proceed.

## Verify Shortcut Data and Permissions

Switch to Desktop Mode. Open SRM and go to Settings > Shortcuts. Ensure the shortcut directory path is correct (typically /home/deck/.steam/steam/userdata/[ID]/config). Check that the userdata folder exists and is writable. If you recently moved ROMs or changed SD cards, re-run the parser and save again. A common cause of **steam rom manager not showing games** is SRM writing shortcuts to a stale userdata ID after a Steam profile change.

## Verification Test

Create a single test shortcut: in SRM, parse just one ROM, save, and restart Steam. If it appears in Gaming Mode, the pipeline works—re-parse your full library. If not, note whether SRM shows any error on save.

## Rollback and Recovery

Before further changes, back up your SRM configuration (Settings > Export). If shortcuts appear but launch incorrectly, remove them via SRM's Remove All Shortcuts and re-add. For persistent issues,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) with your SRM logs and userdata path.
