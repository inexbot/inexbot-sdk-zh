# C++

# 1. 引言

本开发包旨在为二次开发提供便捷的接口。通过本开发包，用户能够实现对控制器的控制、路径规划、状态监控、工艺参数设置等一系列功能。

# 2. 目标受众

# 3. 开发包使用说明

## 3.1 Windows 环境

### 3.1.1 编译器

- 机械臂开发者：对于希望利用C/C++语言进行编程和调试的机器人开发者来说，本开发包提供了丰富的API和示例代码，方便快速上手。
- 自动化系统集成商：在自动化系统中集成纳博特控制器功能时，本开发包能够简化集成过程，提高开发效率。

### 3.1.2 开发包说明

- MSVC 19.16（Microsoft Visual C++ 2017）以上
- MinGW64 GNU10.3以上

c_interface：存放c接口

cpp_interface：存放c++接口

parameter：存放数据结构定义

win_mingw64_debug_v1.x.x：对应的Windows MinGW 64位 Debug 编译器使用的库

win_mingw64_v1.x.x：对应的Windows MinGW 64位 Release 编译器使用的库

win_msvc64_debug_v1.x.x：对应的Windows MSVC 64位 Debug 编译器使用的库

win_msvc64_v1.x.x：对应的Windows MSVC 64位 Release 编译器使用的库

## 3.2 Linux 环境

### 3.2.1 支持的架构

- 头文件：include
- 动态链接库（dll）

### 3.2.2 编译器

- x86
- aarch64

### 3.2.3 开发包说明

- GNU 4.8 以上
- aarch64-linux-gnu-gcc-9 以上

c_interface：存放c接口

cpp_interface：存放c++接口

parameter：存放数据结构定义

linux_x86_debug_v1.x.x：对应的Linux x86 Debug 编译器使用的库

linux_x86_v1.x.x：对应的Linux x86 Release 编译器使用的库

linux_aarch64_debug_v1.x.x：对应的Linux aarch64 Debug 编译器使用的库

linux_aarch64_v1.x.x：对应的Linux aarch64 Release 编译器使用的库

- 头文件：
- 动态链接库（dll）
