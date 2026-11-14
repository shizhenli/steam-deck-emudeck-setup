---
title: "EmuDeck Controller Not Working: Fix the Emulator Detection Step"
description: "Steam Deck controls work in Steam but not inside the emulator? Follow these checks to restore controller detection in EmuDeck."
seo_title: "EmuDeck Controller Not Working on Steam Deck? Fix Detection"
seo_description: "Steam Deck controls work in Steam but not inside the emulator? Follow these checks to restore controller detection in EmuDeck."
keywords:
  - "emudeck controller not working"
date: 2026-11-14T19:38:39+08:00
publishDate: 2026-11-14T19:38:39+08:00
draft: false
categories:
  - "Handheld Emulation"
category_slug: "handheld-emulation"
---

You are in Gaming Mode on your Steam Deck, launching a game through EmuDeck, and the Deck's built-in controls work in the Steam menus but the emulator never detects them.

## Confirm the Emulator Is Actually Running

First, make sure the emulator window has focus. Press the Steam button, then use the trackpad to click directly on the game window. If the controls respond after clicking, the issue was focus, not detection. If nothing changes, continue below.

## Check Steam Input Per-Game

Open the game's shortcut in your Steam library, select the controller icon, and confirm the layout is set to Gamepad with Joystick Trackpad. If it shows Keyboard and Mouse, change it and relaunch. A layout that emulates a keyboard will not register as a controller inside the emulator.

## Reorder or Reset the Controller in EmuDeck

Open EmuDeck from your library and run the controller configuration step again. Choose the standard Steam Deck layout when prompted. This rewrites the emulator's controller profile. If the emulator still ignores input, open its own input settings and set the device to the first detected gamepad rather than auto.

## Verification Test

Launch a game and open the emulator's input or controller menu. Press a face button and watch for the binding to highlight. If it highlights, detection is restored. Test the left stick and D-pad separately to catch partial mappings.

## Rollback Note

If reordering breaks other emulators, return to EmuDeck's controller step and select the previous layout, then retest one emulator at a time. This is the most common cause of **emudeck controller not working** after an update.

If detection still fails after these checks,

![Steam ROM Manager parser preview on a Steam Deck](/images/service-detail-960.webp "Steam ROM Manager parser and shortcut check")

[Ask for help](/#consult) with your emulator name and the exact step where input stops.
