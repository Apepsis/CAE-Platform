# CAE Platform

Hub for my Cambridge C1 Advanced (CAE) study setup. The code lives in **[Apepsis/Ruta-CAE](https://github.com/Apepsis/Ruta-CAE)**; this repo just links the pieces together.

| Piece | Where | What it is |
| :-- | :-- | :-- |
| **Ruta CAE (web app)** | https://apepsis.github.io/Ruta-CAE/ | The full platform as an installable PWA: practice for every paper, Listening, Writing & Speaking marking, Media Lab, Speaking Tutor, Weekly Word Sheet (PDF), Deck Hub / Anki export |
| **Ruta C2 (claude.ai)** | https://claude.ai/artifact/KFEAm6NUy6ZYK7j2R4Zz7B | The original version, running inside claude.ai with Claude built in and the listening recordings included |
| **Source code** | https://github.com/Apepsis/Ruta-CAE | App, Chrome extension, Tauri desktop wrapper, CI |
| **Desktop app + extension** | https://github.com/Apepsis/Ruta-CAE/releases | Built by GitHub Actions when a `v*` tag is pushed |

## Setup, once

1. **Open the web app** → ⚙ (top right) → **AI**: choose Claude and paste an Anthropic API key (or Ollama, free and local).
2. **Content pack** (Listening audio + transcripts, private, never in a public repo): ⚙ → **Content pack** → *Import pack* → pick `ruta-cae-pack-PRIVADO.zip` **without unzipping it**. The Listening tab lights up.
3. **Progress from Ruta C2**: in the claude.ai version click the exam countdown (top bar) → *Export my progress (.json)*. In the web app: ⚙ → **Backup & sync** → *Import backup*. Imports merge, they never delete.
4. **Chrome extension**: download `ruta-cae-extension.zip` from Releases (or use the `extension/` folder of Ruta-CAE) → `chrome://extensions` → Developer mode → *Load unpacked*. It already points at the web app above.
5. **Desktop app**: in Ruta-CAE, `git tag v1.0.0 && git push --tags` → Actions builds Windows / macOS / Linux installers into a draft Release.

Everything lives on each device (browser storage). Use ⚙ → Backup & sync → Export to move it between browser, desktop and phone.
