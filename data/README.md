# Experimental data policy

No experimental data have been acquired into this repository yet. Create session directories when actual data exist; do not create synthetic files that resemble measurements.

## Original acquisition files

Store exact, unmodified instrument exports under `data/raw/YYYY-MM-DD_session-ID/`. Use a session record based on [the templates](../docs/records.md) to map original filenames to specimens, mount pairings, replicate order and settings. Preserve native acquisition formats when available, along with exports.

- Processing must never write into an input acquisition file.
- Keep original columns, units, decimal formatting, headers and invalid values. Convert only into separate derived files.
- Preserve original exported filenames where feasible; do not overwrite repeated names. If renaming is necessary to prevent collisions, record the original name and mapping.
- Correct a transcription through an explicit amendment preserving the prior value, author, date and reason. Do not alter instrument output to repair a suspected error.
- Record input checksums when import tooling is added. Version control supports provenance but is not the only backup: retain a separate laboratory copy of original acquisitions.

## Derived data and figures

Create `data/processed/` for regenerable tables and `results/` for figures and technical reports when needed. Link every output to source sessions, protocol/criterion versions, transformations, exclusions and analysis revision. Report units and distinguish percent transmission from fractional transmission.

Add small scripts under `analysis/` only after inspecting real exports. Declare actual dependencies, include a meaningful runnable check for non-trivial calculations, and provide the command needed to reproduce outputs. No package framework or simulated scientific result is required for Phase 0 preparation.

## Session timing

Store timezone-qualified timestamps and actual elapsed days from the accepted baseline. Nominal visits are days 0, 1, 7, 14, 30, 60 and 90; the calendar schedule starts only after actual day zero. Missed or delayed sessions remain visible.

## Sharing and size

Publish project-owned data under the scope in [LICENSE.md](../LICENSE.md). Avoid including account details, purchasing credentials or unrelated personal information. Reference third-party manuals and certificates by provenance and applicable redistribution rights.

Small text exports can live in Git. If native files become impractically large, record their checksums and use an appropriate archive with a persistent link; choose Git LFS or archival storage only when actual file sizes require it. Do not silently omit raw evidence from a release.
