# VerseFrame Studio migration handoff

Updated 2026-11-10. **Implementation paused pending host validation and explicit owner resumption.**

## Resume here

Read README.md, AGENTS.md, docs/ARCHITECTURE.md, docs/MODELS_AND_LYRICS.md and docs/ROADMAP.md. Do not reopen settled product requirements without a specific implementation conflict. The first implementation work is P1 in the roadmap after prerequisites are met and the owner explicitly resumes the project.

## Settled decisions

Name: VerseFrame Studio. General-purpose branding. Loopback-only Docker web UI on a validated Linux host. Exact owner host preferences are maintained privately. English only. Quality over speed. All singing arrangements are evaluation targets. Configurable vocal treatment. Bottom overlay with movement/removal. Full cadence cue combination. Prefer seamless existing-lyric replacement in first example; cover panel accepted initially. Free lyric search plus local singing transcription and manual revision; optional paid providers later. Selectable export codecs for actual playback targets. Public/private repository pair.

## Platform clarification

Distribution-maintained and custom upstream kernels are different compatibility claims. Verify the actual kernel, GPU drivers and runtime against current official support information before execution. Exact image, ROCm/PyTorch, drivers and model revisions remain unpinned. Actual owner platform preferences are recorded privately.

## Outstanding implementation decisions

- Final model checkpoints require actual target-host tests; singing models are not yet verified on ROCm.
- Exact lyric providers beyond LRCLIB need access/coverage evaluation. No paid dependency is required.
- Seamless removal is experimental until output passes visual review.
- Public application license is not selected; a public repository is not itself an open-source license grant. Review dependencies and weight terms before selecting a license or distributing models.
- Codec presets need player verification. Suggested default MP4/H.264/AAC is broad compatibility, not a universal guarantee.
- Brand/domain/trademark availability has not been cleared; no domain purchase is part of this work.

## Resume instruction

> Resume VerseFrame Studio only after prerequisites and owner resumption. Inspect the actual Linux/kernel/AMD/Docker state and follow P1 validation. Keep all model inference local and prioritize quality. Validate the full singing-specific pipeline before claiming support. Record exact revisions, licenses and evidence; proceed to one authorized end-to-end example when compatibility passes. Preserve the public/private split and project corrections.
