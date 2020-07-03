# vscode_ros2_ws
develop ros2 application in vscode

1.Before run debugging, colcon build should run first.

```
colcon build --packages-select <your_project_name_in_CMakeList>
```

2.Then open 'publisher_member_function.cpp' file in current vscode window.

3.Start debugging.

PS:
1. If want to change debug target, just modify the code in launch.json
    such as
```
"program": "install/ros2_pkgs_/lib/ros2_pkgs_/talker"
```
is responsed for 'publisher_member_function.cpp'
    change into
```
"program": "install/ros2_pkgs_/lib/ros2_pkgs_/listener"
```
is responsed for 'subscriber_member_function.cpp'

2. If could not find rclcpp.so, because the ros-bash-env do not source in terminal when you launch the VSCode use command of 'code'.
   To solve this problem, you should type the command below into terminal before starting VSCode (remember to close the VSCode before operate) :
```
source /opt/ros/dashing/setup.bash
code .
```
