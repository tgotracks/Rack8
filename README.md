# Rack8

Created by **Tgo Tracks** · TRX DSP

The bridge between producing and live looping—without a full DAW.

Rack8 is a standalone plugin host built for loopers, with the BOSS RC-505 MKII workflow at its heart. Shape your sound with VST3 instruments and effects, build MIDI phrases, and bring them into your live looping setup from one focused workspace.

- Eight independent racks, each with eight plugin slots total.
- Separate MIDI playlist tracks for separate instruments.
- Reusable patterns and a piano roll with selection, group editing, copy/paste, duplication, undo and redo.
- Live audio effects for your loop station’s output.
- MIDI clock sync and dedicated CC/program-change lanes for hardware control.
- In-app update checking and signed startup updates.
- Launchpad Pro MK3 Session integration with an 8x8 reusable MIDI pattern launch grid.

## Download

[Download Rack8 v0.7.1 for Windows x64](https://github.com/tgotracks/Rack8/releases/tag/v0.7.1) — Session update, pre-release.

Download and run **Rack8-Setup-v0.7.1.exe** once, then launch Rack8 from its shortcut. Existing installer-based versions can update from inside Rack8. Leave **Auto-update** enabled to receive published updates on launch, or use **Check for updates**. Updates install when Rack8 is idle; stop playback, live audio input and hardware MIDI output before updating.

In Launchpad Session mode, the eight buttons directly below the grid launch scenes. Shift + those buttons selects a rack; Shift + pad stops one track. Bottom-right **Stop Clip** and Rack8's **Stop session** stop immediately. Side buttons such as Steps no longer trigger scenes. Connect through the dedicated Pro MK3 DAW ports in Rack8's Session tab.

Rack8 follows the RC-505's MIDI Start/Stop. If pausing the looper leaves **Start received** displayed, check its LOOP SYNC, 1SHOT and RHYTHM STOP TRIG settings and try All Stop. Continuous MIDI clock alone cannot indicate a pause. See the included SESSION-MODE.md. The corrected mapping and physical stop behavior need checking on your setup before live use.

The initial installer is not Windows Authenticode-signed and may show a reputation warning. Updates are separately verified with an EdDSA signature. Do not disable Windows security.

## MIDI editing shortcuts

Enable **Select** and drag empty piano-roll space to select a group of notes. Move or resize them together. Use **Ctrl+C / Ctrl+V** to copy/paste, **Ctrl+B** to duplicate, **Ctrl+Z** to undo, and **Ctrl+Alt+Z** to redo.

## Open source

Rack8's original application code is released under **AGPLv3**; third-party components retain their own licences, including GPLv3 ASIO portions. Full licence texts, dependency sources, notices and build instructions are included in the matching [Rack8-Source-v0.7.1.zip source bundle](https://github.com/tgotracks/Rack8/releases/download/v0.7.1/Rack8-Source-v0.7.1.zip).

Use that specifically named source bundle to build this release. GitHub's automatically generated “Source code” archives contain this repository snapshot, not the complete application bundle.

Windows 10/11 x64. Plugins and the RC-505 MKII driver are installed separately. Latency depends on your driver, buffer, routing and plugins. Back up your sessions and test your setup before performing. Rack8 is an independent product, not affiliated with or endorsed by BOSS, Roland, or third-party plugin makers.
