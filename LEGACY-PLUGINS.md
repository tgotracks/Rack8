# Legacy DLL plugins

Rack8 0.8.0 adds legacy 64-bit Windows audio-plugin DLL hosting alongside VST3.
The legacy interface uses the open-source FST headers and JUCE's plugin host.

1. Install the plugin using its own installer, including its content and licence.
2. Open **Plugins** in Rack8, then **SCAN / MANAGE**.
3. Choose the **VST** scan option for legacy DLLs; the **VST3** option is separate.
4. Add the folder containing your 64-bit plugin DLL and scan it.
5. Pick the discovered plugin in any of the eight slots on any rack.

For Tone2 Electra on this computer, the plugin entry is
`C:\Program Files\Steinberg\VSTPlugins\Tone2\Electra.dll`.
Some plugin DLLs are small loaders that depend on the rest of the installed
product. Do not copy only the DLL onto a friend's computer: use Tone2's installer
and that person's own valid licence. No third-party plugins are bundled.

Only 64-bit audio-plugin DLLs are supported. Ordinary Windows DLLs are not
plugins, and 32-bit plugins require a separate bridge (not included).
Compatibility depends on the plugin. Optional custom MIDI key-name queries
are disabled; standard piano-roll note names remain available.
Back up sessions and test your plugins before performing live.

Developers can run `Rack8.exe --test-plugin-file "C:\path\plugin.dll"` to scan,
instantiate, round-trip state and render MIDI/audio into silent buffers without
opening audio/MIDI devices. It also checks editor creation. The diagnostic
report is written one directory above the executable. It does not prove all
presets, every plugin feature, hardware latency or live-performance stability.
