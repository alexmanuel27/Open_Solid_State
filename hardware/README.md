# Direct-insertion reference — mechanical requirements

Status: requirements only. No validated CAD, DXF, STL, or STEP exists yet.

The agreed design is a rectangular PMMA piece retained in a printed square base, inserted directly into the instrument's cuvette holder. There is no surrounding cuvette and no immersion liquid. The nominal 3 mm PMMA thickness is the optical thickness at normal incidence; it is unrelated to the holder's nominal 10 mm liquid-cuvette path.

Candidate base height is 5 mm. Its footprint, slot, engagement, and insertion depth are **TBD from measurements**. A nominal cuvette path does not specify the holder's mechanical interface.

## Coordinate convention and datums

- x: nominal beam propagation; the sheet thickness lies along x.
- y: transverse horizontal direction; piece width must cover the beam footprint and positioning margin.
- z: vertical direction; piece height must cover the beam and remain accessible for removal.
- A: bottom seating surface defining z.
- B: selected side face controlling lateral position and rotation in the actual holder.
- F: marked front face defining the instructed insertion orientation.

Do not assume every holder locates a square object against the same surfaces. Record spring contacts, locating faces, and any adapters.

## Holder and beam survey

Copy this table for each instrument into its record using docs/records.md. Record measured values with method and uncertainty or resolution; distinguish drawings from observations.

| Parameter | Value | Source/method | Design consequence |
|---|---|---|---|
| Instrument and holder/accessory ID | TBD | Inventory | Compatibility is holder-specific |
| Clear opening in x and y | TBD | Measure/drawing | Maximum footprint and insertion clearance |
| Opening shape, corner radii, taper | TBD | Inspect/measure | Square base fit |
| Bottom stop and available insertion depth | TBD | Inspect/measure | Seating datum and removal access |
| Spring/locating faces | TBD | Inspect | Orientation and preload |
| Beam center height above seating datum | TBD | Document/verify | Whether 5 mm base clears beam |
| Beam footprint at the PMMA plane | TBD | Document/verify | Optical width/height and margins |
| Available position along beam axis | TBD | Inspect | Repeatable PMMA plane |
| Allowed sample height and lid clearance | TBD | Inspect | Maximum assembly height |
| Removal access | TBD | Trial | Handle/grip outside beam |

## Prototype requirements

1. Use the original sheet faces as the optical faces. Cut the perimeter only; do not route light through a laser-cut edge.
2. Cover the whole beam at the selected PMMA plane and every allowed seating position. Do not let transmitted light bypass an edge.
3. Keep printed material, identifiers, and retaining features outside the beam envelope, including its uncertainty and insertion margin.
4. Set slot width from actual sheet thickness and observed printer fit. No unsupported universal clearance value is specified.
5. Hold the PMMA without rocking, bowing, scratching the optical area, or requiring forced insertion. Check actual printed dimensions after cooling.
6. Use removable mechanical retention for the first prototype. Adhesives and optical coatings are not part of the initial process.
7. Mark front and specimen identity outside the optical region. A square allows 90-degree rotations; a front mark is procedural control, not mechanical proof of one-way insertion. Add a key only if the holder supports it.
8. Demonstrate repeatable seating at the bottom stop. A short base is acceptable only if its engagement and specimen retention prevent meaningful tilt.
9. Use a matched empty mount for the blank, with the same beam clearance. Record its identity; it is not a certified optical reference.

## Manufacturing sequence

Survey one holder -> draw one adjustable prototype -> check printer fit on a non-optical coupon -> cut one clear PMMA prototype -> inspect and measure -> verify beam coverage and ten insertion cycles -> revise if needed -> release the first experimental geometry -> fabricate nine pieces.

Laser cutting is preferred only after the machine type, material grade, masking, extraction, and operating procedure are confirmed compatible. Do not assume an unspecified laser can cut clear PMMA. Existing CNC access is the fallback; compare methods only if needed to resolve a real issue. Follow grade-specific manufacturer and laboratory machining instructions [R8](../docs/references.md).

Record machine settings, sheet position, kerf/finished dimensions, printer settings, filament, slot fit, and surface condition. Do not adopt polishing or annealing without a documented reason and a new process record.

## Files to release after validation

Keep editable CAD as the source. Export dimensioned drawings and appropriate DXF/STL/STEP files with units, revision, and source linkage. Instrument-specific interfaces may need separate variants; do not label one mount universally compatible before testing. No fabricated geometry is released from assumed holder dimensions.
