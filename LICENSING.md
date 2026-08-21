# Licensing

OmniAPO is free software under the **GNU General Public License, version 3 or later**.

This page states what that means for you, why it is GPLv3 rather than GPLv2, how to obtain
the source code, and which third-party components are included. It is written to be read,
not to be waved at.

---

## Your rights

Whoever has a copy of OmniAPO has all four freedoms the GPL grants:

1. **Use it** for any purpose, including commercially, on any number of machines.
2. **Study it.** The complete source code is available to you — see below.
3. **Modify it** however you like.
4. **Redistribute it**, modified or not, to anyone, for any price or for nothing.

Nobody — including the author — may add restrictions on top of these. If you received a
copy with terms attached that contradict this page, those terms are void and this page is
what applies.

## How donations and the GPL fit together

They fit without friction, and it is worth being precise about why.

The GPL says nothing about price. Section 4 states plainly that you may *"charge any price
or no price for each copy that you convey."* Distributing OmniAPO only to people who
donate is therefore entirely within the licence. There is no obligation on anyone to give
software to the general public, and no obligation to publish it anywhere.

What the GPL does require is that **every recipient of the binary can get the
corresponding source** (section 6), and that they keep the freedom to pass both on. So:

- The donation buys **the download and the work behind it** — not a licence, not
  permission, not exclusivity.
- Once you have a copy, what you do with it is your decision, not mine. Including giving
  it to someone who did not donate.
- I cannot and do not ask you to keep it to yourself. Section 10 forbids imposing that
  kind of further restriction, and a request dressed up as a condition would be exactly
  that.

If you would rather support the project than redistribute it, that is appreciated. It is a
preference, not a term.

## How to get the source code

**Written offer under GPLv3 section 6(b).**

For at least **three years** from the date you received a binary copy of OmniAPO 1.0.1,
and for as long as spare parts or customer support are offered for this version, the
copyright holder will provide the **Corresponding Source** for that binary to anyone who
possesses it.

- **Who may ask:** anyone in possession of the object code. You do not need to have
  donated, and you do not need to explain why.
- **What you get:** the complete source code for the version you hold, including the build
  scripts and everything needed to generate, install and run it, under the terms of the
  GPL.
- **Cost:** no more than the cost of physically performing the distribution. In practice
  that means a download link at no charge.
- **How to ask:** omnivex@theomnigrid.biz

This offer is extended to any third party who receives the binary from you. If you pass
OmniAPO on, pass this offer on with it — the file `WRITTEN-OFFER.txt` in the download
exists for exactly that, and copying it along satisfies your own obligation under section
6(b).

## Why GPLv3 and not GPLv2

Equalizer APO, and the double-precision fork this build descends from, are licensed
*"version 2 of the License, or (at your option) any later version."*

The VST3 hosting layer in this build — bundle resolution, the plugin state save/restore
envelope and the plugin-editor attach sequence — adapts logic from
[Mixomo/EqAPO64_with_VST3_support](https://github.com/Mixomo/EqAPO64_with_VST3_support),
which is licensed GPLv3-or-later.

Combining GPLv2-or-later code with GPLv3-or-later code is permitted precisely because of
the "or any later version" clause: the whole may be distributed under GPLv3-or-later. That
is the option this build exercises, so the combined work is **GPLv3-or-later**.

Nothing about this narrows the original grant. The upstream code remains available from
upstream under its own terms, and the individual source files still carry their original
headers.

## Third-party components

Every component distributed with OmniAPO is named, attributed and licensed in the `NOTICE`
file inside the download, with full licence texts in `licenses/`. In summary:

| Component | Licence |
|---|---|
| Qt 6.10.1 (Core, Gui, Svg, Widgets and platform plugins) | LGPL v3, dynamically linked, unmodified |
| AOCL-FFTW 3.3.10 (AMD's FFTW fork) | GPL v2 or later |
| libsndfile 1.2.2 | LGPL v2.1 |
| muparserx 4.0.12 | BSD |
| TCLAP 1.2.5 | MIT |
| Steinberg VST3 SDK 3.8.0 | MIT (the SDK moved to MIT with 3.8; the vendored `LICENSE.txt` is reproduced as `licenses/VST3SDK-MIT.txt`) |
| NSIS and its extensions | zlib, BSD |
| Space Grotesk (Florian Karsten) | SIL Open Font License 1.1 |

**Trademark note.** VST is a trademark of Steinberg Media Technologies GmbH. OmniAPO is
not affiliated with, endorsed by or sponsored by Steinberg. The trademark is used only to
state a fact about compatibility.

## What this page is not

This is a plain-language summary written by the project, not legal advice, and it does not
replace the licence text. Where anything here disagrees with the GNU General Public License
version 3 — shipped as `LICENSE-GPLv3.txt` in the download and published at
<https://www.gnu.org/licenses/gpl-3.0.html> — **the licence text governs.** (The `License.txt`
installed next to the program is upstream Equalizer APO's GPLv2 text; its "or any later
version" clause is what the combined work's GPLv3 licensing rests on.)

---

Copyright © Omnivex and contributors. Portions copyright Jonas Thedering, TheFireKahuna,
Mixomo and others as recorded in `NOTICE`.
