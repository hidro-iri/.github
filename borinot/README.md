# Borinot 🐝

Borinot is an open-source Unmanned Aerial Manipulator (UAM), developed by the HiDRo group. This torque-controlled robot is designed for hybrid flying and contact loco-manipulation. It utilizes its extremity as a tail for flying locomotion, a hand for agile aerial manipulation, or a leg for hybrid aerial-contact locomotion. Check out a demo of Borinot [here](<!-- Add video link -->).

<!-- Quick section of the main software associate with it: eagle_mpc_lib -->

## Table of Contents

- **[Hardware](hardware/README.md)**
  - [Components List](hardware/components_list.md)
  - [Building Instructions](hardware/building_instructions.md)
- **[Software](software/README.md)**
  - [MPC Controller](software/eagle_ros2/control/mpc_controller.md)
  - [Decentralized Controller](software/eagle_ros2/control/decentralized_controller.md)
- **[Resources](resource/README.md)**
  - [Preflight Checks](resource/preflight.md)
  - [Optitrack Fusion](resource/optitrack.md)
  - [Troubleshooting](resource/troubleshooting.md)
  
## Quick start

To get started with Borinot, follow the instructions in the following directories:

- [Preflight Checks](resource/preflight.md): This document contains a checklist of preflight checks that must be performed before operating Borinot to ensure its safety and reliability.
- [Optitrack fusion](resource/optitrack.md): This document explains how to fuse data from the Optitrack motion capture system and the PX4 flight controller to obtain accurate position and orientation estimates for Borinot.
- [Borinot Bringups](resource/bringup.md): This document describes the steps required to bring up the various subsystems of Borinot, including the flight controller, manipulator, and sensors.
- [MPC Controller](resource/mpc.md): This document provides an overview of the Model Predictive Controller (MPC) used to control Borinot's hybrid locomotion, and explains how to run simulations and experiments with the controller.

## Citing

If you use Borinot in your research work, please cite the following paper:

> :warning: **Put citing line**
<!-- Put citation -->

[Back to HiDRo Group](../profile/README.md)
