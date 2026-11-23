# Test neck assy v1

MG90S-driven two-axis neck prototype for the Loro sculpture. This checkpoint preserves the current PETG prototype geometry, with a cleaned Fusion browser tree and consistently numbered part names.

**Prototype, not a print-ready or physically qualified release.** In particular, `3mf/08_yaw_output_gear_22T.3mf` has a known non-manifold junction between its gear and flange. The defect also exists in the native Fusion body. It is included to preserve the complete test assembly, but needs repair and revalidation before printing. The other 12 component meshes passed the recorded topology checks; that does not establish physical fit or durability.

## Assembly guide

See [ASSEMBLY.md](ASSEMBLY.md) for the part-by-part glue/no-glue map, fastener schedule, dry-fit and assembly order, servo indexing, PETG fit checks, and commissioning checklist. In particular, capture the ball's **integral pitch pins** in the arms before permanently bonding the arms. The guide follows this exact V1 snapshot and does not change its CAD or mesh geometry.

## Files

- `test-neck-assy-v1.f3d`: complete native Fusion assembly, including editable history, parameters, and two non-printable MG90S envelope references.
- `3mf/`: one geometry-only file per printed component, in millimetres. No servos, purchased screws, or reference envelopes are included in these files.
- `manifest.json`: relative file paths, sizes, SHA-256 hashes, and component labels.
- `mesh-validation.json`: actual mesh topology and volume checks, including the output gear failure.
- `ATTRIBUTION.md`: source attribution and the license applying to this adapted CAD package.

These are geometry exports, **not slicer project files**: they contain no qualified printer settings, build-plate arrangement, supports, or G-code. Import at 100% scale and choose print orientations in your slicer. Part numbering matches the Fusion component labels. One of each listed printed part is required for this checkpoint.

| File in `3mf/` | Fusion label | Assembly |
|---|---|---|
| `01_head_ball.3mf` | 01 Head ball | Tilting ball |
| `02_front_shoulder_cup.3mf` | 02 Front shoulder cup | Stationary base |
| `03_rear_shoulder_cup.3mf` | 03 Rear shoulder cup | Stationary base |
| `04_yaw_carrier.3mf` | 04 Yaw carrier | Yaw carrier assembly |
| `05_yaw_retaining_collar.3mf` | 05 Yaw retaining collar | Stationary base |
| `06_tilt_pinion_40T.3mf` | 06 Tilt pinion 40T | Yaw carrier assembly |
| `07_yaw_servo_gear_36T.3mf` | 07 Yaw servo gear 36T | Stationary base |
| `08_yaw_output_gear_22T.3mf` | 08 Yaw output gear 22T | Yaw carrier assembly — needs mesh repair |
| `09_yaw_arm_1.3mf` | 09 Yaw arm 1 | Yaw carrier assembly |
| `10_yaw_arm_2.3mf` | 10 Yaw arm 2 | Yaw carrier assembly |
| `11_base_plate.3mf` | 11 Base plate | Stationary base |
| `12_tilt_rack.3mf` | 12 Tilt rack | Tilting ball |
| `13_subbase.3mf` | 13 Subbase | Stationary base |

## Fusion organization

The top-level groups are `01 Stationary base`, `02 Yaw carrier assembly`, `03 Tilting ball`, and hidden `99 Legacy construction - empty`. Empty historical construction components remain intentionally preserved rather than deleting potentially referenced timeline history. An additional empty gear-construction child is hidden in the carrier. Both servo envelopes are labeled `REF`, and the yaw servo is correctly identified as stationary.

The hierarchy is organizational, not a new native joint simulation. Source placements, solid counts, topology counts, bounds, volumes, areas, appearances, and physical-part visibility/grounding were compared before and after regrouping. Group hide/isolation behavior was checked. The exported F3D was reopened and its hierarchy, labels, history, parameters and geometry compared to the source.

This remains a hybrid imported/parametric design, not a fully constrained clean-sheet model. Two pre-existing timeline warnings (`Extrude12`, cached missing body reference; `Chamfer2`) remain. Some imported body result labels can revert to historical source labels following a full recompute; the numbered component names are the stable part identifiers. No geometry booleans, mesh repair, or clearance changes were made for this publication.

## Prototype assembly and fit notes

- Use PETG for this test. Sliding fits and servo spline fit still require physical testing with the actual printer, filament and motors.
- The rack and arms are glued in place. Their tight locating slots are intentional; do not automatically widen them as running clearances.
- The yaw shaft is part of the base in this checkpoint. The retaining collar holds the yaw cassette; no replaceable bushings are required for this prototype.
- Servo gears are intended to seat on the MG90S output splines and use the included axial retaining screws. Spline diameter, tooth form, screw length and actual motor travel are **not physically qualified** by this CAD export. Do not force a printed hub onto a servo.
- Plate-to-subbase fasteners: four M3 plastic self-tapping screws, nominally M3 x 25, through the plate into the subbase pilots. Cup-to-plate fasteners: two nominal M3 x 20 from below; assemble before fitting the subbase. Confirm actual screw length/head style against the printed parts before tightening.
- Existing arm fastener holes remain in the geometry, but the intended arm connection is now glue. If using these optional holes, the output flange requires flush countersunk heads rather than protruding pan heads.
- The tilt servo mounting holes are clearance holes; do not assume they provide self-tapping engagement. Use a suitable through-fastener arrangement and check head/nut access.

## Modeled range and clearances — not a hardware guarantee

The stationary yaw servo drives a 36:22 speed-increasing pair. A 220-degree total yaw range requires approximately 134.44 degrees of servo travel. Actual MG90S usable travel must be calibrated on the particular motors; nominal retail travel claims are not an installed-range test.

Prior sampled geometry checks support a provisional pitch range of -30 to +55 degrees. Do not command +60 degrees: rack/arm and ball/arm interference was found there. The checks are sampled, not continuous swept-volume certification, and do not include real wire stiffness or printed deformation.

Recorded prototype running clearances include 0.25 mm radial yaw journal clearance, 0.4 mm yaw collar axial clearance, and 0.25 mm radial clearance between the ball's integral 3 mm smooth pitch pins and 3.5 mm arm bores. Prior tooth-phase samples found minimum surface separations of approximately 0.199 mm for yaw and 0.156 mm for tilt; these are **not measurements of circumferential gear backlash**. Ball/arm shoulders have intentional sliding contact, and a small localized cup seam overlap remains. Check fit, avoid clamping moving surfaces, and inspect the sliced toolpaths before printing.

No head/beak geometry, electronics, controller calibration, physical torque test, or endurance qualification is included in this neck-only checkpoint.
