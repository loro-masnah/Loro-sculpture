# Test neck assy v1 — assembly guide

This guide follows the **published V1 parts**, not the earlier linkage-driven tilt or orbiting-yaw-servo layouts. The yaw servo is stationary in the base; the tilt servo travels with the yaw carrier. The rack and arms are bonded parts. The shoulder cups, base closure and servo connections remain removable.

**Status:** a geometry-grounded prototype assembly plan, not a record of a completed physical build. Read the stop checks below before printing or applying glue. No CAD geometry was changed to produce this guide.

## 1. Stop checks before assembly

- **Part 08 needs repair before printing.** The published `08_yaw_output_gear_22T.3mf` has a non-manifold gear/flange junction, also present in the native Fusion body. Do not accept a slicer's silent repair as proof of a sound load-bearing connection. Repair/revalidate that part and inspect its sliced junction before using it. The other 12 meshes passed the published topology checks.
- **Dry-assemble the entire mechanism before bonding anything.** Tight locating slots are intentional, but a press fit that splits PETG, distorts an arm or changes gear alignment is not acceptable. Remove print debris/elephant's foot locally; do not globally scale the assembly to fix one fit.
- **The pitch pins are already part of the ball.** The Ø3 mm cylindrical pins at the sides of part 01 are solid, integral geometry. They run inside the Ø3.5 mm arm bores. Do not buy loose pitch pins or put screws through these pivots. The small enclosed cavities farther out in the ball are not through-access holes.
- **Prove both MG90S spline fits and screw seating with the actual motors.** These are provisional printed direct-spline hubs, not factory-qualified spline tooling. Do not hammer a hub on, use the screw to pull on a tight hub, or let an overlong screw bottom in the servo.
- **Do not assume a universal MG90S travel range.** The [TowerPro product page](https://towerpro.com.tw/product/mg90s-3/) does not specify usable angular travel or pulse endpoints. Calibrate the particular motors with gears disengaged before commanding the assembled mechanism.

## 2. Parts and mechanism map

One of each printed part is used. Numbers below match the Fusion component names and the individual files in [`3mf/`](3mf/).

| Part | File | Function / connection |
|---|---|---|
| 01 | [Head ball](3mf/01_head_ball.3mf) | Moving spherical shell, with integral pitch pins; receives glued rack 12 |
| 02 | [Front shoulder cup](3mf/02_front_shoulder_cup.3mf) | Fixed shell; feet screw to plate 11 from underneath |
| 03 | [Rear shoulder cup](3mf/03_rear_shoulder_cup.3mf) | Removable shell half; screws to front cup |
| 04 | [Yaw carrier](3mf/04_yaw_carrier.3mf) | Rotating journal and tilt-servo mount |
| 05 | [Yaw retaining collar](3mf/05_yaw_retaining_collar.3mf) | Split clamp on the reduced tip of the fixed base shaft; retains cassette without squeezing it |
| 06 | [Tilt pinion 40T](3mf/06_tilt_pinion_40T.3mf) | Directly on tilt-servo spline, secured with supplied axial screw |
| 07 | [Yaw servo gear 36T](3mf/07_yaw_servo_gear_36T.3mf) | Directly on stationary yaw-servo spline, secured with supplied axial screw |
| 08 | [Yaw output gear 22T](3mf/08_yaw_output_gear_22T.3mf) | Coaxial driven gear and arm-support flange; repair junction first |
| 09 | [Yaw arm 1](3mf/09_yaw_arm_1.3mf) | One pitch support; slides over one integral ball pin before bonding its fixed locating interfaces |
| 10 | [Yaw arm 2](3mf/10_yaw_arm_2.3mf) | Opposite pitch support; mirror-side installation, not a second copy of 09 |
| 11 | [Base plate](3mf/11_base_plate.3mf) | Fixed integral yaw shaft, yaw-servo mounting and cup feet |
| 12 | [Tilt rack](3mf/12_tilt_rack.3mf) | Curved toothed sector bonded into the ball's locating feature |
| 13 | [Subbase](3mf/13_subbase.3mf) | Lower enclosure/stand, screwed to plate after underside work is complete |

The two `REF MG90S` bodies in the F3D are non-printable envelopes. The hidden empty legacy components are not extra parts to print.

```text
FIXED: 13 subbase — screws — 11 plate + integral shaft
                                  |— 02/03 shoulder cups
                                  |— stationary yaw servo — 07 gear
                                  |— 05 retaining collar (clamped to shaft)

ROTATES ON SHAFT: 08 driven gear + 04 carrier + 09/10 arms
                                      |— carried tilt servo — 06 pinion
                                      |— ball's integral pins in arm bores

TILTS BETWEEN ARMS: 01 ball + glued 12 rack, driven by 06
```

This is a connection diagram, not an exploded drawing or a claim that the Fusion groups contain motion joints. Both motion axes pass through the neck's common center. Only the neck area needs to remain spherical; the lower base is the service/access enclosure.

## 3. Glue map — fixed joints versus running surfaces

| Interface | Treatment |
|---|---|
| Rack 12 → its locating seat inside ball 01 | **Glue.** Fully seat the rack and verify pinion engagement before curing. Keep adhesive off teeth. |
| Arms 09/10 → their matching carrier locating faces and feet on output flange 08 | **Glue at the fixed mating faces.** Preserve the tight location fit and the exact arm spacing. Capture the ball first; see sequence below. |
| Carrier 04 → output gear/flange 08 | These are separate printed bodies in final V1 and must act as one rigid cassette. Their mating surfaces meet at the carrier's lower face. Include this fixed interface in the cassette bond-up; do not rely on friction against the base shaft to transmit yaw. This bond is an assembly recommendation from the final part interfaces, not a tested adhesive joint. |
| Ball pins → arm bores; ball shoulders → arm faces | **NO GLUE.** These are the pitch bearing/contact surfaces. |
| Carrier/output-gear bores → base shaft; cassette thrust faces → plate/collar | **NO GLUE.** These are yaw running/retaining surfaces. |
| Collar → shaft | **Clamp, not glue.** Keep removable and retain axial freedom. |
| Servo splines and axial screws | **No glue.** Press-seat only after fit is proven, then use the servo's included retaining screw. |
| Cups, plate/subbase, servo mounting ears | **Fasteners, not glue.** Keep access for servicing. |

Use an adhesive whose manufacturer explicitly supports bonding the actual PETG, and prove it on printed scrap first. Follow its surface-preparation, ventilation/PPE and full-cure instructions. Lightly prepare only bonding faces; remove debris and let cleaned parts dry. Do not assume ordinary plastic solvent cement will weld PETG.

Apply a controlled amount to the fixed faces, away from pins, journals and teeth. Do not flood tight slots with thin adhesive that can wick into a bearing. Mask/protect running surfaces without contaminating bond faces. Maintain alignment with a fixture; do not use clamp pressure to bend the arms around the ball. Remove squeeze-out before it becomes a hard interference. The design has not qualified an adhesive type, bond strength or cure schedule.

## 4. Fasteners and supplies

Use the actual screws to check head clearance and depth before final tightening. Sizes below distinguish modeled hardware allowances from unverified purchasing details. Plastic self-tapping screws are not interchangeable with machine screws just because both are labeled M2/M3. No tightening torque has been qualified for these PETG parts; tighten by hand, only enough to seat securely without stripping or crushing them.

| Connection | Quantity | Hardware / fit |
|---|---:|---|
| Plate 11 → subbase 13 | 4 | Nominal **M3 × 25 plastic self-tapping**; Ø3.4 plate clearance into Ø2.5 pilots. About 14.8 mm grip and 10.2 mm engagement in nominal 12 mm pilot depth. |
| Front cup 02 → plate 11 | 2 | Nominal **M3 × 20 plastic self-tapping**, inserted **from below the plate**. Ø7 × 3 mm head pockets; about 11.8 mm grip and 8.2 mm engagement in nominal 10 mm pilots. Install before subbase. |
| Rear cup 03 → front cup 02 | 2 | M3 plastic self-tapping through Ø3.4 clearance into Ø2.4 pilots. About 8 mm clearance-side thickness and 8 mm blind pilot depth; choose actual length with tip/bottom clearance. Do not bottom a screw to make the seam close. |
| Collar 05 split clamp | 1 | M3 plastic self-tapping through Ø3.4 clearance into Ø2.4 pilot. Select length for the actual head seat and blind pilot; do not assume a through-bolt/nut joint. |
| Stationary yaw servo → underside of plate 11 | 2 | Matching small servo-ear/plastic screws into Ø1.6 pilots, nominal 6.9 mm available depth. Check the real ear thickness and supplied screws. |
| Tilt servo → carrier 04 | 2 sets | M2 through bolts and nuts, not self-tapping into the Ø2.5 clearance holes. M2 × 14 was a clearance-check candidate, not a verified purchase length; confirm the printed mount/ear/nut stack. |
| Pinions 06 and 07 → servo shafts | 2 total | The **included axial shaft screws**, one per motor. Each hub has a Ø2.5 screw passage and a nominal 1.2 mm seating web; verify engagement and that the screw actually clamps the hub rather than bottoming. |
| Optional arm-foot holes | 4, optional | Not required by the intended glued-arm construction. If used, nominal M2 × 8 **90° countersunk** screws into Ø1.6 pilots; heads must be flush below flange 08. Protruding pan heads foul its underside. |

Also needed: two actual MG90S servos, compatible controller and regulated supply, a means to test the servos unloaded, hand drivers, calipers, local deburring tools, and suitable adhesive/fixtures. No separate yaw shaft, replaceable bushings or loose pitch axle pins are required by this V1 geometry.

## 5. Assembly order

### A. Prepare, label and dry-fit everything

1. Resolve part 08's junction defect before printing/assembly. Import the geometry-only 3MFs in millimeters at 100% scale. Use your PETG manufacturer's profile; no printer/nozzle-specific settings are qualified by this release. Inspect the small spline teeth, gear roots, pin surfaces and screw pockets in sliced preview.
2. Remove supports and burrs without rounding gear teeth or enlarging the intentional locating slots indiscriminately. Label the parts, especially the different arms 09/10 and gears 06/07/08.
3. Test the carrier/output bores on the plate's integral shaft. Test each arm bore on its corresponding integral ball pin **before bonding the arms down**. Check that the ball moves without spreading the arms or being squeezed between their shoulders.
4. Temporarily assemble the rack, carrier, arms and output flange in their CAD positions. Demonstrate both gear meshes and the ball's installation path. Mark orientation with witness marks. If something cannot be seated without force, stop and correct the local print-fit issue before glue makes it permanent.
5. Test spline engagement and shaft-screw seating on both motors with the gears disengaged from their mates. Determine a repeatable safe servo reference and usable travel without running into its internal stops. Record reference pulse/angle; do not assume the full advertised endpoints.

### B. Make the fixed base accessible, not closed

6. Mount the yaw servo under plate 11, with its output shaft pointing up through the offset opening. Its axis is offset toward the rear of the base, not concentric with the yaw shaft. Fit the two ear screws from the accessible underside and route its lead out without trapping it under an ear.
7. Leave yaw gear 07 off for now so the cassette can be checked by hand without back-driving a servo. Leave subbase 13 and the cups off until the upper mechanism and their access paths have been proven.

### C. Prepare the rotating carrier and rack

8. Fit the tilt servo into carrier 04 and install its through bolts/nuts while both sides are accessible. The spline faces the rack side of the ball. Do not let a nut, screw tip or mounting ear touch the future ball/rack path. Temporarily seat pinion 06 to check position, then remove it if needed for ball installation.
9. Dry-locate carrier 04 on repaired output gear/flange 08, using the arms temporarily as an alignment check. Bond the **fixed carrier-to-output interface** off the base, preserving coaxial bores and the CAD orientation. Remove the temporary arms again before the next steps. Keep adhesive out of the journal and let this bond cure fully before loading it.
10. Dry-fit rack 12 in ball 01, confirm its correct face/orientation against pinion 06, then bond it into its locating seat. Remove squeeze-out and let it cure fully. Do not glue the rack to the pinion or use the servo to hold a misaligned rack in position.

### D. Retain the cassette, then capture the ball

11. With the arms still loose and the ball out, lower the carrier/output assembly onto the integral shaft. Fit collar 05 onto the reduced shaft tip while that area is accessible. Tighten its split clamp onto the **fixed shaft**, without clamping the rotating cassette between collar and base. Confirm free yaw and detectable end freedom. The collar is a friction clamp, not a positively keyed connection.
12. Slide arms 09/10 over the ball's corresponding integral pins, then bring their lower locating features into the carrier/flange. **Do not permanently glue both arms to the carrier first and then try to force the ball between them.** Support the ball and loose arms during this operation; do not flex a printed pin to make the installation path work.
13. Before bonding, verify pinion 06 can still be fitted and its axial screw reached. Refit the pinion, check rack engagement through the intended pitch arc, then disengage/remove it as necessary for a free pivot check. The ball must tilt freely with the drive disengaged.
14. Bond the arms only at their **fixed locating faces/feet**, with the ball captured and correctly spaced. Protect the nearby shaft, journal and ball pivots from adhesive. If the trial fit shows that the intended bond faces cannot be reached cleanly in place, remove the loose ball/arms and arrange the glue-up fixture first—do not blindly inject adhesive into the assembled mechanism. Hold the fixed faces seated without squeezing the ball, and leave the assembly undisturbed until full cure.

### E. Time the drives and close the fixed shell

15. With power off, disengage the gears as needed; set each unloaded servo to its recorded reference, then power off again. Position the mechanism at a marked, safe reference pose and install gears 06/07 on the splines. The yaw cassette's forward reference and the pitch reference must be recorded separately; a servo's electrical midpoint is **not automatically** level pitch or the middle of the useful pitch range.
16. Secure both gears with their included axial screws. A spline index may not put the mechanism exactly at the desired zero; record/calibrate that offset. Do not force tooth-to-tooth engagement or change the center distance to hide a bad spline index or print defect.
17. Fit front cup 02 and install its two underside M3 × 20 screws through plate 11. Fit rear cup 03 with its two seam screws. Bring the halves together evenly; the cups must not squeeze the moving ball. A small localized overlap remains in the modeled cup seam, so investigate a seam that will not seat rather than drawing it closed by excessive screw force.
18. Route the tilt-servo cable with a service loop that follows yaw without entering either gear mesh or the ball/cup gap. Keep the yaw-servo lead stationary. Do not assume the small central shaft bore is a connector/cable passage. Check the loop at both yaw extremes and at combined pitch/yaw corners before closure.
19. Only after all underside fasteners, cables and access checks are complete, fit subbase 13 with the four M3 × 25 screws. Tighten gradually in a crossing sequence. Stop if closing the base changes motor clearance or makes a previously free joint bind.

## 6. Fit checks and first motion

These are nominal CAD values, not guaranteed printed tolerances:

| Location | Recorded geometry | Bench check |
|---|---|---|
| Yaw journal | Ø10 shaft / Ø10.5 bores: 0.25 mm radial clearance | Free rotation with drive disengaged; no adhesive or print burrs in bore |
| Retaining collar | Nominal 0.4 mm cassette axial allowance | Clamp shaft securely without eliminating running freedom |
| Pitch pivots | Integral Ø3 pins / Ø3.5 arm bores: 0.25 mm radial clearance | Free tilt; no glue, crushed bore or forced arm spread |
| Arm locating features | Approximately 0.10 mm per-side fit in prior check | Intentionally tight bond location, **not** a bearing to loosen automatically |
| Ball/arm shoulders | Intentional contact | No axial squeeze or adhesive film locking the pivot |
| Yaw gear tooth-phase samples | Minimum surface separation about 0.199 mm | Check the actual printed mesh across travel, not only at center |
| Tilt tooth-phase samples | Minimum surface separation about 0.156 mm | Check tooth engagement and tight spots along the rack |
| Yaw driver to pocket floor | Nominal 0.4 mm allowance | Hub/screw must not bottom or let gear rub the floor |

The two tooth-separation figures are **not circumferential backlash measurements**. Check for slight free play rather than a wedged mesh, continued tooth engagement, and no tooth-tip/root fouling. Never use a servo's torque to wear through a tight spot. PETG print variation, adhesive alignment and cable loads are not covered by the CAD samples.

### Command limits and calibration

- Yaw uses **36T driver → 22T output**, an external gear pair: output direction is opposite the servo. Relative to calibrated reference positions, `yaw = -servo_delta × 36/22`; inversely, `servo_delta = -yaw × 22/36`. This is not the old orbiting-servo formula.
- A total 220° yaw span (±110°) requires about **134.44° total servo travel**; 200° requires about **122.22°**. Confirm the actual motor supports the needed span without internal-stop contact. The gearing increases travel at the expense of output torque; no head-load torque test has been performed.
- Tilt uses the 40T pinion against the internal sector's 60T parent-circle geometry. Nominal magnitude is `pitch_delta = servo_delta × 40/60`; establish the command sign and offset with a small unloaded movement. Do not treat physical tooth count along the partial sector as the ratio.
- Start near the marked reference pose with small, slow commands. Use an appropriate regulated servo supply and controller, keep power cutoff accessible, and keep fingers out of the exposed gears. Stop on sustained buzzing, current rise, rubbing, pin deflection or cable tension.
- For the first PETG trial, use **−30° to +53° pitch as an upper target envelope**, approached gradually from a smaller tested range. Prior geometry checks extended to +55°, but the rack/arm separation there is only about 0.376 mm; at +53° it was about 0.637 mm. **Do not command +60°**: rack/arm and ball/arm collisions were found there. Losing a few degrees is preferable to forcing the prototype.
- Expand yaw only after independent pitch/yaw checks, then test combined extremes slowly with the real cable loop. No continuous 360° yaw is intended. The published collision tests were sampled poses, not a proof of every intermediate configuration.

## 7. Service order and acceptance record

For access: disconnect power, remove subbase to reach underside screws and the stationary servo, then remove the cup seam screws and cup-foot screws as needed. Remove a servo's gear/axial screw before withdrawing that servo; support the moving cassette before releasing its retaining collar. Remove the ball/carrier module together when practical. Because the arms capture integral pins and are glued, **ball removal from the arms is not a promised nondestructive service operation**. Plan the glue-up accordingly.

Before adding a head or running unattended, record:

- [ ] Output gear junction repaired, revalidated and inspected in sliced preview.
- [ ] All parts present; both motors and gears positively retained; screws do not bottom.
- [ ] Rack and fixed cassette bonds fully cured; no adhesive on teeth, pivots or journal.
- [ ] Ball captured without stressing pins; free tilt and yaw with drives disengaged.
- [ ] Collar retained without binding; shell and base closure do not change free motion.
- [ ] Actual spline fits, servo reference pulses, command signs and travel limits recorded.
- [ ] Small-range powered tests passed, then independent ranges and combined corners passed.
- [ ] Cable loop clears all moving parts; no rubbing, persistent buzzing or loosening.
- [ ] Agreed reduced pitch/yaw limits entered in the controller rather than relying on hard stops.

Record actual results here or in a build log: printer/filament, adhesive and cure, screw types/lengths, measured fits, servo identities, reference pulses, safe endpoints and any local print cleanup. Blank checklist items are not passes.

## Basis and scope

Source snapshot: repository commit `d78756fcf08e372599ab277d90207cca4cd53700`, native [`test-neck-assy-v1.f3d`](test-neck-assy-v1.f3d), SHA-256 `e49f51dc8814df33fcf1f81e574cfd7a8f147ac7186aea4ea0e96149a35a6534`. The guide was checked against the saved V1 native body inventory, cylindrical surfaces and mating-surface distances, plus the previously recorded fit/motion checks summarized in the [package README](README.md). A direct native point-containment check distinguishes the ball's **solid pins** from the arms' **bores**; cylindrical surface dimensions alone do not make that distinction.

The assembly order and bonding procedure are engineering recommendations from those interfaces and Joshua's glued-rack/glued-arm prototype intent. They still require the full dry-fit installation/access check before irreversible bonding. No physical assembly, adhesive-strength qualification, load test, slicer profile qualification or endurance test is claimed. The native file and all mesh files remain unchanged by this documentation addition. See [ATTRIBUTION.md](ATTRIBUTION.md) for the OB-3D source and CC BY-SA 4.0 terms.
