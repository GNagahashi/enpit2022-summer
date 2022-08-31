# enPiT Summer School 2022

To begin with, check this: https://github.com/hisazumi/gnc

## How to use

1, Clone this repository.
```sh
# e.g.
cd ~/catkin_ws/src
git clone https://github.com/GNagahashi/enpit2022_summer.git
```

2, Rename this repository in the local from `enpit2022_summer` to `gnc`.
```sh
# e.g.
cd ~/catkin_ws/src
mv enpit2022_summer/ gnc
```

3, Build on BridgePoint. (If you needed, run `catkin clean` and `catkin build` on terminal.)  

4, Run in Terminal.  
```sh
cd ~/Desktop
./simulator.sh
# New tab, after 'cd ~/Desktop'
./sitl.sh
# New window, after 'source ~/.bashrc && source <your work space>/devel/setup.bash'
roscore
# New tab
roslaunch iq_sim apm.launch
# New tab
rosrun gnc ctrl
```

5, Let's control a drone.  

If you want to control a drone, please send a message to `/gnc_drone/cmd` topic(Use `std_msgs/String`)  
Message variation: start, halt, grab, forward, backward, left, right  

OR, use this package: https://github.com/GNagahashi/enpit2022_summer_drone_ctrl.git  

