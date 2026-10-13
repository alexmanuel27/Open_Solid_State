# OSORK-ABS — Pilot measurement protocol

Protocol ID: ABS-PILOT-0.1. Status: **draft; not yet frozen or executed**.

This protocol evaluates directly inserted mounted PMMA pieces. It does not use a surrounding cuvette or immersion liquid. See the [mechanical requirements](../hardware/README.md), [criteria](phase-0-plan.md), and [record templates](records.md).

## 1. Before acquisition

1. Identify the instrument, holder, source, detector, software/firmware, spectral bandwidth, sampling interval, and collection geometry. Record provenance of each specification.
2. Follow the actual instrument warm-up instructions and record elapsed time. Confirm readiness with the available independent check; a manufacturer's specification is not evidence that this particular instrument currently meets it.
3. Register PMMA grade, sheet coordinates, actual thickness, processing, mount revision, pairing, orientation and optical region. Inspect and photograph faces.
4. Confirm fit, repeatable seating and full beam coverage. Keep labels, base and cut edges outside the beam. Do not proceed with beam bypass or clipping.
5. Use a documented PMMA-compatible cleaning process. Record it and allow the specimen to reach measurement conditions. Avoid changing cleaning processes mid-series without a deviation record.
6. Fix gain, exposure/integration time, source settings and averaging wherever possible. Disable automatic changes or record them and demonstrate that the instrument's ratio remains valid. Record opaque blocking/background procedures if available.
7. Record temperature, humidity if available, sensor location, operator, start/end times and light exposure. Select the initial band set in reconnaissance, then freeze it before confirmatory measurements.

Use an initial instrument such as the GENESYS 30 if available. Its published 5 nm bandwidth and 1 nm data interval are different quantities [R9](references.md). Confirm the settings and actual instrument variant.

## 2. Reference, background and controls

- Reference: a matched empty printed mount in the same instructed orientation, with its identity recorded. Clear PMMA is a specimen, not the main blank.
- Reference checks: at the start and end of each block of at most three specimens, and after a setting change. Preserve the measured blank/check readings as well as any instrument zeroing operation.
- Background: use the instrument's documented procedure. An opaque blocker can reveal dark/background and residual light under that configuration; it is not a certified measurement of spectral stray radiant power.
- Independent check: measure a suitable stable artifact at the beginning and end of a stability session. Record certificate/characterization scope and uncertainty if available. Do not use a candidate PMMA specimen as the only independent proof of its own stability.
- Do not silently subtract unexplained control changes. Investigate, apply only justified corrections, and mark sessions inconclusive when attribution is unresolved.

Blank sequencing and correction/interpolation rules must be fixed in the session plan. For automatic manufacturer processing, record what the export represents and do not apply its corrections again.

## 3. Fabrication and mechanical screening

Start with ABS-CL-P01 and HLD-P01. Run ten complete removal/reinsertion cycles without disassembling the piece and mount. Check seating, play, insertion orientation and surface condition before and after. Verify beam coverage at the actual PMMA plane. Do not force the object into the instrument.

Only proceed to the nine-piece set after an accepted geometry decision. Freeze the assembly and handling procedure before starting day zero. Any later process or mounting change requires a record and may require a new baseline.

## 4. Exploratory spectra

Acquire three scans per specimen over 400–700 nm, removing and reinserting the complete assembly between scans. Use a balanced or randomized specimen order and save the actual order. Use the supported sampling interval and report bandwidth separately; do not infer additional resolution by interpolation.

Identify useful bands using signal, background, saturation, slope and expected uncertainty. Reject regions that cannot support the intended check. Document the selection rule, all excluded regions, and the original reconnaissance results. The same data must not be presented as an independent confirmatory pass after optimizing the criterion on them.

Prefer broad, moderately attenuating grey regions for the first repeatability check. A red transition can be useful as a spectral challenge but is sensitive to bandwidth and wavelength errors. A blocked red region does not automatically qualify as a stray-light standard.

## 5. Repeatability and assembly effects

For each of the nine final pieces and each frozen band (or full spectra if acquisition is practical):

1. Acquire ten readings without moving the assembly. Preserve individual readings and timestamps; note that close readings can be correlated.
2. Acquire ten readings with complete removal and reinsertion between readings, using the instructed front orientation and the same seating procedure. Keep PMMA fixed in its mount.
3. On one representative piece per material, separately perform five PMMA removal/remount cycles, with three readings after each remount. Record the pairing and any fit change. This is a diagnostic mounting test, distinct from normal insertion repeatability.

Report means, sample SDs, n, and contrasts between the tests. A small SD does not demonstrate absolute accuracy. Evaluate future single-insertion variation separately from uncertainty of a mean. If the specimen is remounted after day zero, log the event and assess whether the original stability baseline remains comparable.

## 6. Spatial dependence and between-piece variation

For each piece, use the center plus four known displaced positions in the usable optical region. Record coordinates and footprint. Hold angle, aperture and illumination configuration fixed and acquire three independent placements at each position. Recheck the center at the end to reveal temporal drift.

If the setup cannot translate without changing tilt, aperture or beam coverage, label the result positioning sensitivity, not pure material homogeneity. Do not average that confounding away. Spatial translations may need a temporary measurement fixture; its design is deferred until the available geometry is known.

Compare the three specimens of each material using their individual means and uncertainties. Report thickness and location with the spectra. Do not force thickness normalization by Beer–Lambert behavior unless the assumptions and surface effects are supported. These observations concern one sheet/process; they are not an interlaboratory reproducibility result.

## 7. Stability schedule and storage

Nominal elapsed days: **0, 1, 7, 14, 30, 60, 90**. Day zero is the first accepted baseline session after fixing the assembly and procedure. Record real acquisition times and elapsed days. A missed date is recorded as missed/delayed, never relabeled as on-time.

At every session:

1. Inspect without an unnecessary cleaning/remounting intervention; record any intervention that is needed.
2. Record environment, warm-up, checks and any instrument maintenance/settings change.
3. Acquire three independent assembly insertions per piece at the predefined bands. Full scans are preferred when practical; define their frequency before the baseline.
4. Preserve start/end blank and independent check results.
5. Store each assembly separately, protected from dust, optical-face contact and uncontrolled light. Log exposure duration, storage changes and any damage.

Evaluate change from day zero with uncertainty of the difference, including significant shared-baseline correlations and instrument-check limitations. Day-to-day variation on one instrument is an intermediate-precision/stability observation, not automatically reproducibility under changed laboratories or systems.

Without adequate independent control, report observed assembly-plus-instrument change. Do not claim that the material alone was stable. No accelerated exposure is interpreted as equivalent to 90 real days without a validated aging model.

## 8. Measurement model and validity

If compatible original sample, reference and dark signals are available:

```text
T_app = (S - D_S) / (R - D_R)
A_app = -log10(T_app)
```

S and R must correspond to compatible acquisition configurations or justified normalized signals. A common reference can induce covariance. The model is conditional on instrument behavior and does not correct every optical systematic effect.

For exported percent transmission, divide by 100 before a logarithm. For already processed instrument absorbance, preserve the original values and document their definition. Do not apply a second background or percent conversion.

Flag saturation, inadequate reference signal, nonpositive corrected signal, and signal near the background limit. Do not clip invalid transmittance to a positive epsilon. Retain values above one or negative instrument absorbance for diagnosis, with flags; do not silently coerce them into a physical range. Keep exclusions explicit in derived outputs.

Apparent absorbance includes losses and collection effects other than bulk absorption. Absolute material absorption and traceable transmittance are not claimed from this pilot.

## 9. Later comparison between architectures

Start only after short feasibility. Under linear detection, fixed collection geometry, negligible interfering fluorescence, and an adequately treated background, an effective band transmittance can be modeled as:

```text
T_eff,j = integral(W_j(lambda) * T(lambda) d lambda)
          / integral(W_j(lambda) d lambda)
A_eff,j = -log10(T_eff,j)
```

W includes the incident source spectrum, optical throughput and detector/channel response. An empirical spectrum with finite bandwidth is not exact high-resolution T(lambda); document the approximation and its limits. Do not average absorbance instead of transmission.

AS7265x channels have nominal 20 nm FWHM [R11](references.md); a center-wavelength interpolation does not establish equivalence to a scanning spectrophotometer. Bands whose response extends outside 400–700 nm need wider characterization or exclusion. If response weighting or geometry is unknown, compare each instrument's own stability and report cross-instrument discrepancies descriptively.

## 10. Required outputs

Original exports and metadata; fabrication/assembly records; spectra and validity domains; repeatability and reinsertion summaries; spatial and between-piece comparisons; control/time-series plots; preliminary uncertainty budget; pass/revise/fail/inconclusive decisions with rationale. Include unsuccessful materials, missed sessions, deviations and limitations. Report no experimental result until a corresponding dataset exists.
