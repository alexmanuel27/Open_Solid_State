# Phase 0 — Scientific definition and feasibility

Status: draft for laboratory preparation. Created: 2026-10-13.

## Question and intended use

Can inexpensive PMMA pieces in a reproducibly seated printed mount provide sufficiently repeatable and stable apparent transmission measurements to support specified optical instrument checks?

The initial intended use is comparative monitoring under fixed conditions, not assignment of universally transferable true absorbance values. The magnitude of instrumental change worth detecting remains **TBD** and must be recorded before confirmatory qualification.

The device under evaluation is the complete **PMMA + mount + insertion procedure**. Material-only claims require experiments that separate material and mounting effects.

## Scope and terminology

| Operation | Meaning for this project |
|---|---|
| Characterization | Determine spectral behavior, variability, sensitivity, and stability under stated conditions |
| Verification | Supply evidence that a specified requirement is met, accounting for relevant uncertainty |
| Calibration | Establish a relationship between reference quantity values and instrument indications, with uncertainties |
| Adjustment | Change the measuring system to obtain prescribed indications |

Use the VIM definitions [R1–R3](references.md). Commercial instrument readings alone do not establish certification or metrological traceability of a PMMA piece.

Active: OSORK-ABS, candidate 400–700 nm domain. Future: OSORK-FLUO and OSORK-TURB. Fluorescence or scattering that affects ABS measurements is an interference to investigate, not permission to start the future workstreams.

## Hypotheses and ways to challenge them

| Hypothesis | Test | Evidence against it |
|---|---|---|
| A printed mount makes insertion sufficiently reproducible | Fixed-position readings versus complete assembly reinsertion | Reinsertion spread materially exceeds the intended use allowance |
| Candidate PMMA provides useful attenuation | Exploratory transmission scan with background and saturation checks | No adequately measured spectral domain |
| The optical region is sufficiently uniform | Known lateral positions at fixed angle and aperture | Position-dependent variation exceeds the spatial allowance |
| Pieces from one sheet have similar responses | Three independently identified pieces per material | Between-piece differences preclude interchangeability; individual baselines may remain usable |
| The assembly is sufficiently stable | Scheduled readings with an independent instrument check | Changes exceed the allowance, or instrument drift cannot be separated adequately |
| References can be useful on another architecture | Compare within instrument-specific response bands and geometries | Useful domains disappear or differences cannot be explained within the available model |

These are hypotheses, not established properties of PMMA.

## Initial specimens

| Material | Candidate thickness | Planned experimental pieces | IDs |
|---|---|---|---|
| Clear transparent PMMA | 3 mm | 3 | ABS-CL-001 through ABS-CL-003 |
| Grey transparent PMMA | 3 mm | 3 | ABS-GR-001 through ABS-GR-003 |
| Red transparent PMMA | 3 mm | 3 | ABS-RD-001 through ABS-RD-003 |

All IDs are reservations; no physical pieces are asserted to exist. Use ABS-CL-P01 for the first clear prototype and HLD-P01 for its mount. Give final mounts separate HLD identifiers and record each assembly pairing.

Obtain manufacturer grade/color codes, actual thickness, sheet provenance, and stock location maps. Three pieces of one material from one sheet are within-sheet samples, not three supplier lots. Different cutting runs, supplier lots, operators, and laboratories require later experiments with their conditions explicitly specified [R4](references.md).

## Principal risks and responses

| Risk | Initial response |
|---|---|
| Grey material is not spectrally neutral | Measure its spectrum; do not label it a neutral-density standard |
| Red blocking region approaches the measurement floor | Mark invalid regions; do not interpret the floor as material transmission or a certified stray-light test |
| Surface reflection, scattering, or fluorescence contributes to the reading | Report apparent attenuation, fixed collection geometry, and unresolved effects |
| Beam bypasses PMMA or mount clips the beam | Verify the full beam footprint, edge margin, and empty-mount transmission |
| Mount seating, square-footprint rotation, or slot play changes response | Fixed datums, front mark, measured fit, and reinsertion trials |
| Laser cutting or cleaning changes the specimen | Preserve original optical faces; log processing and inspect retained coupons [R8](references.md) |
| Thickness or sheet composition varies | Measure thickness at registered positions and preserve specimen location maps |
| Instrument and specimen change together | Independent check in every stability session; report unresolved attribution |
| Temperature changes instrument and specimen simultaneously | Record conditions; use controlled specimen-only experiments before assigning a material coefficient |
| Unequal spectral responses mimic disagreement | Compare weighted transmission domains; do not interpolate absorbance and call instruments equivalent |

## Provisional decision criteria

The following are **internal screening targets**, not normative limits or demonstrated performance. Freeze their version after reconnaissance and before the confirmatory runs. Any change requires a dated decision with rationale; retain the original record. Set an intended-use change threshold and a compatible uncertainty allowance before declaring qualification.

Apply each criterion only in predefined usable bands and to its appropriate material. Assess all three pieces independently. Report failed and excluded bands, not just successful wavelengths.

| Metric | Candidate target |
|---|---|
| Mechanical fit | Ten insertion cycles without forced insertion, damage, uncontrolled movement, or detectable beam clipping/bypass |
| Useful signal | No saturation; signal distinguishable from background with documented uncertainty; 0.1–0.8 transmittance is a preferred initial grey range, not a requirement for clear PMMA |
| Fixed-position sample SD | s(A_app) <= 0.002, n = 10 |
| Complete assembly reinsertion sample SD | s(A_app) <= 0.005, n = 10 |
| Spatial range | Maximum minus minimum position means <= 0.010 in A_app |
| Short stability | abs(A_day7 - A_day0) + U(difference) <= 0.010 |
| Extended stability | abs(A_day90 - A_day0) + U(difference) <= 0.020 |
| Completeness | Original exports, metadata, controls, and deviations are available |

Absorbance is dimensionless. U(difference) is expanded uncertainty, with coverage factor and method reported, including significant covariance. A coverage factor of two is not automatically justified for every small-sample result. The SD estimates themselves have sampling uncertainty; passing ten observations is pilot evidence, not a guarantee of future performance.

Do not equate a nonsignificant difference with stability. A stability pass needs the difference and its uncertainty to fit inside the specified allowance. Unresolved instrument drift, insufficient uncertainty information, or inadequate signal gives **inconclusive**, not pass. A day-90 pass does not erase an earlier unacceptable excursion: assess every scheduled session against the intended-use requirements.

A material may advance independently of the other colors. Different pieces may receive individual baselines; a small mean difference is not required for individual use, but interchangeability needs its own allowance and uncertainty assessment. There is no photometric-linearity gate with the current single-grey-level set.

## Initial uncertainty model

Separate reading variation, assembly reinsertion, PMMA remounting, blank/reference variation, spatial dependence, between-session effects, and relevant environmental influence. Include wavelength sensitivity in steep spectral regions, instrument background, and unresolved response-band effects when applicable. Record instrument specification terms as specifications, not measured errors.

Do not add fixed-reading noise twice if it is already included in the reinsertion variation. Piece-to-piece variability belongs to an interchangeability claim, not automatically to the uncertainty of one individually assigned reference. Distinguish uncertainty of a mean from variability of a future individual insertion. Retain correlations from shared references or a common day-zero baseline. Follow the JCGM guidance [R5](references.md).

## Milestones and deliverables

| Milestone | Deliverable | Exit condition |
|---|---|---|
| M0: definition | Equipment inventory, holder survey, material specifications, prototype procedure | Inputs adequate to design one prototype |
| M1: mechanical prototype | Editable design, one clear prototype, fit/beam checks, manufacturing record | Acceptable seating and beam coverage |
| M2: short feasibility | Reconnaissance, frozen confirmatory protocol, nine-piece dataset, days 0/1/7, uncertainty notes, material-specific decision | At least one useful material/domain, or documented redesign |
| M3: extended ABS characterization | Days 14/30/60/90, revised uncertainty budget, technical findings | Intended-use performance supported or explicitly rejected |
| M4: transfer and independent fabrication | Second architecture, new fabrication run/lot as available | Conditions and limits of reproducibility documented |
| M5: reproducible technical release | CAD + exports, BOM, protocols, raw data, analysis, figures and versioned findings | Another laboratory can reproduce the specified workflow; consider Zenodo |

M2 permits continued ABS development; it does not claim 90-day stability or unlock FLUO/TURB automatically. Ninety days are measured from actual day zero after the assembly and handling procedure are fixed. No calendar start date is assigned yet.

## Novelty and standards boundary

Solid filter references and cuvette-holder-compatible mounts have established precedents [R6](references.md). The proposed contribution is evidence for accessible fabrication, cost, uncertainty, stability, and interoperability; this remains to be demonstrated.

ASTM E275 and E387 are relevant background [R10](references.md). Only their public scope descriptions have been consulted here. This protocol is not claimed to implement or comply with their full procedures. PMMA color filters are not substitutes for qualified wavelength or spectral stray-light standards.
