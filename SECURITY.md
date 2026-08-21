# Security

OmniAPO runs inside `audiodg.exe`, the Windows audio engine, and its configuration
directory is writable by every account on the machine. Two things follow from that and
are documented rather than hidden:

- **Plugins are code.** A VST3 or VST2 plugin named in the configuration is loaded into
  the audio process. `Check configuration` (Start menu) lists every plugin loaded from
  outside the installation folder, so an unexpected entry can be seen. Treat a plugin you
  did not put there like an unexpected program starting with Windows.
- **Impulse responses are parsed in-process.** Only WAV, Wave64, AIFF, FLAC, Ogg and CAF
  are accepted, identified by header rather than extension, and the parser is libsndfile
  1.2.2 with its published parser fixes applied. An impulse response from a stranger still
  deserves the caution you would give any downloaded file.

There is no network code in any OmniAPO binary, so there is no update channel to
compromise and nothing to phone home. Security-relevant fixes ship as new versions of the
download; the changelog says what changed.

## Reporting

Report a security issue privately to **omnivex@theomnigrid.biz** rather than in a public issue.
Say what you found, how to reproduce it, and which version you tested. You will get an
answer, and credit in the changelog if you want it.
