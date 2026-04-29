# Moveit2安装

和ROS1不同，ROS2 Humble需要手动配置Moveit2环境，以下是配置流程：

### 1.二进制安装Moveit2

```
sudo apt install ros-humble-moveit
```
若运行不报错，即安装成功。注意，不同版本指令不同，本教程以ROS2 humble为例。

### 2.安装moveit-setup-assistant

```
sudo apt install ros-humble-moveit-setup-assistant
```
### 3.安装所有 MoveIt 相关包

```
sudo apt install ros-humble-moveit-*
```
### 4.启动moveit_setup_assistant

```
 ros2 run moveit_setup_assistant moveit_setup_assistant
```
弹出如下界面表示安装成功！moveit_setup_assistant的使用流程，ROS2和ROS1并无区别，这里不再详细介绍

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/HPxrD8XW/resources/gUAREct65-_izqLJ8wlTOjsSHCrhs7HPhXYZAe1l4-0.png)
