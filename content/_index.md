---
title: Steam Deck EmuDeck Setup
seo_title: Steam Deck EmuDeck Help | Games Missing from Steam
seo_description: Remote Steam Deck help when Steam ROM Manager detects games but they do not appear in the Steam library.
keywords:
- steam rom manager not showing games
- emudeck games not in steam
- steam deck emulation setup
hero_kicker: STEAMDECK EMULATION
hero_h1: EmuDeck games missing from Steam?
hero_lead: Get Steam ROM Manager parsers, paths, and Steam shortcuts aligned so one self-supplied game appears in Game Mode and launches.
hero_proof:
- One emulator and one self-supplied game
- Parser preview and saved shortcuts checked
- Launch and exit tested in Game Mode
hero_alt: Steam Deck handheld running an emulation game library
hero_title: Steam Deck handheld emulation library
body_alt: Steam ROM Manager parser preview on a Steam Deck
body_title: Steam ROM Manager parser and shortcut check
body_caption: Detection in the preview is not enough; the shortcut must launch the game in Game Mode.
failures_kicker: THE THREE FAILURES WE SEE
failures_heading: What is going wrong?
test_kicker: HOW WE TEST
test_heading: Find the failing layer, then prove the fix.
scope_kicker: SERVICE SCOPE
scope_heading: What is included
scope_note: The session covers one agreed device and one verified path. Anything outside the written scope is quoted separately before work starts.
faq_kicker: FAQ
faq_heading: Before you book
consult_heading: Tell us what is happening.
consult_lead: Send the device, software, exact symptom, and what you have already tried. We will confirm scope and a fixed quote before booking.
form_placeholder: Device, software version, exact symptom, and what you have tried.
first_guide_url: /guides/steam-deck-emudeck-setup/
symptoms:
- title: The ROM is detected but no shortcut appears
  text: Steam ROM Manager preview lists the game, but after saving there is no tile in the Steam library.
- title: The shortcut opens the wrong emulator
  text: A tile exists, but it launches a desktop app, a blank window, or the wrong system.
- title: The game exits immediately
  text: The shortcut starts and returns to Game Mode, or the emulator cannot find the ROM path.
checks:
- title: Confirm the ROM path
  text: Check that the file is in the folder EmuDeck expects and is readable by the Deck user. A path inside a mounted SD card can differ from desktop.
- title: Review the parser preview
  text: In Steam ROM Manager, confirm the parser is enabled, the ROM appears with the correct title, and the launch command points to the installed emulator.
- title: Save shortcuts and restart Steam
  text: Save the preview, restart Steam or Game Mode, and search the library for the exact title.
- title: Launch and exit once
  text: Start the game from Game Mode, confirm controls and sound, then exit cleanly back to the Deck UI.
included:
- One Steam Deck, one emulator, one game
- Steam ROM Manager parser and path review
- Shortcut creation and Game Mode launch
- Rollback notes for parser changes
excluded:
- Providing ROMs or BIOS files
- Repairing a microSD card
- Guaranteeing every emulator or game
- SteamOS reinstallation
faqs:
- q: Do I need to use desktop mode?
  a: Steam ROM Manager is usually configured in Desktop Mode, then tested in Game Mode. The handover test happens in Game Mode.
- q: Why does the tile disappear after a restart?
  a: The shortcut may not have been saved, Steam may have been running during the save, or the parser output was not committed. Restart and check the saved shortcuts.
- q: Can you install EmuDeck for me?
  a: The session can review the existing install and one emulator path. A clean reinstall is a separate decision if the installation is damaged.
---
