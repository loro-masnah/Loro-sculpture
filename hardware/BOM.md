# Hardware bill of materials (BOM)

Prices are **planning estimates in USD**, not live checkout quotes. Exclude sales tax, shipping, sculpture labor and ongoing cloud AI usage.

| Part | Quantity | Status | Estimated purchase cost | Notes |
|---|---:|---|---:|---|
| Raspberry Pi 4 Model B | 1 | Owned | $0 | RAM amount unknown; 4GB recommended for cloud AI; 8GB optional |
| Adafruit BrainCraft HAT #4374 | 1 | Owned | $0 | Includes audio codec, fan, microphones, GPIO and display |
| Raspberry Pi Camera Module 3 | 1 | Owned | $0 | 12MP autofocus |
| microSD card, good quality 64GB | 1 | Check/buy | $10–20 | OS, code and knowledge notes |
| Pi 4 USB-C 5.1V 3A supply | 1 | Check/buy | $9–15 | Stable mains power |
| Camera ribbon cable, Pi 4 15-pin | 1 | Check/buy | $0–10 | May already be included |
| 8Ω 1W enclosed speaker | 1–2 | Buy | $4–10 each | Mount inside parrot chest |
| JST-PH 2-pin speaker cables | 1–2 | Check/buy | $2–6 total | Verify connector |
| Wires, standoffs, brackets, strain relief | Set | Buy | $10–35 | Serviceable mounting |
| Recycled body materials | Set | Gather | $0–100 | Artist fabrication |
| Optional beak servo & suitable power supply | 1 | Optional | $15–50 | Add after speech milestone |
| Optional powered external speaker/amp | 1 | Optional | $25–90 | For noisy gallery |

**Basic additional electronics budget:** about $35–106 excluding owned main components. Exact total depends on purchases already in hand and speaker count. Check real supplier availability before buying.

## RAM guidance
The Pi 4 Model B RAM is part of the board, not the microSD. Verify the installed capacity before spending on another Pi. 4GB works with cloud AI; intensive local models may need stronger hardware.

## Audio recommendation
Start with one enclosed **8Ω 1W** speaker on one HAT amplified channel. Do not wire two speakers in parallel on one channel. Test gallery intelligibility before considering external amplification.

## References
- https://www.adafruit.com/product/4374
- https://learn.adafruit.com/adafruit-braincraft-hat-easy-machine-learning-for-raspberry-pi/required-parts
- https://www.raspberrypi.com/documentation/accessories/camera.html
