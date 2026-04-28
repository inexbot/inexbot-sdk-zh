# 二次开发API（码垛工艺）

# 概述

本章旨在帮助用户对于二次开发的库和函数接口的调用，参数的设置等。

# 版本信息

| 二次开发版本 | 公司 |
| 1.0.0 | INEXBOT |

# 版本迭代

| 版本 | 修改日期 | 修改人 | 描述 |
| 1.0.0 | 20260402 | Shanyufeng | 初始版本 |

# 函数库 API说明

此章节用于对函数库的API的功能说明及其使用方法介绍。

## NexIghLib API 函数列表

| 函数名称 | 函数功能 |
| NRC_Pallet_SetUsePalletType | 设置使用简易码垛还是完整码垛。 |
| NRC_Pallet_GetUsePalletType | 获取使用的是使用简易码垛还是完整码垛。 |
| NRC_Pallet_SetGripperParm | 设置码垛抓手数据。 |
| NRC_Pallet_GetGripperParm | 获取码垛抓手数据。 |
| NRC_Pallet_SetSimplePosParm | 设置简易码垛位置数据。 |
| NRC_Pallet_GetSimplePosParm | 获取简易码垛位置数据。 |
| NRC_Pallet_SetSimpleNumParm | 设置简易码垛个数数据。 |
| NRC_Pallet_GetSimpleNumParm | 获取简易码垛个数数据。 |
| NRC_Pallet_ClearCurrentStatus | 清除码垛当前状态。 |
| NRC_Pallet_SetPalletedWpNum | 设置码垛已码个数。 |
| NRC_Pallet_GetPalletedWpNum | 获取码垛已码个数。 |

### NRC_Pallet_SetUsePalletType

| 函数原型 | int NRC_Pallet_SetUsePalletType(int id, int type); |
| 功能描述 | 设置使用简易码垛还是完整码垛。 |
| 参数说明 | 输入参数：
    id  码垛工艺的工艺号，参数范围：1 <= id <= 99
    type  使用的码垛类型  0-简易码垛  1-完整码垛 |
| 返回值 | 0：函数调用成功返回
-101：无效的输入参数返回
-102：目标对象不存在，一般出现在系统初始化未完成时，调用其他函数时可能返回该值返回
-103：目标对象当前处于不可操作状态返回 |
| 备注说明 | 无 |

### NRC_Pallet_GetUsePalletType

| 函数原型 | int NRC_Pallet_GetUsePalletType(int id); |
| 功能描述 | 获取使用的是使用简易码垛还是完整码垛。 |
| 参数说明 | 输入参数：
    id  码垛工艺的工艺号，参数范围：1 <= id <= 99 |
| 返回值 | 使用的码垛类型： 0-简易码垛 1-完整码垛 |
| 备注说明 | 无 |

### NRC_Pallet_SetGripperParm

| 函数原型 | int NRC_Pallet_SetGripperParm(int id, int gripperSum, int gripper[4]); |
| 功能描述 | 设置码垛抓手数据。 |
| 参数说明 | 输入参数：
    id  码垛工艺的工艺号，参数范围：1 <= id <= 99
    gripperSum 可用抓手总数，参数范围：1 <= gripperSum <= 4
    gripper  每个抓手所绑定的工具坐标号，1 <= gripper[i] <= 9 |
| 返回值 | 0：函数调用成功返回
-101：无效的输入参数返回
-102：目标对象不存在，一般出现在系统初始化未完成时，调用其他函数时可能返回该值返回
-103：目标对象当前处于不可操作状态返回 |
| 备注说明 | 无 |

### NRC_Pallet_GetGripperParm

| 函数原型 | int NRC_Pallet_GetGripperParm((int id, int &gripperSum, int &gripper[4]); |
| 功能描述 | 获取码垛抓手数据。 |
| 参数说明 | 输入参数：
    id  码垛工艺的工艺号，参数范围：1 <= id <= 99
输出参数：
    gripperSum 获取到的可用抓手总数
    gripper  获取到的每个抓手所绑定的工具坐标号 |
| 返回值 | 0：函数调用成功返回
-101：无效的输入参数返回
-102：目标对象不存在，一般出现在系统初始化未完成时，调用其他函数时可能返回该值返回
-103：目标对象当前处于不可操作状态返回 |
| 备注说明 | 无 |

### NRC_Pallet_SetSimplePosParm

| 函数原型 | int NRC_Pallet_SetSimplePosParm(int id, int posType, NRC_Position pos); |
| 功能描述 | 设置简易码垛位置数据。 |
| 参数说明 | 输入参数：
    id  码垛工艺的工艺号，参数范围：1 <= id <= 99
    posType 简易码垛的位置类型：  - 0 起始工件点  - 1 列末端  - 2 行末端  - 3 高末端  - 4 起始辅助点  - 5 起始入口点
    pos 点位数据 |
| 返回值 | 0：函数调用成功返回
-101：无效的输入参数返回
-102：目标对象不存在，一般出现在系统初始化未完成时，调用其他函数时可能返回该值返回
-103：目标对象当前处于不可操作状态返回 |
| 备注说明 | 无 |

### NRC_Pallet_GetSimplePosParm

| 函数原型 | int NRC_Pallet_GetSimplePosParm(int id, int posType, NRC_Position& pos); |
| 功能描述 | 获取简易码垛位置数据。 |
| 参数说明 | 输入参数：
    id  码垛工艺的工艺号，参数范围：1 <= id <= 99
    posType 简易码垛的位置类型：  - 0 起始工件点  - 1 列末端  - 2 行末端  - 3 高末端  - 4 起始辅助点  - 5 起始入口点
输出参数：
    pos 点位数据 |
| 返回值 | 0：函数调用成功返回
-101：无效的输入参数返回
-102：目标对象不存在，一般出现在系统初始化未完成时，调用其他函数时可能返回该值返回
-103：目标对象当前处于不可操作状态返回 |
| 备注说明 | 无 |

### NRC_Pallet_SetSimpleNumParm

| 函数原型 | int NRC_Pallet_SetSimpleNumParm(int id, int numX, int numY, int numZ); |
| 功能描述 | 设置简易码垛个数数据。 |
| 参数说明 | 输入参数：
    id  码垛工艺的工艺号，参数范围：1 <= id <= 99
    numX 简易码垛在其托盘X方向(对应用户坐标的X方向)上的工件数目，即行数
    numY 简易码垛在其托盘Y方向(对应用户坐标的Y方向)上的工件数目，即列数
    numZ 简易码垛在其托盘Z方向(对应用户坐标的Z方向)上的工件数目，即层数 |
| 返回值 | 0：函数调用成功返回
-101：无效的输入参数返回
-102：目标对象不存在，一般出现在系统初始化未完成时，调用其他函数时可能返回该值返回
-103：目标对象当前处于不可操作状态返回 |
| 备注说明 | 无 |

### NRC_Pallet_GetSimpleNumParm

| 函数原型 | int NRC_Pallet_GetSimpleNumParm(int id, int& numX, int& numY, int& numZ); |
| 功能描述 | 获取简易码垛个数数据。 |
| 参数说明 | 输入参数：
    id  码垛工艺的工艺号，参数范围：1 <= id <= 99
输出参数：
    numX 简易码垛在其托盘X方向(对应用户坐标的X方向)上的工件数目，即行数
    numY 简易码垛在其托盘Y方向(对应用户坐标的Y方向)上的工件数目，即列数
    numZ 简易码垛在其托盘Z方向(对应用户坐标的Z方向)上的工件数目，即层数 |
| 返回值 | 0：函数调用成功返回
-101：无效的输入参数返回
-102：目标对象不存在，一般出现在系统初始化未完成时，调用其他函数时可能返回该值返回
-103：目标对象当前处于不可操作状态返回 |
| 备注说明 | 无 |

### NRC_Pallet_ClearCurrentStatus

| 函数原型 | int NRC_Pallet_ClearCurrentStatus(int id); |
| 功能描述 | 清除码垛当前状态。 |
| 参数说明 | 输入参数：
    id  码垛工艺的工艺号，参数范围：1 <= id <= 99 |
| 返回值 | 0：函数调用成功返回
-101：无效的输入参数返回
-102：目标对象不存在，一般出现在系统初始化未完成时，调用其他函数时可能返回该值返回
-103：目标对象当前处于不可操作状态返回 |
| 备注说明 | 无 |

### NRC_Pallet_SetPalletedWpNum

| 函数原型 | int NRC_Pallet_SetPalletedWpNum(int id, int layerNum, int layerPalletedWpNum); |
| 功能描述 | 设置码垛已码个数。 |
| 参数说明 | 输入参数：
    id  码垛工艺的工艺号，参数范围：1 <= id <= 99
    layerNum 要修改的已码层数
    layerPalletedWpNum 要修改的层已码工件数 |
| 返回值 | 0：函数调用成功返回
-101：无效的输入参数返回
-102：目标对象不存在，一般出现在系统初始化未完成时，调用其他函数时可能返回该值返回
-103：目标对象当前处于不可操作状态返回 |
| 备注说明 | 无 |

### NRC_Pallet_GetPalletedWpNum

| 函数原型 | int NRC_Pallet_GetPalletedWpNum(int id, int& curPalletedWpSum, int& curLayerNum, int& curLayerPalletedWpNum, int& totalWpNum, int& totalLayerNum, int& curLayerWpSum); |
| 功能描述 | 获取码垛已码个数。 |
| 参数说明 | 输入参数：
    id  码垛工艺的工艺号，参数范围：1 <= id <= 99
输出参数：
    curPalletedWpSum 当前已码工件数
    curLayerNum 当前已码层数
    curLayerPalletedWpNum 当前层的已码工件数
    totalWpNum 垛堆工件总数
    totalLayerNum 垛堆总层数
    curLayerWpSum 当前层的工件总数 |
| 返回值 | 0：函数调用成功返回
-101：无效的输入参数返回
-102：目标对象不存在，一般出现在系统初始化未完成时，调用其他函数时可能返回该值返回
-103：目标对象当前处于不可操作状态返回 |
| 备注说明 | 对于用作返回值的6个参数，当其值为-1时，表示个数未知 |
