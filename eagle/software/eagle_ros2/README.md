# Eagle ROS2

## 1 Installation

### 1.1 Dependencies: libraries

#### 1.1.2 EagleMPC

See the installation instructions [here](../eagle_mpc_lib/README.md#1-installation)

#### 1.1.3 PX4-Autopilot

See the installation instructions [here](../px4/README.md#1-installation)

### 1.2 ROS2 packages (dependencies and Eagle ROS2)

In order to install this ROS2 repository and its ROS2 dependencies, we recommend to use the [vcs tool](https://github.com/dirk-thomas/vcstool) to unify the management of this package and its dependencies.

> :warning: We assume that a ROS2 workspace has already been created. [See here](https://docs.ros.org/en/galactic/Tutorials/Workspace/Creating-A-Workspace.html) for more info about how it is done. Only tested with **ROS Galactic**

### 1.2.1 Using VCS Tool (recommended)
Download the `yaml` file at your ROS2 workspace.
```console
foo@bar:~$ cd <ros2-ws>/src
foo@bar:<ros2-ws>/src$ wget https://raw.githubusercontent.com/hidro-iri/.github/main/eagle/software/eagle_ros2/files/ros2_pkgs.yaml -O ros2_pkgs.yaml
foo@bar:<ros2-ws>/src$ vcs import < ros2_pkgs.yaml
```

### 1.2.2 Manually (alternative to VCS tool)
#### px4_msgs
```console
foo@bar:~$ cd <ros2-ws>/src
foo@bar:<ros2-ws>$ git clone --branch master https://github.com/hidro-iri/px4_msgs.git
```
#### px4_ros_com
```console
foo@bar:~$ cd <ros2-ws>/src
foo@bar:<ros2-ws>$ git clone --branch master https://github.com/hidro-iri/px4_ros_com.git
```

#### eagle_ros2
```console
foo@bar:~$ cd <ros2-ws>/src
foo@bar:<ros2-ws>$ git clone --branch devel https://github.com/hidro-iri/eagle_ros2.git
```

## 2 Build
There are several repositories and steps to take in order to work with the ROS2 packages of this repo.

### 2.1 Building dependencies

#### 2.1.1 C++ EagleMPC

You should be sure that EagleMPC is correctly installed. [See here]([here](../eagle_mpc_lib/README.md#2-build) to know how to do it.

> :information_source: **NOTE**: This library is only used in the [mpc_controller]() node.

#### 2.1.2 PX4
See [here to build the firmware](../px4/README.md#2-build).

### 2.2 Building the ROS2 workspace

> :information_source: **NOTE**: Before compiling, make sure to source the ROS2 `setup.bash` and the one inside your workspace.

You can build the ROS2 workspace with the following command:
```console
foo@bar:~$ cd <ros2-ws>
foo@bar:<ros2-ws>$ colcon build --event-handlers console_direct+ --cmake-args -DCMAKE_EXPORT_COMPILE_COMMANDS=ON -DCMAKE_BUILD_TYPE=Release
```

> :information_source: **NOTE**: In case you have changed the `.yaml`file from `px4_ros_com` to receive or send a different kind of message you should add the flag `--cmake-force-configure` just after `console_direct+` in the building command.

## 3 ROS2 Packages

This repository contains several ROS2-packages to work with *unmanned aerial manipulators* (UAMs) and ROS2. Click on the different links to know more about each of them.

> :information_source: **NOTE**: It has only been tested with [ROS2 Galactic](https://docs.ros.org/en/galactic/index.html).


### 3.1 [EagleMPC - ROS2: Control](control/README.md)
Nodes to deploy control algorithms into the UAM.

### 3.2 [EagleMPC - ROS2: Interfaces](interfaces.md)
Message and service definitions.

### 3.3 [EagleMPC - ROS2: Visualization](visualization.md)
Tools (nodes, RViz configurations, Python scripts) to bring good visualization experience to all other nodes.

### 3.4 [EagleMPC - ROS2: RViz Plugins](rviz_plugins.md)
RViz plugins specifically created to visualize UAM operations.


[Back to Software](../README.md)