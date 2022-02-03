# Installation
This package has been tested with the [ROS Galactic](https://docs.ros.org/en/galactic/Installation/Ubuntu-Install-Debians.html).
## 1 Dependencies: Libraries

### 1.2 EagleMPC

C++ library. See [installation instructions here](https://github.com/PepMS/eagle_mpc_devs).

### 1.3 PX4-Autopilot

In order to perform direct actuator control we need to modify the [original](https://github.com/PX4/PX4-Autopilot) PX4 repository. You should install [this modified version](https://github.com/PepMS/PX4-Autopilot).

> :warning: we use the `motor_control` branch.

Quick installation commands (the last command it is a script to install all PX4 Autopilot dependencies):
```console
foo@bar:~$ cd <path-to-px4-inst-folder>
foo@bar:<path-to-px4-inst-folder>$ git clone --branch motor_control https://github.com/PepMS/PX4-Autopilot.git eagle-px4
foo@bar:<path-to-px4-inst-folder>$ cd eagle-px4
foo@bar:<path-to-px4-inst-folder/eagle-px4>$  git submodule update --init --recursive
foo@bar:<path-to-px4-inst-folder/eagle-px4>$  ./Tools/setup/ubuntu.sh
```

### 1.4 Oher PX4 dependencies: FastDDS & Fast-RTPS-Gen
To broadcast PX4 messages to ROS2, **FastDDS** & **FastRTPS-Gen** need to be installed.
#### 1.4.1 Fast-DDS
To build **FastDDS**, **Foonathan memory** is required. Both installation procedures are explained at the PX4 wiki.
1. [**Foonathan memory**](https://docs.px4.io/master/en/dev_setup/fast-dds-installation.html#foonathan-memory)
2. [**FastDDS**](https://docs.px4.io/master/en/dev_setup/fast-dds-installation.html#fast-dds)

#### 1.4.2 Fast-RTPS-Gen
To build **FastRTPS-Gen**, we need **Gradle**, which at the same time must be downloaded using **SDKman**. Thus we recommend to follow a reverse order:

1. Install [**SDKman**](https://sdkman.io/install)
2. Install [**Gradle**](https://docs.px4.io/master/en/dev_setup/fast-dds-installation.html#gradle). From a terminal run: `sdk install gradle 6.3`.
3. Follow [these steps](https://docs.px4.io/master/en/dev_setup/fast-dds-installation.html#fast-rtps-gen) to build **Fast-RTPS-Gen**.

## 2 ROS2 packages

In order to install this ROS2 repository and its ROS2 dependencies, we recommend to use the [vcs tool](https://github.com/dirk-thomas/vcstool) to unify the management of this package and its dependencies.

> :warning: We assume that a ROS2 workspace has already been created. [See here](https://docs.ros.org/en/galactic/Tutorials/Workspace/Creating-A-Workspace.html) for more info about how it is done. Only tested with **ROS Galactic**

### 2.1 VCS tool

Download the `yaml` file at your ROS2 workspace.
```console
foo@bar:~$ cd <ros2-ws>/src
foo@bar:<ros2-ws>/src$ wget https://raw.githubusercontent.com/PepMS/eagle_mpc_ros2_dev/control_pkg_restructure/doc/vcs_yamls/ros2_pkgs.yaml?token=GHSAT0AAAAAABHJ2FA7COQAE7IEVLBJEXH2YP2VDPA -O ros2_pkgs.yaml
foo@bar:<ros2-ws>/src$ vcs import < ros2_pkgs.yaml
```

### 2.2 Manually (alternative to VCS tool)
#### px4_msgs
```console
foo@bar:~$ cd <ros2-ws>/src
foo@bar:<ros2-ws>$ git clone --branch master git@github.com:PepMS/px4_msgs.git
```
#### px4_ros_com
```console
foo@bar:~$ cd <ros2-ws>/src
foo@bar:<ros2-ws>$ git clone --branch master git@github.com:PepMS/px4_ros_com.git
```

#### eagle_mpc_ros2
```console
foo@bar:~$ cd <ros2-ws>/src
foo@bar:<ros2-ws>$ git clone --branch devel git@github.com:PepMS/eagle_mpc_ros2_dev.git
```

Now it is time to build the workspace. Follow the instructions [detailed here](build.md).

## 3 Next steps

- ### [Control Manager Interface](../eagle_mpc_2_control/ctrl_mgr_interface.md)
  You can now proceed to launch the main node in this repository to operate a UAM. In case you have not build the workspace, it will walk you through.
- ### [Building instructions](build.md)
  Complete walkthrough to build the ROS2 workspace and all related systems.


[Back to Procedures](README.md)
