# Open Solid-State Optical Reference Kit (OSORK)

An open-source, low-cost toolkit for optical instrument verification.

OSORK investigates reusable solid optical references, their fabrication, and their performance under documented measurement conditions. This repository contains technical development, experimental protocols, original data, analysis, and findings. Manuscript writing is managed separately.

**Status:** Phase 0 — scientific definition and experimental preparation. No specimens have been qualified and no experimental results are available in this repository.

## Current design

OSORK-ABS is the active workstream, initially covering 400–700 nm. Rectangular PMMA pieces will be held by printed square bases and inserted directly into instrument cuvette holders, without a surrounding cuvette or liquid.

- Candidate PMMA optical thickness: **3 mm**, subject to measured transmission.
- Candidate base height: **5 mm**, subject to beam clearance and seating checks.
- Light crosses the original sheet faces; cut edges remain outside the illuminated region.
- Base dimensions, slot clearance, insertion depth, and optical position require measurements of the actual holder and beam.
- Air remains upstream and downstream of the PMMA. Mechanical restraint controls orientation; removing a cuvette does not remove all air interfaces.
- A square footprint alone permits four insertion orientations. A front mark is required; mechanical keying depends on the instrument interface.

The first prototype is one clear PMMA piece and one base. The planned experimental set is three clear, three transparent grey, and three transparent red pieces. Prototype parts are tracked separately unless explicitly accepted into the experimental set.

OSORK-FLUO and OSORK-TURB are independent future workstreams. Their experiments and software are deferred until OSORK-ABS has sufficient evidence.

## Start here

| Resource | Purpose |
|---|---|
| [Phase 0 plan](docs/phase-0-plan.md) | Scientific scope, hypotheses, uncertainty, decision gates, and milestones |
| [Task list](docs/tasks.md) | Ordered work and outstanding measurements |
| [Shopping list / BOM](hardware/BOM.md) | What is needed, when, and what must be confirmed before purchase |
| [Mechanical requirements](hardware/README.md) | Direct-insertion design and holder survey |
| [Pilot protocol](docs/protocol-abs-pilot.md) | Fabrication, acquisition, repeatability, and stability procedures |
| [Record templates](docs/records.md) | Materials, instruments, specimens, sessions, deviations, and decisions |
| [Data policy](data/README.md) | Preservation of original exports and reproducible processing |
| [Sources](docs/references.md) | Primary literature, terminology, and manufacturer documentation |
| [Licensing](LICENSE.md) | Hardware, software, documentation, and data scopes |

## Scientific boundaries

These are experimental optical references, not certified reference materials. Characterization, verification, calibration, and adjustment are distinct operations. No metrological traceability, absolute accuracy, universal instrument compatibility, or photometric linearity is claimed without supporting evidence.

Three pieces from one sheet estimate within-sheet variation; they do not establish between-lot or interlaboratory reproducibility. Every qualified use must specify the specimen, assembly, spectral domain, instrument configuration, and relevant uncertainty.

## Working approach

Documentation is written in English. Preserve positive, negative, and inconclusive findings. Record sources separately from hypotheses and measurements. Use existing equipment first, measure before designing, and validate one prototype before making the full set.

There is no analysis package yet. Small Python tools will be added against real instrument exports, using standard library facilities and established scientific libraries when needed. Raw acquisition files will never be overwritten by processing.
