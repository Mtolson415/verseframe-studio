# Models and lyric acquisition

All entries are candidates; none has been executed or quality-tested in this project. Do not infer singing accuracy from ordinary speech benchmarks or AMD compatibility from CUDA instructions.

| Task | Candidates | Evaluation requirement |
| --- | --- | --- |
| Vocals/instrumental | BS-RoFormer, MelBand RoFormer through Audio Separator | Compare exact checkpoints; audible vocal leakage, lost instruments, artifacts; ROCm operations including FFT/complex handling |
| Lead/backing separation | Compatible karaoke/lead-vocal checkpoints | Evaluate independently from all-vocal removal; choir parts may not separate cleanly |
| Open-ended transcription | Full Whisper large-v3 and VocalParse singing research model | English solo/choir/children, repeats, sustained vowels, hallucinations, licensing, local dependencies |
| Fine alignment | English singing SOFA-combined; WhisperX baseline | Word and phoneme boundaries, phoneme-to-syllable grouping, held vowels and melisma; alignment is not transcription |
| Beat/downbeat | Beat This! | Tempo changes, pickups, rests; beats are independent from sung syllables |
| Visible lyric reading | PaddleOCR detection/recognition | Outlined/animated text, low contrast, text movement, unrelated text |
| Video restoration | ProPainter research candidate | ROCm portability, temporal consistency, mask quality, resolution, scene cuts, license |

VocalParse reports joint lyrics/melody/word-note transcription. That is a reason to investigate, not proof it is best for this application. SOFA-combined's model card reports English singing data and CC-BY-NC-SA-4.0; it is an optional research candidate requiring license review before distribution/use beyond its terms. Keep a permissive-path alternative. No weights will be redistributed automatically. Existing local voice-assistant models may be reusable only after verifying identity and compatibility; Turbo is not selected merely because it is installed.

## Acquisition strategy

1. Read title/artist/version/duration metadata; allow user correction before search.
2. Inspect permitted source captions, description, supplied sidecars, and OCR lyrics visible in the video. Treat all as candidates.
3. Search LRCLIB exact metadata and broader title/artist variants. Timed lyrics are useful evidence, not authoritative timing for a cover or different arrangement.
4. Provide adapters for additional free sources with supported access, including artist/publisher pages when usable. Record which sources were queried, matches, errors, and why candidates were rejected. No universal coverage guarantee and no silent account-dependent scraping.
5. Allow paste, TXT/LRC/ASS/SRT imports, and manual entry. Normalize for comparison while retaining original spelling/punctuation.
6. Transcribe locally from original and/or separated vocals. Compare candidate transcripts and published lyrics; flag disagreements, repeats, omitted lines, and arrangement differences.
7. User approves recording-specific text. If no usable online lyric is found, local transcription plus manual checking is a complete supported path, not an error state.
8. Align approved text; make uncertain and unmatched regions explicit. Refine syllables/holds and review audio. Do not equate character timestamps with reliable phoneme boundaries.

Paid lyric APIs are optional future adapters, disabled by default; no paid inference or automatic paid fallback. A future local language model may suggest corrections but must not invent missing lyrics or override approved text.

## Selection gate

After migration, record model source/revision/hash, code license, weight license, dependencies, container digest, host/runtime versions, dtype, device, and settings. Establish correct full-quality output before optimization. Precision is selected by supported operations and measured artifacts; FP32 alone does not guarantee superior results. No aggressive quantization or model downsizing for speed by default. Small evaluation set: authorized solo, choir, children, backing vocals, sustained notes, animated/embedded lyrics, moving background and scene cuts. Keep private detailed listening notes and share only permitted examples/results. Select checkpoints using observed output, not model size or popularity.
