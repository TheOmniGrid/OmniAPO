# Changelog

OmniAPO's public history starts at 1.0.0. Earlier version numbers exist in the
project's own git history, where they describe builds that were never published
under this name.

## 1.0.1 — Small correctness fix

The Problems count in the Configuration Editor's analysis panel could very rarely be
off by one, if a device-registration check happened to run at the same moment as the
analysis. It always corrected itself on the next edit, but it is now exact every time.

The shipped guide and configuration reference also now correctly show this version
number instead of 1.0.0.

## 1.0.0 — OmniAPO

Renamed to **OmniAPO** and restyled to share the visual design of OmniScale and OmniPlay: the Omni palette, Space Grotesk as the display face, and a redrawn icon and installer.

Nothing about how the engine is found or configured changed. The install path (`C:\Program Files\EqualizerAPO`), the registry key (`HKLM\Software\EqualizerAPO`), `ConfigPath` and the configuration file format are all deliberately unchanged, so Peace, HeSuVi and any other front end keep working across the rename. Upgrading in place preserves the existing `config` directory.

The Qt applications are now dark-only rather than following the Windows theme, matching the rest of the Omni family.

**The update check is gone.** `UpdateChecker.exe` queried upstream Equalizer APO's version endpoint at every logon, reporting itself as a plain `1.4.2` — so an upstream release would have offered a download that, if accepted, replaced this build with vanilla Equalizer APO. OmniAPO has no version feed of its own; new builds are downloaded and installed by hand. What is left of that binary is the APO registration health check it always carried, now shipped as `HealthAgent.exe` with the logon task renamed to `OmniAPOHealthAgent`; upgrading unregisters the old task first. Run by hand it also confirms an all-clear, and has a **Check registration** entry in the Start menu.

With it went `Qt6Network.dll` and the `qt\tls` backend, which nothing else imported. No binary in this build links a networking library.

New: **Check configuration** in the Start menu runs the configuration checker (`Benchmark.exe --check`), which reports lines the engine would reject. It now also lists any plugin loaded from outside the installation — an advisory, not an error, since the configuration directory is writable by every account on the machine and a plugin path is a thing worth being able to see.

Impulse responses are now identified by their container before libsndfile parses them, and only WAV, Wave64, AIFF, FLAC, Ogg and CAF are accepted. libsndfile 1.2.2 has published parser defects in formats nobody uses for impulse responses, and it selects its parser from the file's header rather than its extension.

The full complement of interface languages is now English, German, Spanish, French and Romanian, in the installer and in all three applications.

Bundles Space Grotesk (Florian Karsten) under the SIL Open Font License 1.1 — see `licenses/SpaceGrotesk-OFL-1.1.txt`.

---

Older internal releases (1.4.2-plugin.1 and before) shared Equalizer APO's version
number while this was still a private fork. They are recorded in the source
repository rather than here, because nothing was ever distributed under them.
