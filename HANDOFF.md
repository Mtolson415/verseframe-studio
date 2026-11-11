# VerseFrame Studio migration handoff

Updated 2026-11-10. **Paused for Linux migration at the user's request.**

## Resume here

Read README.md, AGENTS.md, docs/ARCHITECTURE.md, docs/MODELS_AND_LYRICS.md and docs/ROADMAP.md. Do not reopen settled product requirements without a specific implementation conflict. The first implementation work is P1 in the roadmap after the user confirms migration is complete and resumes the project.

## Settled decisions

Name: VerseFrame Studio. General-purpose branding. Local Z13-only Docker web UI. Ubuntu 26.04 LTS, intended mainline kernel 7.0+. English only. Quality over speed. All singing arrangements are evaluation targets. Configurable vocal treatment. Bottom overlay with movement/removal. Full cadence cue combination. Prefer seamless existing-lyric replacement in first example; cover panel accepted initially. Free lyric search plus local singing transcription and manual revision; optional paid providers later. Selectable export codecs for actual playback targets. Public/private repository pair.

## Platform clarification

Ubuntu documents a distribution-maintained GA 7.0 kernel. AMD's 7.14.1 matrix lists Ubuntu 26.04 GA 7.0 for gfx1151. A custom upstream/mainline kernel 7.0+ is the user's stated target but is not automatically covered by that matrix. Verify installed kernel and AMD compatibility after migration; discuss any concrete conflict rather than silently changing the requested platform. Exact image, ROCm/PyTorch, drivers and model revisions remain unpinned. Avoid reusing old Windows driver assumptions.

## Outstanding implementation decisions

- Final model checkpoints require actual Z13 tests; singing models are not yet verified on ROCm.
- Exact lyric providers beyond LRCLIB need access/coverage evaluation. No paid dependency is required.
- Seamless removal is experimental until output passes visual review.
- Public application license is not selected; a public repository is not itself an open-source license grant. Review dependencies and weight terms before selecting a license or distributing models.
- Codec presets need player verification. Suggested default MP4/H.264/AAC is broad compatibility, not a universal guarantee.
- Brand/domain/trademark availability has not been cleared; no domain purchase is part of this work.

## Resume instruction

> Resume VerseFrame Studio after Linux migration. Inspect the actual Ubuntu/kernel/AMD/Docker state and follow P1 validation. Keep all model inference local and prioritize quality. Validate the full singing-specific pipeline before claiming support. Record exact revisions, licenses and evidence; proceed to one authorized end-to-end example when compatibility passes. Preserve the public/private split and project corrections.
