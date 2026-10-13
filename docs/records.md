# Laboratory record templates

Copy the relevant block into a dated Markdown record alongside the acquisition session, or into a separately identified material/instrument record. These are blank templates, not measurements. Use `unknown` for unverified information and `not applicable` only with a reason. A nominal value, supplier claim and measured value must have separate labels.

## Material / procurement

```text
Record ID / date / operator:
Internal sheet ID:
Manufacturer / supplier / product URL:
Grade and color code / cast or extruded / coating or finish:
Supplier lot / source of lot information:
Receipt date / nominal thickness and tolerance:
Datasheet / invoice / machining guidance:
Measured thickness positions, values, method and uncertainty/resolution:
Sheet location map / original photographs:
Storage and retained coupon ID:
BOM ID / actual quantity / cost and currency / shipping/tax treatment:
Unknowns and substitutions:
```

## Instrument and holder

```text
Instrument ID / manufacturer / model / serial:
Holder/accessory ID:
Source / detector / optics / collection geometry:
Firmware / software version:
Wavelength domain / bandwidth / sampling interval / provenance:
Gain / integration time / averaging / auto-settings:
Export format, columns, units and meaning of exported values:
Background/reference procedure and built-in corrections:
Warm-up instruction and source:
Maintenance / calibration and verification history, documents and scope:
Independent check artifact ID / assigned values / uncertainty / conditions:
Holder survey: attach hardware/README.md table with values and methods.
Known limitations / unresolved specifications:
```

## Specimen, fabrication and assembly

```text
Specimen ID / material sheet ID / supplier lot:
Position on sheet / front and original sheet-face orientation:
Geometry revision / measured width, height and optical thickness:
Thickness measurement positions / method / uncertainty or resolution:
Cut date / operator / machine / tool or laser type:
Cut settings / masking / kerf and dimensional checks:
Cleaning / finishing / annealing (including 'none'):
Surface inspection and photographs / retained coupon ID:
Mount ID / CAD revision / actual base height and footprint:
Printer / nozzle / filament product and lot / print settings:
Slot dimensions / measured fit / retention / seating checks:
Assembly pairing date / front mark / qualified beam region:
Remounts / repairs / damage / current status:
```

## Acquisition session

```text
Session ID / protocol revision and frozen-plan reference:
Operator / date / start/end timestamps with timezone:
Instrument and holder IDs / settings / warm-up elapsed:
Day-zero timestamp / actual elapsed days:
Temperature and humidity readings / sensor ID / placement:
Blank mount ID / independent check ID and result files:
Background method / original background and reference filenames:
Specimen-to-mount pairings / instructed orientation:
Measurement mode: fixed / assembly reinsertion / PMMA remount / spatial / stability
Run order / replicate IDs / timestamps:
Band selection / bandwidth / sampling interval:
Spatial coordinates and footprint, if applicable:
Original export filenames / file-to-run mapping:
Pre/post blank and check results / flags:
Cleaning, remounting, handling and accumulated light exposure:
Storage before/after:
Deviations / missed runs / observed problems:
```

## Analysis and technical decision

```text
Record ID / date / author / milestone:
Question / intended use / minimum change worth detecting:
Protocol and criterion versions fixed before confirmatory data:
Evidence type: literature / manufacturer specification / hypothesis / estimate / measurement
Input dataset IDs / raw file provenance:
Processing script revision, dependencies and command, if used:
Transformations / corrections / exclusions with reasons:
Summary statistics and n / uncertainty model and correlations:
Expanded uncertainty coverage factor and method, if reported:
Valid specimen, mount, instrument, geometry and spectral domain:
Criterion-by-criterion result: pass / revise / fail / inconclusive
Unresolved confounding / negative findings:
Decision and rationale / next experiment:
Supersedes (if applicable; preserve the previous record):
```

Reserved final specimen IDs: ABS-CL-001, ABS-CL-002, ABS-CL-003; ABS-GR-001, ABS-GR-002, ABS-GR-003; ABS-RD-001, ABS-RD-002, ABS-RD-003. Assign an ID to a physical object once; never reuse a retired ID. Keep prototype IDs separate and maintain explicit specimen/mount pairings.
