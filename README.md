# VerseFrame Studio

Local karaoke and synchronized lyric video production.

**Status: architecture and planning complete; implementation paused for Linux migration.** No application, model execution, Docker image, or media export has been verified for this project.

VerseFrame Studio is designed to turn authorized source videos into reviewed karaoke videos. It preserves the original picture, separates singing from accompaniment, gathers and transcribes English lyrics, aligns them to the recording, and renders configurable timing cues. Its initial community use is church activities; the product is designed for general use.

## Agreed requirements

- Quality takes priority over processing speed; preparation happens ahead of playback.
- Local model inference on AMD Strix Halo: Ryzen AI Max+ 395 / Radeon 8060S (gfx1151), 128 GB shared memory.
- Ubuntu 26.04 LTS with the user's intended Linux 7.0+ kernel. Exact kernel/driver/runtime compatibility must be validated after migration.
- Docker Compose application with a local web UI, accessible on the Z13 only.
- English lyrics; solo, choir, children, and mixed arrangements are evaluation targets, not claims of equal accuracy.
- Selectable vocal removal and guide-vocal mixing; lead/backing separation where models support it.
- Online lyric discovery, singing transcription, manual entry, comparison, and correction. Free sources first; optional paid integrations later.
- Bottom lyric placement by default; move, resize, style, or disable the overlay.
- Line, word, syllable, entry, beat, pause, and sustained-note cues, with manual correction.
- Preserve existing lyrics, cover them, or attempt seamless replacement. Prefer seamless removal in the first working example; covering is an accepted early fallback.
- Export selectable codec/container profiles. No single codec guarantees compatibility with every player.
- Public application repository plus a private companion; models and media live outside Git.

## Planning documents

- [Architecture](docs/ARCHITECTURE.md)
- [Model and lyric evaluation](docs/MODELS_AND_LYRICS.md)
- [Roadmap and acceptance](docs/ROADMAP.md)
- [Migration handoff](HANDOFF.md)
- [Repository policy](docs/REPOSITORIES.md)
- [Research sources](docs/SOURCES.md)

The application is not runnable yet. Docker manifests and dependency pins will be added after host validation; speculative install commands are intentionally not presented as working setup instructions.
