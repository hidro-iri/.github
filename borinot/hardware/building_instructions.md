# Building Instructions

The instructions are devide between the upper body (flying platform) and the lower body (landing gear and leg).

## Airframe Assembly

The airframe is part of the upper body. In this step you will assemble the motors and escs to the motor case and the carbon fiber frame.
> :warning: the motors are identified using the [Hexarotor X airframe reference](https://docs.px4.io/main/en/airframes/airframe_reference.html#hexarotor-x)

### 3D preparation

- cleaning 3D parts. Remove entirely the support inside the tube holder.
- For each motor, assemble the marker (M4 nut + M4 nylon screw + M4 marker) (follow the pose regarding the motor):

| Motor ID | Marker Position |
|:-:|---|
| 1 | Bottom Right |
| 2 | Top Right |
| 3 | Top Left |
| 4 | Bottom Left |
| 5 | Top Right |
| 6 | Bottom Right |

- On the bottom part, put two inserts
- Assemble the cache

### Motor wiring

- cut phases cable around 5cm
solder the male phase connector
- put thermoretactile around each connector

### esc wiring

- phase:
  - solder 5cm cable (from motor)
  - solder female phase connectors
  - put thermo around full connector
- power:
  - solder ...cm cable (red for + and black for minus)
  - put thermo around cable (do not heat it)
  - solder xt18 connector
  - put thermo around connector (first heat the cable, after connector)
- signal:
  - solder ... cm cable (white for signal and black for ground)

### Assembling

- Put motor top, middle and bottom together
- ith 4xM3x30 (Put the o-ring on the carbon tube and in the corresponding tube holder and motor)
- put esc in motor support
- put cache with 2xM3x6

---

## Lower Body Assembly

The Lower Body is composed by:

- The landing gear,
- The arm (which is composed by the the flying link, the odri link and the extremity),
- The odri controller.

---

## Arm Assembly - Extremity

### Components list

| Part Name | Quantity |
|:-|:-:|
| [Extremity - 3D Kit](CAD/limbs/) | 1 |

### 3D Preparation

- Clean the extremity part

---

## Arm Assembly - ODRI link

This section is cover by the [actuator module page](https://github.com/open-dynamic-robot-initiative/open_robot_actuator_hardware/blob/master/mechanics/actuator_module_v1/README.md#brushless-actuator-module-core-v1) of the ODRI project.

---

## Arm Assembly - Flying link

### Components List

| Part Name | Quantity |
|:-|:-:|
| [Flying link - 3D Kit](CAD/limb/) | 1 |
| Ouput Bearings | 2 |
| Transmission Bearings | 3 |
| M3x5mm flat head Screws | 4 |
| M3x15mm Screw | 4 |
| M3x16mm Flat Head nylon Screw | 2 |
| M3x20mm flat head Screws | 6 |
| 201mm timing belt | 1 |
| 150mm timing belt | 1 |
| M3 Nuts | 18 |
| M3 Inserts | 2 |

### 3D Preparation

- :warning: Clean the 3D Kit.
- For each part of the **Flying - 3D Kit**, insert the **M3 Nuts** inside the corresponding emplacements.
- For each part of the **Flying - 3D Kit**, insert the **M3 Inserts** inside the corresponding emplacements.
- For each part of the **Flying - 3D Kit**, insert the **Ouput Bearings** inside the corresponding emplacements.
- For each part of the **Flying - 3D Kit**, insert the **Transmission Bearings** inside the corresponding emplacements.

### Assembly

- Put the motor inside the flying case A and maintain it with 4 screws.
- Put the 150mm timing belt arround the motor ax.
- Put the encoder next to the motor and maintain it using the nylon screws.
- Put the odri 3D part with the 201mm timing belt and close using the flying case B and the 6 20mm screws.
- Put the odri link and the extremity. fix it using the 15mm screws.

---

## Odri Controller Assembly

### Components List

| Part Name | Quantity |
|:-|:-:|
| [Controller Case - 3D Kit](CAD/platform/) | 1 |
| master board | 1 |
| micro driver | 1 |
| M2 Nuts | 4 |
| M2.5 Nuts | 4 |
| M3 Inserts | 3 |
| M3x5mm Screws| 3 |
| M2x6mm Screws | 4 |
| M2.5x6mm Screws | 4 |

### 3D Preparation

- :warning: Clean the 3D Kit
- For each part of the **Controller Case - 3D Kit**, insert the **M2 Nuts** inside the corresponding emplacements.
- For each part of the **Controller Case - 3D Kit**, insert the **M3 Nuts** inside the corresponding emplacements.
- For each part of the **Controller Case - 3D Kit**, insert the **M3 Inserts** inside the corresponding emplacements.

### Assembly

- Put the master boar inside the controller case - top. Maintain it with the M2 screws.
- Put the micro driver inside the controller case - bottom. Maintain it with the M2.5 screws.
- Connect the two links with the micro driver (the cable should pass throught the hole of the controller case and the flying case).
- Connect the micro driver and the master board, and close the case with 3 M3 screw.

---

## Landing Gear Assembly

### Components list

| Part Name | Quantity |
|:-|:-:|
| [Landing Gear - 3D Kit](CAD/legs/) | 1 |
| Ø20mm O-Ring Seals | 12 |
| M3x10mm Screws | 8 |
| M3x16mm Screws | 8 |
| M3 Nuts | 16 |
| Ø8mmx6mmx110.0mm Carbon Fiber Round Checked Tubes | 4 |
| Ø8mmx6mmx170.0mm Carbon Fiber Round Checked Tubes | 2 |
| Ø8mmx6mmx300.0mm Carbon Fiber Round Checked Tubes | 2 |

### 3D Preparation

- :warning: Clean the 3D Kit (If you have difficulties to insert a tube inside one of the 3d prints, you should clean the entry)
- For each part of the **Landing Gear - 3D Kit**, insert the **M3 Nuts** inside the corresponding emplacements.
- For each **pawn**, put 3 **Ø20mm O-Ring Seals** around it.

### Assembly

- First assemble the wye connectors and the pawns with the 300mm CF tube following the picture. Do it 2 times.
- Assemble the cross-block connectors with the 170mm CF tube following the picture. Do it 2 times.
- Assemble the all together using the 4 110mm CF tubes following the picture.
