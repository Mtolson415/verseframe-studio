# Roadmap and acceptance

## P0: planning / current stopping point

Requirements, proposed architecture, model candidates, repository policy, and migration handoff are written. No implementation or model installation before migration/resumption. Public license choice and exact dependencies are deferred, not blockers for a planning repository.

## P1: Linux host and container validation

Confirm Ubuntu 26.04, exact 7.0+ kernel, firmware, graphics driver, gfx1151, usable shared memory, storage, Docker Engine, Compose, and GPU access inside an unprivileged worker. Choose and pin a matched ROCm/PyTorch/image combination from current official sources. Run representative model operations and a short actual separation/transcription/alignment/restoration sample, not just device enumeration. Record all failures and CPU alternatives using the same model. Do not count model load as quality acceptance.

## P2: first complete working example

Use one authorized English song with visible lyrics if possible. Import source, select vocal mix, discover/transcribe and approve text, align, edit word/syllable/hold timing, attempt seamless embedded-text removal, overlay, preview, and export. Include a countdown and one sustained-note cue. If restoration is inadequate, demonstrate a cover panel and record seamless removal as incomplete. A cover-panel export can be an early usable release, but cannot be described as successful seamless removal.

Acceptance: correct reviewed words; no obvious sync drift; user-adjustable timing and placement; usable accompaniment judged by listening; export decodes and plays on the chosen target; saved project reopens with corrections intact. Preview/export agree at start, mid-song and end. Check source/export duration and scene boundaries. Do not claim all arrangements supported from one example.

## P3: representative quality and resilience

Evaluate solo, choir, children, mixed/backing arrangements, repeated verses, long notes, overlapping words, variable tempo, and difficult text backgrounds. Assess lyric word error before/after correction, correction effort, boundary errors on manually annotated segments, vocal leakage/instrument damage, and restoration flicker. Timing/rate/resource measurements are diagnostic; processing speed is not the ranking objective. Test interruption/restart, missing providers, no online lyrics, unavailable model, corrupt media, and insufficient disk space.

## P4: release and portfolio

Document actual installation, verified hardware/runtime combinations, model licenses, supported codecs, playback checks, limitations, and permitted before/after examples. Add meaningful integration tests for project persistence, revision invalidation, timeline/export agreement, and import validation. Keep experimental restoration/singer separation clearly labeled. Server deployment and broader languages remain future scope.
