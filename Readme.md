# Borot

[![fusion 360](https://img.shields.io/badge/fusion%20360-FF6F00?style=for-the-badge&logo=autodesk&logoColor=white)](https://www.autodesk.com/campaigns/education/fusion-360)	[![motor](https://img.shields.io/badge/motor-lewansoul_lx16a-brightgreen.svg?style=flat-square)](https://github.com/ethanlipson/PyLX-16A)

A self designed robot powered by Raspberry Pi. Used Fusion 360 to design.

The repository contains:

	1. All the 3D printed parts that make up a robot.
 	2. Controling circuit
 	3. Codes to show movement.

Video presentation: https://www.youtube.com/watch?v=awiGGOEJ-E4&ab_channel=BoYuan

## Table of Contents

* [Appearance](#appearance)
* [3D Printed Parts](#3D Printed Parts)
* [Robot Assembly](#Robot Assembly)
* [Controling Circuit](#Controling Circuit)
* [Code](#Code)

## Appearance

Both [.stl](https://github.com/boyuan99/Borot/blob/main/Assembled/rendering%20v7.stl) and [f3d](https://github.com/boyuan99/Borot/blob/main/Assembled/rendering%20v7.f3d) files are uploaded in this repository.

The fully assembled robot shows as following: 

<img src="./img/Assembled_robot.png" alt="img" style="zoom:100%;" />

Body:

<img src="./img/Body.png" alt="img" style="zoom:100%;" />

Leg:

<img src="./img/Leg.png" alt="img" style="zoom:100%;" >

## 3D Printed Parts

Leg:

* [[Connector Thigh Shank1]](https://github.com/boyuan99/Borot/blob/main/Parts/connector_thigh_shank1.stl)

* [[Connector Thigh Shank2]](https://github.com/boyuan99/Borot/blob/main/Parts/connector_thigh_shank2.stl)

* [[Left Shank1]](https://github.com/boyuan99/Borot/blob/main/Parts/shank_left1.stl)
* [[Left Shank2]](https://github.com/boyuan99/Borot/blob/main/Parts/shank_left2.stl)
* [[Right Shank1]](https://github.com/boyuan99/Borot/blob/main/Parts/shank_right1.stl)
* [[Right Shank2]](https://github.com/boyuan99/Borot/blob/main/Parts/shank_right2.stl)
* [[Shank Supporter]](https://github.com/boyuan99/Borot/blob/main/Parts/shank_supporter.stl)
* [[Left Thigh1]](https://github.com/boyuan99/Borot/blob/main/Parts/thigh_left1.stl)
* [[Left Thigh2]](https://github.com/boyuan99/Borot/blob/main/Parts/thigh_left2.stl)
* [[Right Thigh1]]([[Left Thigh1]](https://github.com/boyuan99/Borot/blob/main/Parts/thigh_left1.stl))
* [[Right Thigh2]]([[Left Thigh1]](https://github.com/boyuan99/Borot/blob/main/Parts/thigh_left2.stl))

Foot:

* [[Foot Bottom]](https://github.com/boyuan99/Borot/blob/main/Parts/foot_long.stl)
* [[Foot Top]](https://github.com/boyuan99/Borot/blob/main/Parts/foot_top.stl)

Body:

* [[Body Hat]](https://github.com/boyuan99/Borot/blob/main/Parts/body_hat.stl)
* [[Body Left]](https://github.com/boyuan99/Borot/blob/main/Parts/body_left.stl)
* [[Body Right]](https://github.com/boyuan99/Borot/blob/main/Parts/body_right.stl)

Knee:

* [[Connector Thigh Left1]](https://github.com/boyuan99/Borot/blob/main/Parts/connector_thigh_left1.stl)
* [[Connector Thigh Left2]](https://github.com/boyuan99/Borot/blob/main/Parts/connector_thigh_left2.stl)
* [[Connector Thigh Right1]](https://github.com/boyuan99/Borot/blob/main/Parts/connector_thigh_right1.stl)
* [[Connector Thigh Right2]](https://github.com/boyuan99/Borot/blob/main/Parts/connector_thigh_right2.stl)

Extra:

1. This part is responsible for keeping every parts together.
   * [[Insert]](https://github.com/boyuan99/Borot/blob/main/Parts/insert.stl)
2. These parts are responsible for mounting the motor to the shank, notice that they are **not** the same.
   * [[Motor Shank1]](https://github.com/boyuan99/Borot/blob/main/Parts/motorshank1.stl)
   * [[Motor Shank2]](https://github.com/boyuan99/Borot/blob/main/Parts/motorshank2.stl)
3. These parts are responsible for mounting the motor to the thigh, notice that they are **not** the same.
   * [[Motor Thigh1]](https://github.com/boyuan99/Borot/blob/main/Parts/motorthigh1.stl)
   * [[Motor Thigh2]](https://github.com/boyuan99/Borot/blob/main/Parts/motorthigh2.stl)

## Robot Assembly

8 LewanSoul LX-16A servos are needed for Borot. 2 on the body, 3 on each leg, needs some screws too(M2 screws).

As shown in STL files, many parts are left with square holes, use  [Insert](https://github.com/boyuan99/Borot/blob/main/Parts/insert.stl) to put those parts together. You don't have to fill every holes with inserts, most of the holes are left as spares in case there are inserts break.

Please use fully assembled stl file as reference to install your own robot.

## Controling Circuit

The whole circuit will be placed in the body, space is left on both sides for the cables to connect the motors.

![image-20220709194333119](./img/Circuit.png)

## Code

* Run `movement_show.py` to let the robot walk

* Run `reset_robot.py` to recover the standing up position.

A modern [Python library](https://github.com/ethanlipson/PyLX-16A) for controlling HiWonder's (previously LewanSoul's) LX-16A servos is required

Run the following command:

​	`pip install pylx16a`

Notice:

1. If you do not want to use the GUI to adjust the motors, then python 3.10 is not necessary. 
2. Must adjust the angles of the motors before you assemble the robot, or you can break the parts and have to print again and again... (happened on me)



