# ROS -2安装

首先准备一个干净、换好源的 ubuntu 20.04 以上的虚拟机（建议清华源)，本教程使用Ubuntu 22.04 ，也适用其他 ROS2 版本。

可以通过以下指令查看查看ubuntu 版本

```
lsb_release -a
```
根据自己的 ubuntu 的版本选择 ROS2 版本， 由于本教程使用 ubuntu 22.04 ，所以对应ROS2版本为 humble

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/Pyt99CAr/resources/tuJFQVJcgkmSYMZPARGAyPzuujxQHHrtpCIfXJk_Pcg.png)

这里只列出了 Foxy 之后的Ubuntu版本支持，更多版本与细节可以看ROS官方说明，下面给出两种配置ROS2的方法。

### 方法一：使用官方教程

#### 1. ROS2安装前的基本环境准备

##### （1）设置 locale，确保你的本地语言支持 UTF-8

```
sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8
```
##### （2）设置源

```
sudo apt install software-properties-common
sudo add-apt-repository universe
```
##### （3）添加 ROS 2 GPG key

```
sudo apt update && sudo apt install curl gnupg2 -y
sudo curl -sSL https://gitee.com/tyx6/rosdistro/raw/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg
```
（4）为软件源添加 ROS2 repository（二选一）

官方源

```
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
```
清华源

```
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] https://mirrors.tuna.tsinghua.edu.cn/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
```
#### 2.ROS2的安装

##### （1） 更新系统

在安装ROS2前，先执行系统更新指令：

```
sudo apt update
sudo apt upgrade
```
##### （2）安装ROS2

这里选择安装 ros-foxy-desktop版本，如下指令：

```
sudo apt install ros-humble-desktop
```
##### (3) ROS2环境配置

```
echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc 
source ~/.bashrc  #使环境生效
```
#### 3.ROS2的测试

##### （1）底层通信系统的测试

在一个终端发送消息广播指令：

```
ros2 run demo_nodes_cpp talker
```
若正常，将显示以下信息：

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/Pyt99CAr/resources/rIF2v7CeW-ZM3_x-H6vEBrUa-lQAguO5Ukdv4_j2JoY.png)

在另外一个终端发送消息订阅接收指令：

```
ros2 run demo_nodes_py listener
```
正常将显示以下信息（后面数字不一定相同）：

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/Pyt99CAr/resources/nuagFKLwKLLyw3Iupu506tlmJO11-nbxb2HHSHIdd2k.png)

如果“Hello World”字符串在两个终端中正常传输，说明通信系统没有问题。

##### （2）小海龟的测试仿真示例

再来试一试ROS中的经典示例——小海龟仿真器。启动两个终端，分别运行如下指令：

启动海龟仿真器

```
ros2 run turtlesim turtlesim_node
```
启动键盘控制

```
ros2 run turtlesim turtle_teleop_key
```
效果如下图所示：

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/Pyt99CAr/resources/8yORjE7UUWq0I4JpV12k8vn8Dpofw6yLPRsFX1Q9j-A.png)

#### 4. 配置rosdep

在使用许多 ROS 工具之前，需要初始化 rosdep，有些功能包源码编译需要rosdep 来安装这些系统依赖项

rosdep 请求的是国外的服务器，所以会被墙。有些是通过代理的方式，但这个不稳定。它需要的文件都官方都放在 github 上的，那么我们可以改url地址即可。

##### （1）安装依赖

```
sudo apt install python3-rosdep
```
（2）自动修改

使用脚本

```
wget  https://gitee.com/tyx6/mytools/raw/main/ros/Mrosdep.py 
sudo python3 Mrosdep.py
```
注：此脚本在 rosdistro 目录下，是为了方便编写的，如果脚本执行失败可以手动修改，方法如下：

修改4个文件，都是将地址 https://raw.githubusercontent.com/… 改为https://gitee.com/.......

```
sudo gedit /usr/lib/python3/dist-packages/rosdep2/sources_list.py
# 大概在64行


sudo gedit /usr/lib/python3/dist-packages/rosdistro/__init__.py
# 大概在68行


sudo gedit /usr/lib/python3/dist-packages/rosdep2/gbpdistro_support.py
# 大概在34行
 
sudo gedit /usr/lib/python3/dist-packages/rosdep2/rep3.py
# 大概在36行
```
##### (3)开始配置

```
sudo rosdep init
rosdep update
```
注意：若总是配置失败，则可以尝试方法二一键配置

### 方法二：一键安装

使用小鱼的一键安装系列

```
wget  http://fishros.com/install -O fishros && . fishros 
```
使用该方法可以一键安装ROS2,一键配置rosdep和环境

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/Pyt99CAr/resources/hSc6jhXvy6T39KCzMmYJXZHsPfa_7bxWG-Sh1xUAbsg.png)
