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
- Cheap to build: the PCB can be manufactured for less than 1$ per piece.
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
<img src="img/BL.png" alt="Layer 1 Yampad" width="250"/>
<img src="img/NV.png" alt="Layer 2 Yampad" width="250"/>
<img src="img/FN.png" alt="Layer 3 Yampad" width="250"/>
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
| 1   | YamPAD PCB                           | [Order from PCBWay](https://www.pcbway.com/project/shareproject/YamPAD_mechanical_numpad.html) |
| 5   | M3 screws                            |                                           |

## Assembly guide

There's no wrong order for the YamPAD assembly with the exception of the Arduino/OLED/ResetButton. Here I will suggest an order because I found more comfortable to solder the components this way.

1. Start with soldering the **WS2812 LEDs**. Start by applying solder to a pad, then heat it up while adding the component, finally solder the remaining pads.
2. Now add the **0805 100nF caps**. Use the same technique as before.
3. Add the **1N4148 diodes**.
4. Add the **CPG151101S11 Kailh PCB sockets**.
5. Add the **reset 6mm button switch**.
6. Add some electrical tape just to be sure.
7. Add the **Arduino Pro Micro** bottom side up.
8. Add the **OLED screen**
9. Move to the firmware section and you should be set!

<p align="center">
<img src="img/assembly/stage1.jpg" alt="Stage 1" width="250"/>
<img src="img/assembly/stage2.jpg" alt="Stage 2" width="250"/>
<img src="img/assembly/stage3.jpg" alt="Stage 3" width="250"/>
</p>
<p align="center">
<img src="img/assembly/stage4.jpg" alt="Stage 4" width="250"/>
<img src="img/assembly/stage5.jpg" alt="Stage 5" width="250"/>
<img src="img/assembly/stage6.jpg" alt="Stage 6" width="250"/>
</p>

### Assembly details

#### Step 1: WS2812 assembly

<p align="center">
<img src="img/assembly/step1-a.jpg" alt="Step 1-a" width="250"/>
<img src="img/assembly/step1-b.jpg" alt="Step 1-b" width="250"/>
<img src="img/assembly/step1-c.jpg" alt="Step 1-c" width="250"/>
</p>

#### Step 2: Capacitors assembly

<p align="center">
<img src="img/assembly/step2.jpg" alt="Step 2" width="600"/>
</p>

#### Step 3: Diodes assembly

<p align="center">
<img src="img/assembly/step3.jpg" alt="Step 3" width="600"/>
</p>

#### Step 4: Kailh PCB sockets assembly

<p align="center">
<img src="img/assembly/step4-a.jpg" alt="Step 4-a" width="300"/>
<img src="img/assembly/step4-b.jpg" alt="Step 4-b" width="300"/>
</p>

#### Step 5: Reset switch

<p align="center">
<img src="img/assembly/step5.jpg" alt="Step 5" width="300"/>
</p>

#### Step 6: Electrical tape

<p align="center">
<img src="img/assembly/step6.jpg" alt="Step 6" width="300"/>
</p>

#### Step 7: Arduino assembly

<p align="center">
<img src="img/assembly/step7-a.jpg" alt="Step 7-a" width="300"/>
<img src="img/assembly/step7-b.jpg" alt="Step 7-b" width="300"/>
</p>

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

#### Pre-built

I also added a pre-built .HEX file in the 'firmware/' folder [here](https://github.com/mattdibi/yampad/tree/master/firmware) to test the electronics.

### Donations

If you've read this far and found something useful, please consider donating to help me maintain and further develop this project.

<p align="center">
<a href="https://www.paypal.me/MattiaDalBen"><img src="img/donate-button.jpeg" alt="Donate button" width=300/></a>
</p>
