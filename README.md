
# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step 1:
Use from robomaster import robot

Step 2:
Choose the x,y,z - axis movement distance(meters).

Step 3:
Give ep_chasis.move to move straight

Step 4:
Give ep_chasis.drive to get circular motion.

Step 5:
Give ep_chasis.move to move straight

Step 6:
Give ep_chasis.drive to get circular motion.

## Program
## Program
```
from robomaster import robot
import time

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis

    '''
    x = x-axis movement distance,( meters) [-5,5]
    y = y-axis movement distance,( meters) [-5,5]
    z = rotation about z axis ( degree)[-180,180]
    xy_speed = xy axis movement speed,( unit meter/second) [0.5,2]
    '''
    ep_chassis.move(x=1, y=0, z=0, xy_speed=0.75).wait_for_completed()

    ep_chassis.move(x=0, y=0, z=-135, xy_speed=0.75).wait_for_completed()

    ep_chassis.move(x=1, y=0, z=0, xy_speed=0.75).wait_for_completed()

    ep_chassis.move(x=0, y=0, z=135, xy_speed=0.75).wait_for_completed()

    ep_chassis.move(x=1, y=0, z=0, xy_speed=0.75).wait_for_completed()

    ep_chassis.move(x=0, y=0, z=90, xy_speed=0.75).wait_for_completed()

    ep_chassis.move(x=1, y=0, z=0, xy_speed=0.75).wait_for_completed()

    ep_chassis.move(x=0, y=0, z=-150, xy_speed=0.75).wait_for_completed()

    ep_chassis.move(x=1, y=0, z=0, xy_speed=0.75).wait_for_completed()

    ep_chassis.move(x=0, y=0, z=150, xy_speed=0.75).wait_for_completed()

    ep_chassis.move(x=1, y=0, z=0, xy_speed=0.65).wait_for_completed()
    ep_chassis.drive_speed(x=0.2,y=0,z=20)
    time.sleep(15)



    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

## Insert image here:
![final](https://user-images.githubusercontent.com/94187572/154799347-346285e3-59f3-4b91-8060-d3526d11deda.jpeg)
![in](https://user-images.githubusercontent.com/94187572/154799350-b9e76ba2-e3d2-4061-ab49-457ef080e19e.jpeg)



## MobileRobot Movement Video:

https://youtu.be/ttkfd_p5uvk

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
