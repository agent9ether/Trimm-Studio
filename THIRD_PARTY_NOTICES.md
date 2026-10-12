# Third-party notices

The complete list of bundled components with their license texts is in THIRD_PARTY_LICENSES.md.
This file explains the larger pieces and the optional add-ons.

## yt-short-clipper (MIT)
Parts of `clipforge_core` (YouTube json3 caption parsing, ASS caption generation, GPU encoder
probing, highlight prompts and JSON repair, Repliz client, MediaPipe reframing approach) are derived
from <https://github.com/jipraks/yt-short-clipper>, Copyright (c) 2026 Aji Prakoso (jipraks), MIT licensed.
Files containing derived code carry a `Derived from yt-short-clipper (MIT)` header.

The fonts shipped in the upstream repository (`src-tauri/fonts/*`) carry their own licenses
(see upstream `FONT_LICENSES.md`) and are **not** copied into this repository.

## Bundled with the packaged app
* **deno** (MIT) — <https://github.com/denoland/deno>, Copyright (c) 2018-2026 the Deno authors. Shipped unmodified as
  `clipforge-deno` (pinned release, SHA-256 verified by `scripts/fetch_deno.py`). It is the JavaScript runtime yt-dlp
  uses to solve YouTube's signature challenges, and is only run by yt-dlp.
* **yt-dlp** (Unlicense) — <https://github.com/yt-dlp/yt-dlp>, frozen into the engine for URL imports and channel
  watching.
* **pip** (MIT) — <https://github.com/pypa/pip>, frozen into the engine so "Install offline transcription" can download
  packages without a system Python.

## Downloaded on request (not shipped)
* **piper-tts** (GPL-3.0-or-later, <https://github.com/OHF-voice/piper1-gpl>) with **onnxruntime** (MIT) and **NumPy**
  (BSD), fetched from PyPI into the extras folder when you press *Install* on the local voice engine. It is **not**
  part of Trimm's installers or source. Its voices (about 60 MB each, from <https://huggingface.co/rhasspy/piper-voices>)
  each carry their own license, which can restrict commercial use: check the voice's model card before publishing
  monetised videos with it, or use a cloud voice instead.
* **faster-whisper** (MIT), **CTranslate2** (MIT), **PyAV** (BSD) and their dependencies, fetched from PyPI into the
  extras folder when you press *Install offline transcription*. Whisper model weights (MIT, OpenAI; CTranslate2
  conversions by Systran) download from Hugging Face the first time you transcribe.

## MIT License text
The MIT-licensed components above (yt-short-clipper, deno, pip, and the other MIT-licensed packages bundled in the
engine or downloaded on request) are used under this license. The copyright notice of each component is the one
named beside it above.

```
Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated
documentation files (the "Software"), to deal in the Software without restriction, including without limitation the
rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit
persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the
Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE
WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR
OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```

Copyright holders named: Aji Prakoso (yt-short-clipper, 2026); the Deno authors (deno, 2018-2026); the pip
contributors (pip). Trimm Studio itself is not MIT-licensed: see LICENSE.

## Source code of MPL-2.0 components
A few bundled components are licensed under the Mozilla Public License 2.0 (certifi, and the Rust crates cssparser,
cssparser-macros, dtoa-short, option-ext and selectors). Trimm Studio uses them unmodified. Their source code is
available from the places below, as the MPL requires.

* certifi: https://pypi.org/project/certifi/ (source distribution) and https://github.com/certifi/python-certifi
* cssparser, cssparser-macros, selectors: https://github.com/servo/rust-cssparser and https://github.com/servo/stylo
* dtoa-short: https://github.com/servo/dtoa-short
* option-ext: https://github.com/soc/option-ext
* every Rust crate is also on https://crates.io under the name and version listed in THIRD_PARTY_LICENSES.md

## Components with more than one license
Some components are offered under a choice of licenses (for example "MIT OR Apache-2.0"). Trimm Studio uses them under
the permissive option, MIT or Apache-2.0, and not under any copyleft option that is also listed.
