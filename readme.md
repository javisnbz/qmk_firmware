# Modified Keychron/Lemokey QMK Firmware

[![Star this repo](https://img.shields.io/github/stars/Keychron/qmk_firmware?style=social&label=Star%20this%20repo)](https://github.com/Keychron/qmk_firmware)

Modified QMK firmware for Keychron and Lemokey keyboards hall effect, Auto-calibration no longer persistently writes data to the EEPROM, resulting in greater accuracy; it will always retain the manual calibration performed in Keychron Launcher.

## Why Open Source?

Keychron is the first major keyboard brand to fully open-source both its [firmware](https://github.com/Keychron/qmk_firmware) and [hardware design](https://github.com/Keychron/Keychron-Keyboards-Hardware-Design). We believe you should be able to see, verify, and modify every line of code that runs on your keyboard. Open source means full transparency — no black boxes between you and your hardware.

We also want to build something bigger than what any single company can do alone. By opening our firmware to the community, developers and enthusiasts can push what keyboards are capable of — custom keymaps, new features, creative workflows — and those contributions make every Keychron keyboard better for everyone.

## Features

- **Hall Effect magnetic switch support** — adjustable actuation and rapid trigger on HE boards
- **Wireless connectivity** — Bluetooth 5.1 and 2.4 GHz firmware for wireless models
- **[Keychron Launcher](https://launcher.keychron.com/)** — remap keys, tune HE settings, and configure lighting from your browser with no setup
- **RGB Matrix lighting** — per-key RGB effects and customization
- **Multiple layout variants** — ANSI, ISO, and JIS for every supported board
- **Full QMK feature set** — layers, tap-dance, combos, macros, encoders, OLED, and more

## Getting Started

### How to flash the firmware

Download the firmware corresponding to your exact model, whether it's ANSI, ISO, or JIS.

1. Download QMK Toolbox: https://qmk.fm/toolbox and install.
2. When you open it, it will ask if you want to install the drivers; select yes.
3. With the keyboard disconnected from the USB port, hold down the ESC key while connecting it via USB. The keyboard will enter flashing mode; you will see some yellow text in QMK Toolbox.
4. Press the OPEN button and select the firmware you downloaded.
5. Press the FLASH button, the QMK Toolbox will start erasing and writing the firmware, once it finishes the program will automatically disconnect and the keyboard will be flashed.
6. Go to the Keychron Launcher website https://launcher.keychron.com/ and perform a manual calibration of all keys; this calibration will be saved permanently until you recalibrate.


### Compile the firmware
See the [QMK build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and [make guide](https://docs.qmk.fm/#/getting_started_make_guide) for details. New to QMK? Start with the [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).

build examples:

```bash
qmk compile -kb keychron/k10_he/iso -km via
```



## Supported Keyboards

Keychron: K2HE, K4HE, K6HE, K8HE, K10HE, Q1HE, Q3HE, Q5HE, Q6HE

Lemokey: L1HE, P1HE

All board definitions live under [`keyboards/keychron/`](keyboards/keychron/) and [`keyboards/lemokey/`](keyboards/lemokey/).



Each board folder contains its own `readme.md` with exact build targets, product links, and reset instructions.

## Hardware Design

For PCB files, schematics, and hardware design resources, see the companion repository:

[Keychron-Keyboards-Hardware-Design](https://github.com/Keychron/Keychron-Keyboards-Hardware-Design)

## Community and Support

- **Join the community**  
  Join the [Keychron Discord](https://discord.com/invite/HAYbRrTsjN) to share builds, ask questions, and help grow the hardware modding community.
- [Keychron Website](https://www.keychron.com)
- [Keychron on Reddit](https://www.reddit.com/r/Keychron/)
- [QMK Discord](https://discord.gg/qmk)
- [QMK Documentation](https://docs.qmk.fm)

## Contributing

Contributions are welcome — whether it's a new keymap, a bug fix, or documentation improvement. See [`docs/contributing.md`](docs/contributing.md) for guidelines on submitting pull requests.

## License

This project is licensed under the [GNU General Public License v2.0](LICENSE).

This repository tracks the [upstream QMK firmware](https://github.com/qmk/qmk_firmware) with Keychron-specific board definitions and firmware additions.
