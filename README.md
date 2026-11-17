# MarkDeck natural voices

Offline voice packs that the [MarkDeck](https://markdeck.app) reader downloads, on request, for its Read aloud feature. Once downloaded, they run entirely on the device; no text or audio leaves it.

Each pack is built from the publisher's Piper 1.5 voice ([rhasspy/piper-voices](https://huggingface.co/rhasspy/piper-voices)):
- the weights are quantized to int8;
- `tokens.txt` is derived from the voice's phoneme map;
- the voice's licence and credits are included.

No GPL code or data (such as espeak-ng) is included.

| Pack | Language | Voice licence | Credit |
|---|---|---|---|
| `es_ES-davefx.tar.gz` | Spanish (Spain) | CC0 1.0 | Piper voice «davefx», rhasspy/piper-voices |
| `pt_BR-faber.tar.gz` | Portuguese (Brazil) | CC0 1.0 | Piper voice «faber», rhasspy/piper-voices; base voice trained on Hi-Fi TTS reader 92 (CC BY 4.0) |
| `en_US-ljspeech.tar.gz` | English (US) | Public domain | Piper voice «ljspeech» (LJ Speech dataset, public domain); pronunciations from CMUdict, © 1993-2015 Carnegie Mellon University, BSD-2-Clause |

Each pack contains `model.onnx`, `tokens.txt`, `voice.json`, `LICENSE.txt` and `CREDITS.txt`. The English pack also contains `lexicon.tsv`, which is CMUdict converted to IPA.

The packs are published as release assets. The app checks the SHA-256 of each pack before installing it.
