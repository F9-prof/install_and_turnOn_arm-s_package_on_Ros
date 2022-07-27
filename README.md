# install_and_turnOn_arm-s_package_on_Ros
## First step: Installing the package *arduino_robot_arm*

- Add the “arduino_robot_arm” package to “src” folder

```
$ cd ~/catkin_ws/src
$ sudo apt install git
$ git clone https://github.com/smart-methods/arduino_robot_arm 
```

- Install all the dependencies of noetic Ros virsion


```
$ cd ~/catkin_ws
$ rosdep install --from-paths src --ignore-src -r -y
$ sudo apt-get install ros-noetic-moveit
$ sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
$ sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
$ sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
```


## Second step: power on the package *arduino_robot_arm*

- Compile the package


```
$ catkin_make
```
![Screenshot_1](https://user-images.githubusercontent.com/108638709/181179203-0e1ab12a-8bb4-4619-9461-53fec8dfeebd.png)

- Controlling the motors
```
$ roslaunch robot_arm_pkg check_motors.launch
```


![Screenshot_2](https://user-images.githubusercontent.com/108638709/181180113-191f3934-1104-440e-a140-f62512eb0c26.png)




  
