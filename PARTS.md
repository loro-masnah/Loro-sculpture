# Parts list – Parrot Head Prototype 1

Buy in two rounds. Round 1 gets the beak talking on the bench (build steps 1–3 in the README).
Round 2 adds the neck (turn and nod) once the beak works.

Prices were checked in November 2026 and may change. "Example" parts are ones that meet the
spec; any servo with the same size, speed and torque will work.

## Already have

- [x] Raspberry Pi 4 + its power supply + microSD card
- [x] Adafruit BrainCraft HAT

## Round 1 – electronics and beak (buy first)

| Qty | Part | Why | Example / notes |
|----:|------|-----|-----------------|
| 1 | **Adafruit PCA9685 16-channel servo driver** (product 815) | Drives all servos over I²C | $14.95 at adafruit.com. Needs light soldering of the header pins. |
| 1 | **STEMMA QT / Qwiic to female-socket jumper cable** | Connects the BrainCraft's STEMMA QT port to the driver's header pins (the 815 has no STEMMA QT port of its own) | Adafruit or SparkFun, 4-pin JST-SH to female sockets |
| 1 | **6 V regulated DC power supply, 5 A or more** | Separate servo power, so snapping servos can't reset the Pi | Any regulated 6 V 5 A+ switching supply with a 2.1 mm barrel plug |
| 1 | **Female DC barrel jack to screw-terminal adapter** (2.1 mm) | Connects the supply to the driver's power terminal | — |
| 1 | **1000 µF electrolytic capacitor, 10 V or higher** | Absorbs servo current spikes; fits on the driver board | — |
| 2 | **Micro metal-gear servo, 180°** (one is a spare) | BEAK (channel 2) | Example: Turnigy TGY-R5180MG (2.0 kg·cm, 0.10 s/60° at 6 V, 180°) or any MG90S-class micro servo |
| 1 | **Small speaker, 4–8 Ω, 1–3 W, with a JST-PH 2-pin plug** | Plugs into the BrainCraft speaker port | Small enclosed speakers sound better |
| 1 | **Pushrod kit** (about 2 mm rods, clevises or ball links) | Links the beak servo to the lower-beak hinge | RC-plane pushrod sets work well |
| 1 | **Pack of servo extension cables, 30 cm** | Lets cables run down the neck later | — |

## Round 2 – neck: turn and nod (buy once the beak works)

| Qty | Part | Why | Example / notes |
|----:|------|-----|-----------------|
| 1 | **Fast standard-size digital metal-gear servo** | TURN (channel 0); snap speed matters most | Example: Power HD DS120M (0.11 s/60° and 12.8 kg·cm at 6 V, metal gears, two ball bearings). **Check its travel range covers about ±85°.** |
| 1 | **Standard-size metal-gear servo, high torque** | NOD (channel 1) | Example: Adafruit 1142 (10 kg·cm, 0.16 s/60° at 6 V, $19.95). Fine for a light foam head; choose 15–20 kg·cm if the head gets heavy. |
| 1 | **Lazy-susan turntable bearing, about 75–100 mm** | Carries the head's weight so the turn servo only rotates it | Hardware store or online |
| 2 | **Metal servo horns or hubs** matching the servo splines (usually 25T) | Strong joints for the turn and nod axes | Match the spline to the servos you buy |
| 1 | **Servo bracket / pan-tilt bracket set** | Mounting the turn and nod servos | Aluminium bracket kits are cheap and adjustable |
| 1 | **Springs or elastic cord** | Counterbalance for the nod axis | — |
| — | **M3 screws, nuts and standoffs** | General assembly | — |
| — | **Prototype head material**: foam, cardboard, 3D-printed parts or thin plywood | Rough skeleton head, not the final sculpture | — |

## Useful tools

- Soldering iron (for the driver's header pins)
- Multimeter (check the 6 V supply and polarity before connecting servos)
- Hot glue and zip ties

## Later phases (do not buy yet)

- Raspberry Pi 5 (8 GB) + Raspberry Pi AI HAT+ 2 + Active Cooler: the offline "brain"
- Optional 4th servo: TILT (channel 3)
- Wing and tail servos, final sculpture materials, ventilated base, spare-parts kit
