# ROS-2

### 简介

ROS 2（Robot Operating System 2） 是新一代机器人操作系统，在继承ROS 1核心思想的基础上，针对现代机器人需求进行了全面升级。它专注于实时性、分布式计算、跨平台支持和生产级应用，广泛应用于自动驾驶、工业机器人、无人机和智能服务机器人等领域。

#### ROS 2 核心特性

#### ROS 2 版本与生态

当前主流版本包括 Humble Hawksbill（LTS）、Iron Irwini 和最新 Rolling 发行版，社区提供丰富的功能包（如Navigation2、MoveIt 2），推动机器人技术快速发展。

ROS 2 代表了机器人软件的未来方向，适用于从学术研究到商业落地的全场景需求。

- 实时性与可靠性：采用DDS（数据分发服务）作为底层通信机制，支持QoS（服务质量）配置，适应高实时性需求。
- 多平台支持：兼容 Linux、Windows、macOS 和 RTOS（如FreeRTOS），并支持嵌入式设备（如Raspberry Pi、NVIDIA Jetson）。
- 分布式架构：优化多机器人协同，支持微服务（MicroROS），适用于大规模机器人集群。
- 现代化设计：改进的API、更安全的通信（加密支持）和更灵活的构建系统（基于ament和colcon）。
- 仿真与开发工具：集成 Gazebo、Rviz2、rqt 等工具，并支持ROS 1 桥接，便于迁移原有项目。
