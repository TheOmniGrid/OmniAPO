# Frequently asked questions

## Is OmniAPO Equalizer APO?

OmniAPO is a maintained Equalizer APO fork with double-precision processing, AVX2 builds, VST3 hosting, its own interface work, and additional documentation.

## Does it process every application?

It sits in the Windows audio-processing pipeline, so configured devices are processed system-wide rather than per application.

## Does it use the network?

No. OmniAPO has no update check, telemetry, analytics, cloud service, or networking library. See [PRIVACY.md](PRIVACY.md).

## What does it require?

Windows 10 or Windows 11 x64, an AVX2-capable processor, and a Windows audio device that permits APO installation. See [Requirements](README.md#requirements).

## Is there a 32-bit or ARM64 build?

No. The current build is x64 and requires AVX2.

## Where are installation and configuration instructions?

Use the [OmniAPO guide](docs/OmniAPO-Guide.html) and the [configuration reference](docs/Configuration-Reference.html).

## Is OmniAPO open source?

Yes. OmniAPO is GPL-3.0-or-later. See [LICENSE](LICENSE), [LICENSING.md](LICENSING.md), and the included written offer.

## Where should problems be reported?

Use [SUPPORT.md](SUPPORT.md). Suspected vulnerabilities must be reported privately as described in [SECURITY.md](SECURITY.md).
