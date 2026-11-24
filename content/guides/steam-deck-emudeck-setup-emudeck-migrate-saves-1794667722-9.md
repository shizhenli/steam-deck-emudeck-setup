---
title: "EmuDeck Migrate Saves: Why a Save Stays in the Old Folder and the Emulator Opens an Empty Slot"
description: "Troubleshoot EmuDeck save migration on Steam Deck when a save exists in the old location but the emulator opens an empty slot. Step-by-step checks and verification."
seo_title: "EmuDeck Migrate Saves Not Working: Fix Empty Slot on Steam Deck"
seo_description: "Troubleshoot EmuDeck save migration on Steam Deck when a save exists in the old location but the emulator opens an empty slot. Step-by-step checks and verification."
keywords:
  - "emudeck migrate saves"
date: 2026-11-24T11:06:13+08:00
publishDate: 2026-11-24T11:06:13+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

## Troubleshooting

You copied your old save into the EmuDeck saves folder, but the emulator still starts with an empty slot. First, confirm the emulator's actual save path in Gaming Mode. Open the emulator, load the game, and check its save directory setting. Compare that path to where your save file sits. If they differ, the emulator is reading a different folder, so migration never happened. Next, verify the file name and extension match exactly what the emulator expects. A save named game.srm is ignored if the emulator looks for game.sav. Also check the file is not zero bytes and that the folder is not read-only. If the path and name are correct, the emulator may be using a per-game subfolder. Create that subfolder if missing and place the save inside. Now run a controlled test: back up the current save folder, launch the game, create a new in-game save, exit, and note where the new file appears. That location is the true target. Move your old save there, overwriting the test file, then relaunch. If the slot still loads empty, the save format may be incompatible; try exporting from the old emulator instead of copying raw files. For recovery, restore your backup folder before making further changes. If the emulator now shows the save, the issue was path or naming, not the migration tool. If it still fails, stop and get a second opinion before deleting anything. For a guided check of your exact setup,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult). Remember that **emudeck migrate saves** only works when the emulator's configured path matches the destination.
