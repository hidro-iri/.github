# Borinot 🚁

Borinot is an open-source Unmanned Aerial Manipulator (UAM) developed by the HiDRo group. It is a torque-controlled robot designed for hybrid flying and contact loco-manipulation. it's a unique platform that can achieve hybrid locomotion tasks combining aerial and ground movements, as well as manipulation tasks that require contact with the environment.

<!-- Quick section of the main software associate with it: eagle_mpc_lib -->

## Table of Contents

- **[Hardware](hardware/README.md)**
  - [Building Instructions](hardware/building_instructions.md)
  - [Electronic Setup](hardware/electronic_setup.md)
- **[Software](software/README.md)**
  - [MPC Controller](software/eagle_ros2/control/mpc_controller.md)
  - [Decentralized Controller](software/eagle_ros2/control/decentralized_controller.md)
- **[Usage](usage/README.md)**
  - [Preflight Checks](usage/preflight.md)
  - [Optitrack Fusion](usage/optitrack.md)
  - [Troubleshooting](usage/troubleshooting.md)
  
## Quick start

To get started with Borinot, follow the instructions in the following directories:

- [Preflight Checks](usage/preflight.md): This document contains a checklist of preflight checks that must be performed before operating Borinot to ensure its safety and reliability.
- [Optitrack fusion](usage/optitrack.md): This document explains how to fuse data from the Optitrack motion capture system and the PX4 flight controller to obtain accurate position and orientation estimates for Borinot.
- [Borinot Bringups](usage/bringup.md): This document describes the steps required to bring up the various subsystems of Borinot, including the flight controller, manipulator, and sensors.
- [MPC Controller](usage/mpc.md): This document provides an overview of the Model Predictive Controller (MPC) used to control Borinot's hybrid locomotion, and explains how to run simulations and experiments with the controller.

## Citing

If you use Borinot in your research work, please cite the following paper:

> :warning: **Put citing line**

[Back to HiDRo Group](../README.md)
