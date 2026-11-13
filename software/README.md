# Software package — TODO
No executable application has been implemented yet.

Planned modules:
- `camera.py`: capture still image from Camera Module 3.
- `vision.py`: extract objects and scene.
- `retrieval.py`: select knowledge notes relevant to scene.
- `personality.py`: load configuration and format prompt.
- `generation.py`: invoke AI provider safely.
- `speech.py`: convert and play speech.
- `controller.py`: triggers, cooldown, retry and state management.
- `main.py`: initialize and run.
- systemd service and tests.

See [architecture](../docs/SOFTWARE_ARCHITECTURE.md). Implement incrementally, starting with independent camera and audio smoke tests.
