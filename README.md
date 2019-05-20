# The Yampad project repository

<p align="center">
<img src="img/yampad_logo.png" alt="Yampad logo" width="450"/>
<img src="img/qmk-badge-dark.png" alt="QMK" width="145"/>
</p>

The Yampad project is an open-source, [QMK (Quantum Mechanical Keyboard Firmware)](https://github.com/qmk/qmk_firmware) powered, hot-swappable, RGB-backlighted, OLED featured, mechanical numpad. This repository will be used to share information about the project and instruction on how to use and assembly the Yampad.

<p align="center">
<img src="img/yampad.jpg" alt="Yampad PCB" width="600"/>
</p>

**Designer's bio**: [Mattia Dal Ben (aka u/TiaMaT102)](mailto:matthewdibi@gmail.com) obtained a master's degree in Electrical Engineering with a specialization in Computer Science at the University of Udine. Currently works as a Software Engineer in R&D department for a big IoT and Embedded Computers company.

## Rationale

The Yampad is a Macropad/Numpad which uses Cherry MX style mechanical switches laid out in the usual numeric pad layout. The only difference comes from the bottom row, which uses a 4 keys configuration, thus enabling the use of the macropad as a nav cluster.

The name comes from the acronym: **Y**et **A**nother **M**echanical num**PAD**, referring to the disruptive and innovative nature of the project.

The main goal of this project is to have a cheap, easy-to-build, feature-rich numpad which is completely open source.

Features:
- Cheap to build.
- Easy to source components.
- Easy to build.
- Hot swappable keys using *Kailh PCB sockets*.
- Arduino Pro Micro powered.
- QMK compatible.
- RGB backlighting support (optional).
- OLED 0.91" screen (optional).
- Completely open-source.

#### Useful links

- [YamPAD on Hackaday.io](https://hackaday.io/project/163491-yampad-feature-packed-open-source-macropad)

## Default Layout

<p align="center">
<img src="img/Layer1.png" alt="Layer 1 Yampad" width="300"/>
<img src="img/Layer2.png" alt="Layer 2 Yampad" width="300"/>
</p>

## Bill of materials

| Qty | Item                                 | Notes                                     |
|-----|--------------------------------------|-------------------------------------------|
| 1   | Arduino Pro Micro                    |                                           |
| 18  | Cherry MX compatible swtiches        |                                           |
| 18  | SOD-123 1N4148/1N4148W diodes        |                                           |
| 18  | Kailh PCB sockets CPG151101S11       |                                           |
| 9   | WS2812B RGB LEDs                     |                                           |
| 9   | SMD 0805 100nF capacitors            |                                           |
| 1   | I2C 0.91" 128*32 OLED Display Module | The ones using SSD1306 driver IC over I2C |
| 1   | 6mm*6mm button switch                |                                           |
| 1   | YamPAD PCB                           |                                           |
| 5   | M3 screws                            |                                           |

## Assembly guide

WIP

## Firmware

For now the firmware is available through mattdibi's [QMK firmware repository fork](https://github.com/mattdibi/qmk_firmware/tree/yampad).

Make example for this keyboard (after setting up your build environment):

```sh
make yampad:default
```

Example of flashing this keyboard:

```sh
make yampad:default:avrdude
```

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).

### Donations

If you've read this far and found something useful, please consider donating to help me maintain and further develop this project.

<p align="center">
<a href="https://www.paypal.me/MattiaDalBen"><img src="img/donate-button.jpeg" alt="Donate button" width=300/></a>
</p>
