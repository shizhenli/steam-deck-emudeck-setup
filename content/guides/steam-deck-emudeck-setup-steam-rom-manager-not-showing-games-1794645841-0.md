---
title: "Steam ROM Manager Not Showing Games: Fix Missing Gaming Mode Shortcuts"
description: "Troubleshoot Steam ROM Manager parsing ROMs but no shortcuts appearing in Steam Deck Gaming Mode. Step-by-step checks and verification."
seo_title: "Steam ROM Manager Not Showing Games: Fix Missing Gaming Mode Shortcuts"
seo_description: "Troubleshoot Steam ROM Manager parsing ROMs but no shortcuts appearing in Steam Deck Gaming Mode. Step-by-step checks and verification."
keywords:
  - "steam rom manager not showing games"
date: 2026-11-14T19:38:39+08:00
publishDate: 2026-11-14T19:38:39+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You're in Gaming Mode on your Steam Deck, EmuDeck has parsed your self-owned ROMs in Steam ROM Manager (SRM), but no game shortcuts appear in your library—this guide walks you through a controlled diagnosis to restore the expected outcome.

## Check SRM's save and export settings

Open SRM and confirm you clicked Save to Steam after parsing. Then go to the Preview tab and verify that the games you expect are listed with green checkmarks. If they are unchecked, SRM will not create shortcuts. Also, under Settings, ensure "Create Steam shortcuts" is enabled and the correct user account is selected.

## Verify Steam's shortcut file

In Desktop Mode, navigate to ~/.steam/steam/userdata/[yourID]/config/shortcuts.vdf. Check the file's modified timestamp—it should update after you save in SRM. If it doesn't, SRM may lack write permissions. Right-click the file, check properties, and ensure your user has read/write access.

## Restart Steam and re-check

After saving in SRM, fully exit Steam (not just minimize) and relaunch it. In Gaming Mode, check your library under the "Non-Steam" tab. If shortcuts still don't appear, this is a classic case of **steam rom manager not showing games** in Gaming Mode despite successful parsing.

## Verification test

Add a single ROM manually via SRM: parse only that game, save, restart Steam, and check for its shortcut. If it appears, the issue is with your parser filters or ROM paths for the others. If not, proceed to recovery.

## Rollback and recovery

Before further changes, back up shortcuts.vdf. If shortcuts become corrupted, delete the file and re-save from SRM. For persistent issues,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) to diagnose your specific configuration.
