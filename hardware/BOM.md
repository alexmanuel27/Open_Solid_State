# Shopping list and provisional BOM

Status: procurement planning, 2026-10-13. The user confirms that no PMMA is currently available and that filament, machines and tools are available. Exact models, filament specification, tool types, supplier quotes, prices and sheet dimensions remain unconfirmed. No purchase or supplier contact has been made.

Buy small PMMA samples first: clear transparent, grey transparent and red transparent, nominally 3 mm thick. Obtain product/grade and color codes and confirm that the colored materials are transparent rather than opal or diffusing. Do not buy new machines or filament for the pilot on the current evidence.

Quantities below are planning requirements. Reuse or borrow before buying. PMMA sheet area will be calculated from the approved cutting layout, including prototype, kerf, retained coupon, and spare allowance; do not order a full-size sheet by default.

## First prototype and initial material screening

| ID | Item | Quantity needed | Minimum specification / purpose | Procurement action |
|---|---|---|---|---|
| B01 | Clear transparent PMMA | One small sheet/sample sufficient for prototype, 3 final pieces, retained coupon and spare | Nominal 3 mm, smooth original faces, identifiable grade; uncoated/non-textured preferred | Not owned: purchase a small documented sample after checking processing compatibility and required area |
| B02 | Transparent grey PMMA | One small sheet/sample sufficient for 3 final pieces, retained coupon and spare | Nominal 3 mm; transparent rather than opal/diffusing; known color/grade code | Not owned: purchase a small screening sample before committing to larger stock; transmission spectrum TBD |
| B03 | Transparent red PMMA | One small sheet/sample sufficient for 3 final pieces, retained coupon and spare | Nominal 3 mm; transparent, smooth faces, known color/grade code | Not owned: purchase a small screening sample; useful visible transmission domain TBD |
| B04 | Printer-compatible opaque filament | Existing supply confirmed by user | One documented material/color/lot for prototype; use existing filament if suitable | No purchase planned: record material/color and verify suitability; keep outside beam; do not assume optical opacity from color alone |
| B05 | Printed bases | Initially 1 sample base and 1 matched empty base | Nominal 5 mm height candidate; footprint and slot set by measurements | Print only after holder survey; final mount count decided after prototype |
| B06 | Caliper and, if available, micrometer | Tools available; exact types to confirm | Caliper for fit; low-force thickness measurement for PMMA, with method/resolution recorded | No purchase planned: inventory existing tool types and resolution; borrow any missing instrument first |
| B07 | Thermometer; humidity logger if available | Access to 1 set | Record room and relevant specimen conditions, sensor model and placement | Reuse laboratory equipment; do not buy a chamber initially |
| B08 | Storage box with individual compartments | Space for 9 assemblies plus prototype and controls | Protect optical faces from contact, dust and uncontrolled light exposure | Reuse a suitable box; document storage procedure |
| B09 | Labels and handling/cleaning supplies | Small laboratory supply | IDs outside beam; clean handling by edges; PMMA-compatible cleaning under manufacturer guidance | Inventory first; no unvalidated solvent treatment |
| B10 | Independent stable optical check | Borrow access to 1 suitable reference | Prefer documented characterization valid for instrument bands, geometry, and intended check | Ask within laboratory inventory; price/availability TBD; unresolved absence limits stability attribution |

The first physical build only needs B01 and a verified mount process. Small grey/red samples can be screened once the clear prototype fits. These three colors are not three levels of grey attenuation.

## Shared equipment and access

| Resource | Current knowledge | Next action |
|---|---|---|
| GENESYS 30 or other initial spectrophotometer | Mentioned in project scope; current access/status unconfirmed | Record exact instrument, holder, export capability and performance checks |
| 3D printer | Machines available per user; exact model unconfirmed | Record printer, nozzle, filament and fit capability; no purchase planned |
| Laser cutter | Machines available per user; exact laser type unconfirmed | Verify compatibility with actual PMMA grade, especially clear material; no purchase planned |
| CNC | User reports access | Record machine/tooling; retain as fallback; no purchase planned |
| AS7265x / C12880MA / camera spectrometer | Candidate comparison architectures | Select one second architecture only after short feasibility |

## Defer purchases

- Multiple grey attenuation levels: revisit for a separately designed linearity study.
- Additional PMMA thicknesses: revisit if 3 mm has no useful signal domain.
- Second supplier/lot: obtain when testing independent fabrication or supply reproducibility.
- Environmental chamber, integrating sphere, new spectrometer, and finishing equipment: justify through a failed or inconclusive experiment first.
- Fluorescent and scattering materials: outside the active ABS workstream.
- Surrounding cuvettes: not required for the selected direct-insertion architecture.

## Purchase record — copy one per actual item

```text
BOM ID:
Inventory status: unconfirmed / owned / borrowed / to purchase
Manufacturer and exact product/grade/color code:
Supplier and product URL:
Material, finish, coating and cast/extruded status:
Nominal dimensions and tolerances:
Supplier lot / internal sheet ID:
Quantity / purchased area:
Quote date / currency / unit cost / tax / shipping / total:
Order date / received date:
Datasheet and processing guidance location:
Substitution and rationale:
```

No cost estimate is reported until quotes or receipts exist. Later report material use, printing/cutting consumption, purchased equipment separately from shared equipment, and the costing assumptions. Manufacturer information is background, not measured OSORK performance [R7–R8](../docs/references.md).
