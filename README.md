# AI Parrot — Interactive Sculpture

**Status:** pre-production | **Scope:** one working sculpture in 30 days | **Updated:** November 2026

A parrot-sized artwork. A hidden camera observes everyday objects; a Raspberry Pi describes the scene, retrieves ideas from a curated knowledge archive, and speaks a short interpretation. The parrot embodies how humans absorb beliefs and repeat them as if they were their own. The artwork examines social media, algorithmic echo chambers, and older ideological influences.

## Project scope
- Prototype **one physical parrot** first, designed to scale to five distinct sculptures and personalities.
- Build **The Philosopher**, influenced by Alan Watts, Zen, Taoist themes, attention and impermanence.
- Document **The Radical**, influenced by leftist critique, as an alternate personality for later testing.
- Treat interpretation and object recognition separately: same visible facts can lead to different ideological conclusions.
- Responses should be original; never invent attributed quotes.

## Hardware already owned
- Raspberry Pi 4 Model B (**RAM size not yet confirmed**, 4GB recommended with cloud AI)
- Adafruit BrainCraft HAT #4374
- Raspberry Pi Camera Module 3

See [hardware/BOM.md](hardware/BOM.md) for the purchase checklist.

## Mechanical prototype files

[Test neck assy v1](hardware/test-neck-assy-v1/) contains the native Fusion assembly and 13 named component 3MFs for the MG90S/PETG neck prototype. Read its limitations before printing: the yaw output gear has a known non-manifold junction requiring repair. This is a test checkpoint, not a qualified hardware release.

## Work plan
1. [30-day plan](docs/30_DAY_PLAN.md)
2. [Fresh Pi setup](docs/PI_SETUP.md)
3. [System architecture](docs/SOFTWARE_ARCHITECTURE.md)
4. [Personality design](docs/PERSONALITY_DESIGN.md)
5. [Acceptance checklist](tests/ACCEPTANCE.md)
6. [Open decisions](docs/OPEN_DECISIONS.md)

## Technical status
**Documentation only — software is not implemented yet.** The plan calls for camera capture, scene grounding, knowledge retrieval, language generation, speech output, and unattended recovery.

## Privacy and licensing
Do not upload API keys, Wi-Fi credentials, visitor images, unlicensed books/transcripts, or private artistic research to this public repository. Keep restricted source materials in private storage and maintain backups.

## References
- [BrainCraft HAT](https://learn.adafruit.com/adafruit-braincraft-hat-easy-machine-learning-for-raspberry-pi/overview)
- [Raspberry Pi camera software](https://www.raspberrypi.com/documentation/accessories/camera-software.html)
