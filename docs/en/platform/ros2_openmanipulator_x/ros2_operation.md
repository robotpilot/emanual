---
layout: archive
lang: en
ref: ros2_openmanipulator_x_ros_operation
read_time: true
share: true
author_profile: false
permalink: /docs/en/platform/ros2_openmanipulator_x/ros_operation/
sidebar:
  title: "[ROS2] OpenMANIPULATOR-X"
  nav: "ros2_openmanipulator_x"
---

<div style="counter-reset: h1 6"></div>

# [[ROS2] Operation](#ros-operation)

<iframe width="560" height="315" src="https://www.youtube.com/embed/iZuZZk27Y84" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## [GUI Program](#gui-program)

{% capture coming_soon_01 %}
`GUI Program` for `ROS2 Dashing Diademata` will be released soon!  
{% endcapture %}
<div class="notice">{{ coming_soon_01 | markdownify }}</div>

## [Teleoperation](#teleoperation)
{% capture notice_01 %}
**NOTE**:
- This instruction has been tested on `Ubuntu 18.04` and `ROS2 Dashing Diademata`.
- This instruction is supposed to be run on PC with ROS packages installed in. Please run the instruction below on your PC ROS packages installed in.
- Make sure to run [OpenMANIPULATOR controller](/docs/en/platform/ros2_openmanipulator_x/ros_controller_package/#launch-controller) instructions before running the instructions below.
{% endcapture %}
<div class="notice--info">{{ notice_01 | markdownify }}</div>

<iframe width="560" height="315" src="https://www.youtube.com/embed/FGHBMJByJ7k" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### [Keyboard](#keyboard)

**TIP**: Terminal can be found with the Ubuntu search icon on the top left corner of the screen. Shortcut key for Terminal is `Ctrl`+`Alt`+`t`.
{: .notice--success}

  Launch `open_manipulator_x_teleop_keyboard` node for simple teleoperation test using the keyboard.

  ``` bash
  $ ros2 run open_manipulator_x_teleop open_manipulator_x_teleop_keyboard
  ```
  If the node is successfully launched, the following instruction will appeare in the terminal window.

  ```
  ---------------------------
  Control Your OpenMANIPULATOR-X!
  ---------------------------
  w : increase x axis in task space
  s : decrease x axis in task space
  a : increase y axis in task space
  d : decrease y axis in task space
  z : increase z axis in task space
  x : decrease z axis in task space

  y : increase joint 1 angle
  h : decrease joint 1 angle
  u : increase joint 2 angle
  j : decrease joint 2 angle
  i : increase joint 3 angle
  k : decrease joint 3 angle
  o : increase joint 4 angle
  l : decrease joint 4 angle

  g : gripper open
  f : gripper close

  1 : init pose
  2 : home pose

  q to quit
  ---------------------------
  Present Joint Angle J1: 0.000 J2: 0.000 J3: 0.000 J4: 0.000
  Present Kinematics Position X: 0.000 Y: 0.000 Z: 0.000
  ---------------------------
  ```

### [PS4 Joystick](#ps4-joystick)

Install packages for teleoperation using PS4 joystick.

``` bash
$ sudo apt install ros-dashing-joy
$ sudo pip install ds4drv
```

Connect PS4 joystick to the PC via Bluetooth using the following command

``` bash
$ sudo ds4drv
```

Enter pairing mode with PS4 by pressing and holding Playstation button + share button for 10 sec. If the light on PS4 turns blue, enter the following commands in terminal and control OpenMANIPULATOR-X.

``` bash
$ ros2 run joy joy_node
$ ros2 run open_manipulator_x_teleop open_manipulator_x_teleop_joystick
```

### [XBOX 360 Joystick](#xbox-360-joystick)

Install packages for teleoperation using XBOX 360 joystick.

``` bash
$ sudo apt-get install xboxdrv ros-dashing-joy
```
Connect XBOX 360 joystick to the PC with Wireless Adapter or USB cable, and launch teleoperation packages for XBOX 360 joystick.

``` bash
$ sudo xboxdrv --silent
$ ros2 run joy joy_node
$ ros2 run open_manipulator_x_teleop open_manipulator_x_teleop_joystick
```

## [MoveIt!](#moveit)

{% capture coming_soon_01 %}
`Move it` for `ROS2 Dashing Diademata` will be released soon!  
{% endcapture %}
<div class="notice">{{ coming_soon_01 | markdownify }}</div>



[OpenCR]: /docs/en/parts/controller/opencr10/
[OpenCR Manual]: /docs/en/parts/controller/opencr10/
[rc100]: /docs/en/parts/communication/rc-100/
[bt410]: /docs/en/parts/communication/bt-410/

[open_manipulator_msgs/GetJointPosition]: /docs/en/popup/open_manipulator_msgs_GetJointPosition/
[open_manipulator_msgs/GetKinematicsPose]: /docs/en/popup/open_manipulator_msgs_GetKinematicsPose/
[open_manipulator_msgs/SetJointPosition]: /docs/en/popup/open_manipulator_msgs_SetJointPosition/
[open_manipulator_msgs/SetKinematicsPose]: /docs/en/popup/open_manipulator_msgs_SetKinematicsPose/
[open_manipulator_msgs/SetActuatorState]: /docs/en/popup/open_manipulator_msgs_SetActuatorState/
[open_manipulator_msgs/SetDrawingTrajectory]: /docs/en/popup/open_manipulator_msgs_SetDrawingTrajectory/

[sensor_msgs/JointState]: /docs/en/popup/sensor_msgs_JointState_msg/
[open_manipulator_msgs/KinematicsPose]: /docs/en/popup/open_manipulator_msgs_KinematicsPose/
[open_manipulator_msgs/OpenManipulatorState]: /docs/en/popup/open_manipulator_msgs_OpenManipulatorState/
[std_msgs::String]: /docs/en/popup/std_msgs_string/

[task space]: /docs/en/popup/open_manipulator_coordinates/
[joint space]: /docs/en/popup/open_manipulator_coordinates/