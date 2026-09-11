# Rack8 update log

Created by **Tgo Tracks · TRX DSP**

A bridge between producing and live looping—without a full DAW. Built for loopers, with the RC-505 MKII workflow at its heart.

Published updates are listed newest first. Each entry separates new features, changes, bug fixes and known limitations. Development builds are not presented as public releases.

## v0.7.1 — Session update

September 11, 2026 · Pre-release · [Download and full release notes](https://github.com/tgotracks/Rack8/releases/tag/v0.7.1)

### New features

- **Launchpad Pro MK3 Session support:** launch reusable MIDI patterns from an 8×8 grid, with one independently looping pattern per rack.
- **Scene launching:** start a whole row together, with next-bar, next-beat or immediate launch timing.
- **Pad feedback:** see assigned, playing, queued and stopping patterns on the Launchpad.
- **Save your Session grid:** cell assignments and launch timing are stored in your .rack8 project. Projects load stopped, with hardware MIDI output disarmed.
- **MIDI transport readout:** see whether Rack8 received Start, Continue or Stop from your loop station.

### Changes

- The eight buttons directly below the Launchpad grid launch **scenes 1–8**. Hold **Shift** with those buttons to select a rack.
- **Shift + pad** stops one rack at the selected launch boundary.
- Bottom-right **Stop Clip** and the on-screen **Stop session** button immediately stop transport and cancel active and queued clips.
- Session playback replaces arrangement-note playback. Timeline CC/program-change lanes stay inactive while Session playback is active.

### Bug fixes

- **Steps and the other right-side buttons no longer trigger scenes**, preventing unintended clip launches or stops.
- Session controls respect hardware layout changes instead of firing while you use the sequencer or another layout.
- MIDI Stop cancels queued clips even when Rack8 was already paused.
- Stop from the device that started playback is no longer discarded when another device takes over the tempo clock.

### Testing and known limitations

- Passed **187 automated Session, MIDI editor and playback checks**, plus a MIDI clock diagnostic and isolated installer upgrades from v0.6.0 and v0.7.0.
- The corrected physical Launchpad mapping and RC-505 pause behavior still need checking on your setup before live use.
- Rack8 follows received MIDI Stop. The RC-505 can continue sending clock while stopped, and some track/rhythm settings do not transmit Stop. If the readout stays on **Start received**, check LOOP SYNC, 1SHOT and RHYTHM STOP TRIG, and try All Stop. See the [BOSS manual, page 20](https://static.roland.com/assets/media/pdf/RC-505mk2_eng02_W.pdf).
- Stopping MIDI clips does not mute live audio input or effect tails. Session is a MIDI pattern launcher, not an audio-clip recorder or a full Ableton control script.
- This release includes the Session work from the unpublished v0.7.0 development build. v0.7.0 was not a separate public release.

### How to update

Use **Check for updates** inside Rack8, or leave **Auto-update** enabled for startup updates. Stop playback and turn off live Audio in and hardware MIDI output before updating. The v0.7.1 signed update feed is live. Back up your sessions: Session projects use format 6 and cannot be opened in v0.6.0.

## v0.6.0 — 8×8 racks, MIDI editing and in-app updates

September 10, 2026 · First public installer release · Pre-release · [Download and full release notes](https://github.com/tgotracks/Rack8/releases/tag/v0.6.0)

### Features included

- **Eight independent racks**, each with eight plugin slots total, and separate MIDI playlist tracks for separate instruments.
- **Live audio effects** for processing your loop station's output through hosted effects.
- **Reusable MIDI patterns** and a piano roll with selection, group dragging and resizing.
- **Ctrl+C / Ctrl+V** copy and paste, **Ctrl+B** duplicate, **Ctrl+Z** undo and **Ctrl+Alt+Z** redo for MIDI edits.
- **Check for updates** and signed startup updates, with idle-state checks and a recovery session before update restarts.
- A Windows installer replacing the portable-ZIP distribution workflow, plus a matching full open-source bundle.

### Important notes

- Older portable builds need an installer-based version once to receive future in-app updates.
- Plugins and the RC-505 MKII driver are installed separately. Real latency depends on drivers, buffers, routing and plugins; physical loop-station round-trip latency was not measured.
- Updates are EdDSA-signed. The initial installer is not Authenticode-signed and may show a Windows reputation warning. Do not disable Windows security.

## Earlier development

Earlier prototypes were shared during development. Their individual versions and dates are not reconstructed here; the public history starts with the verified v0.6.0 release.
