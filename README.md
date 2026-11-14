# downloads-deutsch

Offline data for the **Learn Deutsch** app (repo `learning-deutsch`), published
as GitHub release assets. The app downloads these files when it was not
installed from Google Play (Play users get the same data as asset packs).

Release `data-v1`:

| File | What | Unpacked to |
|---|---|---|
| `voice-thorsten.tar.gz` | Piper German voice Thorsten (male, medium) | `voices/de_DE-thorsten-medium` |
| `voice-kerstin.tar.gz` | Piper German voice Kerstin (female, low) | `voices/de_DE-kerstin-low` |
| `whisper-small.tar.gz` | Whisper small speech recognition (sherpa-onnx) | `models/whisper-small` |

Sizes and SHA-256 checksums are in `src-tauri/data-manifest.json` in the app
repo; the app checks them after each download. The files are made by
`tools/package-data.sh` in the app repo. They live only in the release, never
in git, and this repo must stay public: the app downloads without signing in.

Voices: Piper (MIT) with the Thorsten and Kerstin voice models under their own
licences. Speech recognition: OpenAI Whisper (MIT) converted for sherpa-onnx.
