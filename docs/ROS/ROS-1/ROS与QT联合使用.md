# ROS与QT联合使用

### 将 Qt 工程与 ROS1  结合，使得可以通过 rosrun 或 roslaunch 指令运行，需要将 Qt 项目改造为一个 ROS 功能包（package），并正确配置编译系统（CMakeLists.txt）和启动文件。以下是详细的步骤和说明：

##### 1.首先需要确定g++版本，目前，对于qt5来说，需要安装g++和gcc4.8版本，可通过以下命令查看当前版本：

```
g++ --version
gcc --version
```
##### 2.以一个实例演示如何将qt和ROS联合使用，首先创建一个qt工程，构成文件如下，其中libs是库文件.so及其包含的头文件.h

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/XrABsGr3/resources/PnQEInHQajbZ9mIEWGv6JOADbBRQxXsxSd0cfQzzvL0.png)

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/XrABsGr3/resources/V2eCsDpU6VlpuMRv3JeIYXDknkGrlyGpQFWLuYQ5nIE.png)

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/XrABsGr3/resources/RRjsfoTvmnsKFzDzBmlidBqeiHJfH-We2kY92PkmA3E.png)

### 3.创建ROS 创建工作空间​

```
source /opt/ros/noetic/setup.bash
mkdir -p ~/inexbot/src
cd ~/inexbot/src


# 创建一个新的 ROS 功能包，依赖通常包括 qt_build 和 roscpp 等
catkin_create_pkg Qt_test roscpp std_msgs
```
#### 4.将Qt工程迁移到ros中作为ros的一个功能包，注意，需要稍微改变原工程的结构，如下所示：

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/XrABsGr3/resources/mWQ-tJFUUc5G3Su9XLjVYOlbFoJ9worBVrdNLTwOgj0.png)

##### 其中，将原工程中的main.cpp， mainwindow.cpp， mainwindow.cpp，Qt_test.pro文件放到src中，mainwindow.h放到include/Qt_test中:

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/XrABsGr3/resources/GZopou4UiwLhe_MRXIpmsHGTggb0ktDkeHMaLaKbTCY.png)

### 5.修改 CMakeLists.txt 文件

##### 这是最关键的一步。需要修改功能包下的 CMakeLists.txt 文件，使其能够编译 Qt 项目。ROS 使用 CMake，而 Qt 通常使用 qmake，但我们可以通过 CMake 的 find_package 来定位 Qt。以上面的工程为例子，修改后的Cmake文件如下。

```
cmake_minimum_required(VERSION 3.0.2)
project(Qt_test)


# 寻找 Catkin 和 ROS 包
find_package(catkin REQUIRED COMPONENTS
  roscpp
  std_msgs
)


# 设置 C++ 标准
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)


# 寻找 Qt5
set(Qt5_DIR "/usr/lib/x86_64-linux-gnu/cmake/Qt5")
find_package(Qt5 COMPONENTS Core Widgets REQUIRED)


# Catkin 包配置
catkin_package(
  CATKIN_DEPENDS roscpp std_msgs
)


# 包含目录
include_directories(
  include
  /opt/ros/noetic/include
  ${catkin_INCLUDE_DIRS}
  ${Qt5Widgets_INCLUDE_DIRS}
)


# 设置自动处理
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)  # 确保这行存在


# 处理资源文件（如果有）
file(GLOB RESOURCE_FILES "*.qrc")
qt5_add_resources(QT_RESOURCES ${RESOURCE_FILES})


# 设置源文件
set(SRC_FILES
  src/main.cpp
  src/mainwindow.cpp
)


# 设置头文件
set(HEADER_FILES
  include/Qt_test/mainwindow.h
  libs/include/cpp_interface/nrc_api.h
  libs/include/cpp_interface/nrc_interface.h
)


# 添加库路径
link_directories(${PROJECT_SOURCE_DIR}/libs)


# 创建可执行文件
add_executable(${PROJECT_NAME}
  ${SRC_FILES}
  ${HEADER_FILES}
  ${QT_UI_HEADERS}
  ${QT_RESOURCES}
)


# 链接库
target_link_libraries(${PROJECT_NAME}
  ${catkin_LIBRARIES}
  Qt5::Widgets
  Qt5::Core
  nrc_host
)


# 安装
install(TARGETS ${PROJECT_NAME}
  RUNTIME DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)


# 安装库文件（可选）
install(FILES libs/libnrc_host.so
  DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
)


```
##### 说明：

##### qt5_wrap_ui： 自动将 .ui 文件转换为对应的 .h 文件

##### qt5_add_resources： 将 .qrc 资源文件嵌入到可执行文件中

##### 确保你的源文件路径（如 src/main.cpp）是正确的

#### 6.编译功能包

##### 回到工作空间根目录进行编译

```
cd ~/inexbot
catkin_make
```
##### 如果编译成功，应该能在 ~/inexbot/devel/lib/Qt_test/ 目录下找到生成的可执行文件 Qt_test

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/XrABsGr3/resources/p869hcR-Nx3xl0kMTMhQUSvQeQ8QrQqwz8u9JND39rM.png)

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/XrABsGr3/resources/gZCWmtrhS5OgiGZ9rjgKqkCl_PFMupGYmEaTYLs8rAg.png)

### 7.运行文件

```
# 首先确保 roscore 已运行
roscore 
# 然后运行该节点
source devel/setup.bash
rosrun Qt_test Qt_test
```
![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/XrABsGr3/resources/Z-dw7ctDRLuaPsp9_1Y2Z_dy0f59QosZBW8MahwHHwU.png)

### 常见问题与提示

##### 环境变量：确保终端已经 source /opt/ros/noetic/setup.bash 和 source ~/catkin_ws/devel/setup.bash

##### Qt 版本：ROS Noetic 默认基于 Ubuntu 20.04，其 Qt5 版本是 5.12。需要确保项目与该版本兼容

##### 依赖：如果项目依赖其他 ROS 包（如 rviz、tf 等），需要在 catkin_create_pkg 和 find_package(catkin ...) 中添加它们
