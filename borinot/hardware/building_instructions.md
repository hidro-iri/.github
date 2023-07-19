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

## Lower Body Assembly

The Lower Body is composed by:

- The landing gear,
- The arm (which is composed by the the flying link, the odri link and the extremity),
- The odri controller.

## Landing Gear Assembly

### Components list

| Part Name | Quantity |
|:-|:-:|
| [Landing Gear - 3D Kit](cad_files/landing_gear/) | 1 |
| Ø20mm O-Ring Seals | 12 |
| M3x10mm Screws | 8 |
| M3x16mm Screws | 8 |
| M3 Nuts | 16 |
| Ø8mmx6mmx110.0mm Carbon Fiber Round Checked Tubes | 4 |
| Ø8mmx6mmx170.0mm Carbon Fiber Round Checked Tubes | 2 |
| Ø8mmx6mmx300.0mm Carbon Fiber Round Checked Tubes | 2 |

### 3D Preparation

- :warning: Clean the 3D Kit (If you have difficulties to insert a tube inside one of the 3d prints, you should clean the entry)
- Insert
- For each part of the **Landing Gear - 3D Kit**, insert the **M3 Nuts** inside the corresponding emplacement.
- For each **pawn**, put 3 **Ø20mm O-Ring Seals** around it.

### Assembly

- First assemble the foots and the pawn with the 300mm CF tube following the picture. Do it 2 times.
