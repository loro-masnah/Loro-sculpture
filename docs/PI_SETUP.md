# Starting from a new Raspberry Pi 4 Model B

1. Identify onboard RAM (2GB/4GB/8GB): 4GB is recommended for a cloud-assisted prototype; 8GB is useful but not required. RAM cannot be upgraded separately.
2. Obtain a reliable 64GB microSD card, a suitable 5.1V/3A USB-C power supply, and the Pi 4-compatible 15-pin Camera Module 3 ribbon cable.
3. Use Raspberry Pi Imager to install supported **64-bit Raspberry Pi OS**. Set username, secure password, Wi-Fi and SSH as appropriate.
4. Boot and update the system. Record the OS version and firmware before adding BrainCraft audio drivers.
5. Connect the camera with power OFF. Test using `rpicam-hello --list-cameras` and `rpicam-still -o test.jpg` (commands may differ by OS release).
6. Fit the BrainCraft HAT to the 40-pin GPIO header with suitable standoffs and power OFF. Follow Adafruit's specific audio codec configuration for the installed OS.
7. Connect **one 8Ω 1W speaker** to the appropriate HAT channel using the correct JST-PH wiring; test audio before enclosure assembly.
8. Configure a Python virtual environment; do not commit credentials or local image captures to GitHub.

## References
- https://www.raspberrypi.com/software/
- https://www.raspberrypi.com/documentation/accessories/camera-software.html
- https://learn.adafruit.com/adafruit-braincraft-hat-easy-machine-learning-for-raspberry-pi/overview
- https://learn.adafruit.com/adafruit-braincraft-hat-easy-machine-learning-for-raspberry-pi/audio-setup

**Note:** BrainCraft is an older HAT and audio support on recent OS builds must be verified, not assumed.
