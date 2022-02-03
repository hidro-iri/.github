# Build

There are several repositories and steps to take in order to work with the ROS2 packages of this repo.

## 1. Building dependencies

### 1.1 C++ EagleMPC

You should be sure that EagleMPC is correctly installed. [See here](https://github.com/PepMS/eagle_mpc_devs) to know how to do it.

### 1.2 PX4

#### 1.2.1 URTPS Bridge configuration
The packages of this repository use this [PX4 architecture](https://docs.px4.io/master/en/ros/ros2_comm.html) to communicate with the PX4. Not all the messages inside PX4 are broadcasted to ROS2. This is done to avoid saturating the ethernet link between the Pixhawk and the onboard computer. The messages that the Pixhawk and the onboard computer exchange cannot are set at build time by using `.yaml` files.

The `.yaml` files use to select the messages have to be configured are:
- PX4 Autopilot. You should configure [this file](https://github.com/PepMS/PX4-Autopilot/blob/motor_control/msg/tools/urtps_bridge_topics.yaml).
- MicroRTPS Agent: You should configure [this file](https://github.com/PepMS/px4_ros_com/blob/master/templates/urtps_bridge_topics.yaml)

We provide some `.yaml` files with the topics already configured depending on the type of operation that we plan to execute. You only need to copy & paste the content to the files specified above.

The files are places in [`yaml_msgs`](../../yaml_msgs) folder of this repo. Notice that the files with the `px4` prefix should be copied to the `PX4 Autopilot` side, whilst the ones with the `ros2` prefix should be copied to the `px4_ros_com` side.

#### 1.2.2 Build the PX4-Autopilot

There are two options here:
- **Simulation**: 
```console
foo@bar:~$ cd <path-to-px4>
foo@bar:<path-to-px4>$ make px4_sitl_rtps
```     
- **Pixhawk**: 
```console
foo@bar:~$ cd <path-to-px4>
foo@bar:<path-to-px4>$ make px4_fmu-v5x_rtps
```     

## 2. Building the ROS2 workspace

> :information_source: **NOTE**: Before compiling, make sure to source the ROS2 `setup.bash` and the one inside your workspace.

You can build the ROS2 workspace with the following command:
```console
foo@bar:~$ cd <ros2-ws>
foo@bar:<ros2-ws>$ colcon build --event-handlers console_direct+ --cmake-args -DCMAKE_EXPORT_COMPILE_COMMANDS=ON -DCMAKE_BUILD_TYPE=Release
```

> :information_source: **NOTE**: In case you have changed the `.yaml`file from `px4_ros_com` to receive or send a different kind of message you should add the flag `--cmake-force-configure` just after `console_direct+` in the building command.

You are ready now to launch a ROS2 node. For example, you can lau nhc the [decentralized controller](../eagle_mpc_2_control/README.md#22-decentalized-controller).

<!-- ## Generate specific RTPS messages

1. Change the `px4-autopilot/msg/tools/urtps_bridge_topics.yaml` with the messages that have to be published/received.

2. Run `make px4_sitl_rtps` or `make px4_fmuv5x_rtps`

3. Mirror the message changes to the ROS2 side by doing:
    
      3.1 Run python script: `python3 px4-autopilot/msg/tools/uorb_to_ros_urtps_topics.py -i px4-autopilot/msg/tools/urtps_bridge_topics.yaml -o ros2-ws/src/px4_ros_com/templates/urtps_bridge_topics.yaml`

4. Compile ROS2 workspace

## Generate .msg ROS2 files:

```console
python3 /home/pepms/robotics/libraries/px4-autopilot/msg/tools/uorb_to_ros_msgs.py /home/pepms/robotics/libraries/px4-autopilot/msg/ /home/pepms/wsros2/mpc-ws/src/px4_msgs/msg/
``` -->

[Back to Procedures](README.md)