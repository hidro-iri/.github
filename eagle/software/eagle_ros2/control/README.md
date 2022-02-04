# EagleMPC ROS2: Control

This package contains different nodes that allow to interact with the UAM. There are some basic nodes that can be used to test more advanced control architectures.

## 1. Basic (abstract) nodes
The EagleMPC-ROS2 control package has several abstract (or base) classes. These, are common pieces used on a wide variety of control architectures for real robots.
1. We need to get the state estimation of the robot.
2. We need to compute a control (using some fancy algorithm) and send it to the actuators
3. It is good to have a state machine that ensures the good operation of the robot: a proper initialization of data structures and algorithms, a proper ending of algorithms, acceptable handling of unexpected situations, to provide a user interface, etc.

This package contains these pieces implemented as abstract classes. The idea is to build our final control architecture inheriting from the ones that we need. In the following, there is a small explanation of each one of them.

### 1.1 State subscriber & publisher

This node subscribes to different topics containing the state of the robot and publishes the state in one single message.

Even being a base class, it can still be run as a stand-alone node:

1. Enable the PX4 state publication through ROS2. [As described here](../../../procedures/preflight.md).

2. Run the following command:

```
ros2 launch eagle_mpc_2_control state_publisher.py
```

### 1.2 Base controller

This provides the basic functionality to write commands to the UAM actuators (thrust and torque). It is built a an pure virtual class. As such, it must be derived in a separate class so that it can be used.

It has only one pure virtual function called `computeControls()`, which is where the derived classes will call the control algorithms to get the controls for the robot. This is called in its own callback group and, therefore, it is easy to assign an own thread when doing the final node executor. This function is called at fixed rate, specified by a parameter (*to be done, since now it is fixed at 4ms*).

Since it is a pure virtual class, it cannot be launched as a standalone application.

### 1.3 State machine

Generally, to have an operating robot, we need to go through different launch procedures. In these, we make sure that every single subsystem is properly initialized. To ease these procedure we have implemented an abstract class containing a state machine.

<img src="../img/state_machine_interface.png" alt="Node structure" align="center"/>

**FINISH EXPLANATION!**

## 2. Utility (derived) nodes
### 2.1 Control Manager Interface
This is a node with a more advanced functionality. Contains the machinery to run the control based on MPC.

[See here](ctrl_mgr_interface.md) for more info.

### 2.2 Decentralized controller
This is a node to control separately the flying platform and the robotic arm of a UAM.

[See here](decentralized_controller.md) for more info.

### 2.3 Motor test
There are two nodes with the purpose to test the motor in, e.g., the test bench. This is specially useful when our goal is to run an identification algorithm for a motor-propeller set.

#### 2.3.1 Motor test profile

[Back to Eagle MPC - ROS2](../README.md)