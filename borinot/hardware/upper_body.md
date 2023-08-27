# Borinot: Upper Body Assembly Guide

<img src="../media/upperbody_final_top.png" alt="Top view of the assembled upperbody" width="350"/>

> *Assembled Upper Body, [**weight**] g*
<!-- Make sure to provide the actual weight once known -->

The Upper Body of Borinot acts as a flying platform, similar to a hexacopter. It consists of the main body (which houses essential electronics like the onboard NUC computer, the Pixhawk flight controller, and the power module) and the airframe. This structure keeps the motors in their respective positions. The Upper Body can operate as a standalone hexacopter or be integrated into the Lower Body for expanded functionalities.

---

## Components list

| Part Name | Quantity | Description | Reference |
|:-|:-:|:-|:-:|
| Main Body Case | 1 | 3D parts - Stack | [CAD](CAD/platform/) |
| NUC | 1 | NUC Kit NUC7i7DNKE | [intel](https://ark.intel.com/content/www/us/en/ark/products/130392/intel-nuc-kit-nuc7i7dnke.html) |
| Pixhawk 5x | 1 | Flight Controller | [Holybro](https://holybro.com/products/pixhawk-5x?variant=40842119839933) |
| Ethernet Converter | 1 | [**Specify dimension**] | [**Specify Link**] |
| USB C Cable | 1 | [**Specify dimension**] | [**Specify Link**] |
| Wi-Fi Antenna | 1 | Wi-Fi Antenna | [**Specify Link**] |
| Radio Receiver | 1 | Radio | [RC Innovations](https://rc-innovations.es/shop/FS-iA6B-receptor-6-canales-telemetria-flysky) |
| Damper | 10 | For Pixhawk | [**Specify Link**] |
| M3 Nuts | 16 | Hex, M3 | [RS](https://uk.rs-online.com/web/p/hex-nuts/0198318) |
| M3 6mm Screws | 4 | M3x6mm | [RS](https://uk.rs-online.com/web/p/socket-screws/0281372) |
| M3 10mm Screws | 4 | M3x10mm | [RS](https://uk.rs-online.com/web/p/socket-screws/0281394) |
| M3 16mm Screws | 4 | M3x16mm | [RS](https://uk.rs-online.com/web/p/socket-screws/0292423) |
| Long Carbon Fiber Tubes | 4 | 5mmx3mmx150mm, Square | [McMaster](https://www.mcmaster.com/products/carbon-fiber-tubing/) |
| Short Carbon Fiber Tubes | 2 | 5mmx3mmx65mm, Square | [McMaster](https://www.mcmaster.com/products/carbon-fiber-tubing/) |
| Airframe | 1 | Assembled structure | [Airframe Assembly Guide](airframe.md) |
| Power Module | 1 | Essential power component | [Power Module Modification Guide](power_module.md) |

> :warning: Note: While Pixhawk 5x is discontinued, Pixhawk 6x is mechanically compatible. However, ensure to test the software compatibility.

## Assembly

### Prerequisite: Component Preparations

Before starting the assembly of the upper body, ensure that:

1. The power module has been modified following the [Power Module Modification Guide](power_module.md).
2. The airframe has been assembled following the [Airframe Assembly Guide](airframe.md).

### Part 1: Main Body Case Preparation

Ensure the main body case and associated components are ready for assembly:

- **Clean the 3D printed parts.** Ensure there are no residual supports or anomalies.
    > :warning: Pay special attention to the marker holders and fastener holders.
- **Install the M3 nuts and dampers onto the Pixhawk case.**
- **Insert the 65mm square carbon fiber tubes into the Pixhawk case.**
- **Attach the battery support to the Pixhawk case using M3 10mm screws.**
- **Position the M3 nuts and dampers on the top part of the main body case.**
- **Place the M3 nuts on the bottom part of the main body case.**

### Part 2: Main Body Assembly

The main body requires careful placement and connection of components:

- **Attach the Wi-Fi antenna to the Pixhawk case using fasteners.**
- **Mount the power module onto the top part of the main body using 4 M3 6mm screws.**
- **Secure the Ethernet adapter and radio receiver to the top part using fasteners.**
- **Place the Pixhawk 5x inside its designated case.**
- **Guide the cables of the Pixhawk and the antenna through the corresponding holes in the top part.**
- **Secure the Pixhawk case to the top part using fasteners.**
- **Connect the NUC to the power module using the designated computer cable.**
- **Connect the NUC to the Wi-Fi antenna.**
- **Position the bottom part of the main body inside the contour part.**
- **Insert the 150mm square carbon fiber tubes into the top and bottom parts of the main body case.**
- **Place the NUC inside the main body case and secure it to the bottom part using 4 M3 16mm screws.**
- **Establish connections:**
  - **Connect the Pixhawk 5x Ethernet cable to the NUC.**
  - **Connect the Pixhawk 5x power cable to the power module.**
  - **Connect the Pixhawk 5x USB cable to the NUC using the USB C cable.**

Ensure all components are secured and all connections are verified before moving to the next stages of your project.
