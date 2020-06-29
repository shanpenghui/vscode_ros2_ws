# vscode_ros2_ws
develop ros2 application in vscode

1.Before run debugging, colcon build should run first.

    ```
    colcon build --packages-select ros2_pkgs_
    ```

2.Then open 'publisher_member_function.cpp' file in current vscode window.

3.Start debugging.

PS:
If want to change debug target, just modify the code in launch.json
    such as
    ```
    "program": "install/ros2_pkgs_/lib/ros2_pkgs_/talker"
    ```
    is responsed for 'publisher_member_function.cpp'
    change into
    ```
    "program": "install/ros2_pkgs_/lib/ros2_pkgs_/talker"
    ```
    is responsed for 'subscriber_member_function.cpp'