---
title: Steam ROM Manager Detects a Game but No Steam Shortcut Appears
description: Trace an EmuDeck game from ROM path to parser preview to a working Game Mode shortcut.
seo_title: Steam ROM Manager Not Adding Games to Steam
seo_description: Trace an EmuDeck game from ROM path to parser preview to a working Game Mode shortcut.
keywords:
- steam rom manager not showing games
- emudeck games not in steam
- steam deck emulation setup
date: '2026-11-13'
draft: false
categories:
- Handheld Emulation
category_slug: handheld-emulation
---

**steam rom manager not showing games**. 

<p>Steam ROM Manager can detect a ROM in its preview and still fail to create a usable shortcut. Check the path, parser, saved output, and launch command in that order.</p>
<h2>Before you start</h2><ul>
<li>Steam Deck with EmuDeck installed</li>
<li>One compatible emulator and one self-supplied game</li>
<li>Desktop Mode access</li>
<li>The ROM's exact path</li>
</ul>
<h2>Step-by-step checks</h2>
<h3>Step 1: Locate the ROM where EmuDeck expects it</h3>
<p>Open the emulator's ROM folder and confirm the file is present and readable. If it is on a microSD card, verify the card is mounted at the same path in Desktop and Game Mode.</p>
<p>Check: The emulator can see the ROM at the documented path.</p>
<h3>Step 2: Enable and preview the parser</h3>
<p>In Steam ROM Manager, enable only the parser for that system. Add the correct ROM directory, generate the preview, and confirm the title and launch command.</p>
<p>Check: The preview shows the exact game and the installed emulator.</p>
<h3>Step 3: Save the shortcuts and restart Steam</h3>
<p>Save the preview output, close Steam ROM Manager, and restart Steam/Game Mode. Search the library for the exact title rather than scrolling a large collection.</p>
<p>Check: A shortcut with the expected title appears in the library.</p>
<h3>Step 4: Launch and inspect the command</h3>
<p>Start the shortcut from Game Mode. If it fails, open the shortcut properties and compare the launch command and ROM path with the working emulator.</p>
<p>Check: The game starts with the intended emulator, not a desktop window.</p>
<h3>Step 5: Exit and repeat</h3>
<p>Play for a minute, exit with the emulator's normal command, and launch a second time. A shortcut that only works once is not handed over.</p>
<p>Check: The game launches and exits cleanly twice.</p>
<h2>Verify the result</h2>
<p>The game appears as a Steam shortcut, launches from Game Mode with controls and sound, and survives a Steam restart.</p>
<h2>Rollback</h2>
<p>Keep the previous parser configuration. Remove only the test shortcut if it is wrong; do not delete the ROM or emulator data.</p>
<p><a href="/#consult">Ask for help with this exact symptom</a> · All troubleshooting guides</p>
