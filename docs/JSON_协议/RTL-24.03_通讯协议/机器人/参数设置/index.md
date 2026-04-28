# 参数设置

### 机器人类型

- 说明：

- 查询当前机器人类型

- 上位机查询当前机器人类型

```
{}
```
- 命令字：0x2000

- 控制器回复上位机当前机器人类型

- 命令字：0x2001
- "type":1

```
{
  "type":0;
}
```
### 机器人类型及映射

- 表示要操作的机器人编号；int类型，取值范围[0,35]
- 0：未选择机器人类型；
- 1：六轴串联多关节；
- 2：六轴协作；
- 3：六轴喷涂机器人；
- 4：六轴异型二；
- 5：五轴机器人；
- 6：四轴SCARA机器人；
- 7：四轴SCARA异型一机器人；
- 8：四轴连杆码垛机器人；
- 9：四轴码垛丝杆机器人；
- 10：四轴机器人；
- 11：四轴直角机器人；
- 12：四轴极坐标异形机器人；
- 13：三轴SCARA机器人；
- 14：三轴直角机器人；
- 15：三轴异形一机器人；
- 16：二轴SCARA机器人；
- 17：七轴通用机器人；
- 18：一轴机器人；
- 19：五轴龙门焊接机器人；
- 20：delta机器人(四轴并联机器人)；
- 21：酒槽机型；
- 22：五轴龙门焊接机器人类型2；
- 23：四轴直角异型一机器人；
- 24：六轴龙门焊接机器人；
- 25：五轴混动机器人；
- 26：四轴SCARA异型2；
- 27：六轴异型三；
- 28：三轴SCARA异型1；
- 29：delta2D并联机器人模型；
- 30：五轴龙门焊接机器人类型3；
- 31：三轴串联异形一；
- 32：五轴协作机器人；
- 33：四轴SCARA异型三机器人；
- 34：六轴串联-CBBARA；
- 35：高格立柱旋转四轴

- 说明：

- 全部机器人类型及伺服映射的查询与设置

- 上位机设置机器人类型及映射

- 命令字：0x2002

- "sum":1

- 表示机器人数目；int类型，取值范围[1,4]

- "robot":

- 机器人参数列表，包含有机器人类型、伺服映射、注释
- 列表长度为机器人数目
- "robotType": "R_GENERAL_6S"

- 表示机器人类型；string类型
- "R_NULL"：未选择机器人类型；
- "R_GENERAL_6S"：六轴串联多关节；
- "R_GENERAL_6S_1"：六轴协作；
- "R_SIXAXIS_SPRAY_BBR"：六轴喷涂机器人；
- "R_GENERAL_6S_2"：六轴异型二；
- "R_GENERAL_5S"：五轴机器人；
- "R_SCARA"：四轴SCARA机器人；
- "R_SCARA_1"：四轴SCARA异型一机器人；
- "R_FOURAXIS_PALLET"：四轴连杆码垛机器人；
- "R_FOURAXIS_PALLET_1"：四轴码垛丝杆机器人；
- "R_FOURAXIS"：四轴机器人；
- "R_FOUR_CARTESIAN_COORDINATE"：四轴直角机器人；
- "R_FOUR_POLAR_COORDINATE_1"：四轴极坐标异形机器人；
- "R_SCARA_THREEAXIS"：三轴SCARA机器人；
- "R_THREE_CARTESIAN_COORDINATE"：三轴直角机器人；
- "R_THREE_CARTESIAN_COORDINATE_1"：三轴异形一机器人；
- "R_SCARA_TWOAXIS"：二轴SCARA机器人；
- "R_GENERAL_7S"：七轴通用机器人；
- "R_GENERAL_1S"：一轴机器人；
- "R_GANTRY_WELD"：五轴龙门焊接机器人；
- "R_DELTA"：delta机器人(四轴并联机器人)；
- "R_WINE_CHAMFER"：酒槽机型；
- "R_GANTRY_WELD_2"：五轴龙门焊接机器人类型2；
- "R_FOUR_CARTESIAN_COORDINATE_1"：四轴直角异型一机器人；
- "R_GANTRY_WELD_6"：六轴龙门焊接机器人；
- "FIVE_AXLE_MIXED"：五轴混动机器人；
- "R_SCARA_FOURAXIS_2"：四轴SCARA异型2；
- "R_SIX_AXLE_ABNORMITY_3"：六轴异型三；
- "R_SCARA_THREEAXIS_1"：三轴SCARA异型1；
- "R_DELTA_2D_"：delta2D并联机器人模型；
- "R_GANTRY_WELD_3"：五轴龙门焊接机器人类型3；
- "R_GENERAL_3S_1"：三轴串联异形一；
- "R_GENERAL_5S_COLLABORATIVE_"：五轴协作机器人；
- "R_SCARA_3_"：四轴SCARA异型三机器人；
- "R_GENERAL_6S_CBBARA_"：六轴串联-CBBARA；
- "R_HEAVY_DUTY_FOUR_AXIS_"：高格立柱旋转四轴

- "servoMap":[0,0,0,0,0,0]

- 伺服映射列表；int类型
- 列表长度为机器人轴数

- "note":" "

```
{
  "robot":
  [
    {
      "note":"",
      "robotType":"R_GENERAL_7S",
      "servoMap":[0,0,0,0,0,0,0]
    },
    {
      "note":"",
      "robotType":"R_GENERAL_5S",
      "servoMap":[0,0,0,0,0]
    },
    {
      "note":"",
      "robotType":"R_GENERAL_6S",
      "servoMap":[0,0,0,0,0,0]
    }
  ],
  "sum":3
}
```
- 注释；string类型

- 上位机查询当前机器人类型及映射

```
{}
```
- 命令字：0x2003

- 控制器回复上位机当前机器人类型及映射

- 命令字：0x2004

- "sum":1
- 表示机器人数目；int类型，范围[1,4]
- "servoSum":

- 伺服个数；int类型

- "robot":

- 机器人参数列表，包含有机器人类型、伺服映射、注释
- 列表长度为机器人数目
- "robotType": "R_GENERAL_6S"

- 表示机器人类型；string类型
- "R_NULL"：未选择机器人类型；
- "R_GENERAL_6S"：六轴串联多关节；
- "R_GENERAL_6S_1"：六轴协作；
- "R_SIXAXIS_SPRAY_BBR"：六轴喷涂机器人；
- "R_GENERAL_6S_2"：六轴异型二；
- "R_GENERAL_5S"：五轴机器人；
- "R_SCARA"：四轴SCARA机器人；
- "R_SCARA_1"：四轴SCARA异型一机器人；
- "R_FOURAXIS_PALLET"：四轴连杆码垛机器人；
- "R_FOURAXIS_PALLET_1"：四轴码垛丝杆机器人；
- "R_FOURAXIS"：四轴机器人；
- "R_FOUR_CARTESIAN_COORDINATE"：四轴直角机器人；
- "R_FOUR_POLAR_COORDINATE_1"：四轴极坐标异形机器人；
- "R_SCARA_THREEAXIS"：三轴SCARA机器人；
- "R_THREE_CARTESIAN_COORDINATE"：三轴直角机器人；
- "R_THREE_CARTESIAN_COORDINATE_1"：三轴异形一机器人；
- "R_SCARA_TWOAXIS"：二轴SCARA机器人；
- "R_GENERAL_7S"：七轴通用机器人；
- "R_GENERAL_1S"：一轴机器人；
- "R_GANTRY_WELD"：五轴龙门焊接机器人；
- "R_DELTA"：delta机器人(四轴并联机器人)；
- "R_WINE_CHAMFER"：酒槽机型；
- "R_GANTRY_WELD_2"：五轴龙门焊接机器人类型2；
- "R_FOUR_CARTESIAN_COORDINATE_1"：四轴直角异型一机器人；
- "R_GANTRY_WELD_6"：六轴龙门焊接机器人；
- "FIVE_AXLE_MIXED"：五轴混动机器人；
- "R_SCARA_FOURAXIS_2"：四轴SCARA异型2；
- "R_SIX_AXLE_ABNORMITY_3"：六轴异型三；
- "R_SCARA_THREEAXIS_1"：三轴SCARA异型1；
- "R_DELTA_2D_"：delta2D并联机器人模型；
- "R_GANTRY_WELD_3"：五轴龙门焊接机器人类型3；
- "R_GENERAL_3S_1"：三轴串联异形一；
- "R_GENERAL_5S_COLLABORATIVE_"：五轴协作机器人；
- "R_SCARA_3_"：四轴SCARA异型三机器人；
- "R_GENERAL_6S_CBBARA_"：六轴串联-CBBARA；
- "R_HEAVY_DUTY_FOUR_AXIS_"：高格立柱旋转四轴

- "servoMap":[0,0,0,0,0,0]

- 伺服映射列表；int类型
- 列表长度为机器人轴数

- "note":" "

```
{
  "robot":
  [
    {
      "note":"",
      "robotType":"R_GENERAL_7S",
      "servoMap":[0,0,0,0,0,0,0]
    },
    {
      "note":"",
      "robotType":"R_GENERAL_5S",
      "servoMap":[0,0,0,0,0]
    },
    {
      "note":"",
      "robotType":"R_GENERAL_6S",
      "servoMap":[0,0,0,0,0,0]
    }
  ],
  "servoSum":0,
  "sum":3
}
```
### 机器人数目

- 注释；string类型

- 说明：

- 查询机器人数目

- 上位机查询机器人数目

```
{}
```
- 命令字：0x2010

- 控制器回复上位机机器人数目

- 命令字：0x2011

- "sum":1

```
{
  "sum":1
}
```
### 机器人通讯周期

- 表示机器人数目；int类型，范围[1,4]

- 说明：

- 机器人通讯周期、波特率、伺服控制字、丢帧容差参数的设置与查询，其中波特率、伺服控制字、丢帧容差在canopen通讯时起作用，控制器重启生效

- 上位机设置机器人通讯周期时发送

- 命令字：0x2020

- "baudRate":"500K"

- 波特率；string类型，取值"10K","20K","50K","100K","500K","800K","1000K"

- "controlCycle":1

- 通讯周期；int 类型，取值范围1,2,4,8 ms

- "control_word":7

- 伺服控制字；int类型，取值范围[7,8]

- "pdo_lost_tolerance":2

```
{
  "baudRate":"500K",
  "controlCycle":1,
  "control_word":7,
  "pdo_lost_tolerance":2
}
```
- 丢帧容差；int类型，取值范围[1,5]

- 上位机查询机器人通讯周期时发送

```
{}
```
- 命令字：0x2021

- 控制器回复上位机机器人通讯周期时发送

- 命令字：0x2022

- "baudRate":"500K"

- 波特率；string类型，范围"10K","20K","50K","100K","500K","800K","1000K"

- "busType":1

- 通讯方式；int类型，范围1,16
- 值为1时使用etherCat通讯，值为16时使用CanOpen通讯

- "controlCycle":1

- 通讯周期；int 类型，范围1,2,4,8 ms

- "control_word":7

- 伺服控制字；int类型，范围[7,8]

- "pdo_lost_tolerance":2

```
{
  "baudRate":"500K",
  "busType":1,
  "controlCycle":1,
  "control_word":7,
  "pdo_lost_tolerance":2
}
```
### 机器人同步轴

- 丢帧容差；int类型，范围[1,5]

- 说明：

- 机器人外部轴参数设置与查询

- 上位机设置机器人同步轴发送

- 命令字：0x2030

- "sum":1

- 外部轴组数；int 类型，范围[0,12]

- "extGroup":

- 外部轴参数列表，包含有外部轴类型、伺服映射、注释
- 列表长度为外部轴数目
- "groupType": 1

- 表示外部轴类型；int类型，范围[0,5]
- 0表示无外部轴；1表示旋转单轴；2表示旋转双轴；3表示直线单轴；4表示直线双轴；5表示直线三轴

- "servoMap":[0,0,0]

- 伺服映射列表；int类型
- 列表长度为3

- "note":" "

```
{
  "extGroup":
  [
    {
      "note":"",
      "groupType":1,
      "servoMap":[0,0,0]
    },
  ],
  "sum":1
}
```
- 注释；string类型

- 上位机查询机器人同步轴

```
{}
```
- 命令字：0x2031

- 控制器回复上位机机器人同步轴

- 命令字：0x2032

- "sum":1

- 外部轴组数；int 类型，范围[0,12]

- "servoSum":

- 伺服个数；int类型

- "extGroup":

- 外部轴参数列表，包含有外部轴类型、伺服映射、注释
- 列表长度为外部轴数目
- "groupType": 1

- 表示外部轴类型；int类型，范围[0,5]
- 0表示无外部轴；1表示旋转单轴；2表示旋转双轴；3表示直线单轴；4表示直线双轴；5表示直线三轴

- "servoMap":[0,0,0]

- 伺服映射列表；int类型
- 列表长度为3

- "note":" "

```
{
  "extGroup":
  [
    {
      "note":"",
      "groupType":1,
      "servoMap":[0,0,0]
    },
  ],
  "servoSum":0,
  "sum":1
}
```
### 机器人轴组组合

- 注释；string类型

- 说明：

- 存在多个机器人时，不能共用同一个外部轴组

- 上位机设置机器人轴组组合发送

- 命令字：0x2040

- "binding":

- 轴组组合列表，包含有注释、机器人绑定外部轴组数量、外部轴组绑定列表
- 列表长度为机器人数量
- "extGroupNum":[0,0,0]

- 外部轴组绑定列表；int类型
- 列表长度为3，范围为0~已设置的同步轴数

- "extGroupSum": 1

- 表示机器人绑定外部轴组数量；int类型，范围[0,3]

- "note":" "

```
{
  "binding":
  [
    {
      "extGroupNum":[1,2,0],
      "extGroupSum":2,
      "note":""
    },
    {
      "extGroupNum":[0,0,0],
      "extGroupSum":0,
      "note":""
    },
  ],
}
```
- 注释；string类型

- 上位机查询机器人轴组组合

```
{}
```
- 命令字：0x2041

- 控制器回复上位机机器人轴组组合

- 命令字：0x2042

- "binding":

- 轴组组合列表，包含有注释、机器人绑定外部轴组数量、外部轴组绑定列表
- 列表长度为机器人数量
- "extGroupNum":[0]

- 外部轴组绑定列表；int类型
- 列表长度为绑定外部轴组数量，最小为1，范围为0~已设置的同步轴数

- "extGroupSum": 1

- 表示机器人绑定外部轴组数量；int类型，范围[0,3]

- "note":" "

- 注释；string类型

- "sum":2

```
{
  "binding":
  [
    {
      "extGroupNum":[1,2],
      "extGroupSum":2,
      "note":""
    },
    {
      "extGroupNum":[0],
      "extGroupSum":0,
      "note":""
    },
  ],
  "sum":2
}
```
### 机器人轴从动轴配置

- 机器人数量；int类型，范围[1,4]

- 说明：

- 机器人或外部轴关节从动轴配置设置与查询

- 上位机设置机器人从动轴配置发送

- 命令字：0x2050

- "robot":

- 从动轴配置参数总列表，长度为机器人数量
- "sum": 3

- 从动轴个数；int 类型，范围[0,3]

- "data":

- 从动轴配置参数列表，长度为当前机器人的轴数
- "dir": -1

- 相对主电机方向；int 类型，范围-1,1

- "encoder": 8

- 编码器位数；int 类型，范围[1,32]

- "num": 0

- 伺服映射；int 类型

- "reducRatio": 1.0

```
{
  "robot":
  [
    [
      {
        "data":
        [
          {
            "dir":-1,
            "encoder":8,
            "num":0,
            "reducRatio":2.0
          },
          {
            "dir":1,
            "encoder":9,
            "num":0,
            "reducRatio":3.0
          },
        ],
        "sum":2
      },
      {
        "data":
        [
          {
            "dir":-1,
            "encoder":8,
            "num":0,
            "reducRatio":2.0
          },
        ],
        "sum":1
      },
      {
        "sum":0
      }
      {
        "sum":0
      }
      {
        "sum":0
      }
      {
        "sum":0
      }
    ],
    [
      {
        "data":
        [
          {
            "dir":-1,
            "encoder":8,
            "num":0,
            "reducRatio":2.0
          },
        ],
        "sum":1
      },
      {
        "sum":0
      },
      {
        "sum":0
      }
      {
        "sum":0
      }
      {
        "sum":0
      }
      {
        "sum":0
      }
    ]
  ]
}
```
- 减速比；double 类型，范围[0,500]

- 上位机查询机器人从动轴配置

```
{}
```
- 命令字：0x2051

- 控制器回复上位机机器人从动轴配置

- 命令字：0x2052

- "robot":

- 从动轴配置参数总列表，长度为机器人数量
- "sum": 3

- 从动轴个数；int 类型，范围[0,3]

- "data":

- 从动轴配置参数列表，长度为当前机器人的轴数
- "dir": -1

- 相对主电机方向；int 类型，范围-1,1

- "encoder": 8

- 编码器位数；int 类型，范围[1,32]

- "num": 0

- 伺服映射；int 类型

- "reducRatio": 1.0

```
{
  "robot":
  [
    [
      {
        "data":
        [
          {
            "dir":-1,
            "encoder":8,
            "num":0,
            "reducRatio":2.0
          }
        ],
        "sum":1
      },
      {
        "sum":0
      },
      {
        "sum":0
      }
      {
        "sum":0
      }
      {
        "sum":0
      }
      {
        "sum":0
      }
    ]
  ]
}
```
- 减速比；double 类型，范围[0,500]

- 上位机设置机器人外部轴从动轴配置发送

- 命令字：0x2053

- "external":

- 外部轴从动轴配置参数总列表，长度为外部轴数量
- "sum": 3

- 从动轴个数；int 类型，范围[0,3]

- "data":

- 从动轴配置参数列表，长度为当前机器人的轴数
- "dir": -1

- 相对主电机方向；int 类型，范围-1,1

- "encoder": 8

- 编码器位数；int 类型，范围[1,32]

- "num": 0

- 伺服映射；int 类型

- "reducRatio": 1.0

```
{
  "external":
  [
    [
      {
        "data":
        [
          {
            "dir":1,
            "encoder":3,
            "num":0,
            "reducRatio":1.0
          }
        ],
        "sum":1
      }
    ],
    [
      {
        "sum":0
      },
      {
        "sum":0
      }
    ]
  ]
}
```
- 减速比；double 类型，范围[0,500]

- 上位机查询机器人外部轴从动轴配置

```
{}
```
- 命令字：0x2054

- 控制器回复上位机机器人外部轴从动轴配置

- 命令字：0x2055

- "external":

- 外部轴从动轴配置参数总列表，长度为机器人数量
- "sum": 3

- 从动轴个数；int 类型，范围[0,3]

- "data":

- 从动轴配置参数列表，长度为当前机器人的轴数
- "dir": -1

- 相对主电机方向；int 类型，范围-1,1

- "encoder": 8

- 编码器位数；int 类型，范围[1,32]

- "num": 0

- 伺服映射；int 类型

- "reducRatio": 1.0

```
{
  "external":
  [
    [
      {
        "data":
        [
          {
            "dir":1,
            "encoder":3,
            "num":0,
            "reducRatio":1.0
          }
        ],
        "sum":1
      }
    ],
    [
      {
        "sum":0
      },
      {
        "sum":0
      }
    ]
  ]
}
```
### 机器人运行时间

- 减速比；double 类型，范围[0,500]

- 说明：

- 查询当前机器人主程序运行时间

- 上位机查询机器人主程序运行时间

- 命令字：0x2060

- "robot":1

```
{
  "robot":1
}
```
- 表示要查询的机器人；int类型，范围[1,4]

- 控制器回复上位机机器人主程序运行时间

- 命令字：0x2055

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "time": 10

```
{
  "robot":1,
  "time":10
}
```
### 复制机器人参数

- 从动轴个数；int 类型，单位s

- 说明：

- 将机器人参数复制到另一个机器人上
- 参数可以复制到除本机的多个机器人上，与参数机型不一致的机器人会复制失败

- 上位机复制机器人参数发送

- 命令字：0x2062

- "copyToRobot":[false,true,false,false]

- 参数复制到机器人列表；bool类型，长度为4
- true为进行复制，false为不进行复制

- "mainRobot":1

```
{
  "copyToRobot":[false,true,false,false],
  "mainRobot":1
}
```
### 协作机器人

- 复制参数的机器人号

- 说明

- 协作机器人相关参数的设置与查询，包含有双机协作、防抱闸压紧等功能

- 上位机设置双机协作模式发送

- 命令字：0x2070

- "cooperationRobots":true

```
{
  "cooperationRobots":true
}
```
- 是否启用双机同步模式；bool类型
- true为启用，false为不启用

- 上位机查询双机协作模式

```
{}
```
- 命令字：0x2071

- 控制器回复上位机双机协作模式

- 命令字：0x2072

- "cooperationRobots":true

```
{
  "cooperationRobots":true
}
```
- 是否启用双机同步模式；bool类型
- true为启用，false为不启用

- 上位机设置防抱闸压紧使能

- 命令字：0x2073

- "enable":true

```
{
  "enable":true
}
```
- 防抱闸压紧使能开关；bool类型
- true为开启，false为关闭

- 上位机查询防抱闸压紧使能

```
{}
```
- 命令字：0x2074

- 控制器回复上位机防抱闸压紧使能

- 命令字：0x2075

- "enable":true

```
{
  "enable":true
}
```
- 防抱闸压紧使能开关；bool类型
- true为开启，false为关闭

- 上位机设置防抱闸压紧延时

- 命令字：0x2076

- "enableDelay":0.5

- 防抱闸压紧使能延时；double类型，范围[0,99999.99]s
- 单位为s

- "brakeOnDelay":0.5

- 开抱闸延时；double类型，范围[0,99999.99]s
- 单位为s

- "brakeOffDelay":0.5

```
{
  "enableDelay":0.5,
  "brakeOnDelay":0.5,
  "brakeOffDelay":0.5
}
```
- 抱闸关闭后延时；double类型，范围[0,99999.99]s
- 单位为s

- 上位机查询防抱闸压紧延时

```
{}
```
- 命令字：0x2077

- 控制器回复上位机防抱闸压紧延时

- 命令字：0x2078

- "enableDelay":0.5

- 防抱闸压紧使能延时；double类型，范围[0,99999.99]s
- 单位为s

- "brakeOnDelay":0.5

- 开抱闸延时；double类型，范围[0,99999.99]s
- 单位为s

- "brakeOffDelay":0.5

```
{
  "enableDelay":0.5,
  "brakeOnDelay":0.5,
  "brakeOffDelay":0.5
}
```
- 抱闸关闭后延时；double类型，范围[0,99999.99]s
- 单位为s

- 上位机设置抱闸参数

- 命令字：0x2079

- "jointNum":1

- 当前设置的关节号；int类型，范围[1,6]

- "EncodeNum":1

- 编码器个数；int类型，范围[1,2]
- 抱闸类型为插销式时生效

- "Encode1Resolusion":17

- 编码器1位数；int类型，范围[0,99999]
- 抱闸类型为插销式时生效

- "Encode2Resolusion":17

- 编码器2位数；int类型，范围[0,99999]
- 抱闸类型为插销式且编码器个数为2时生效
- 编码器个数为1时需设置为0

- "BrakeType":1

- 抱闸类型；int类型，范围[1,2]
- 1为插销式 , 2为刹片式

- "Distance":20.5

- 运动距离；double类型，范围[0,99999.99]
- 抱闸类型为刹片式时需设置为0

- "CheckDistance":0.0

- 检测距离；double类型，范围[0,99999.99]
- 抱闸类型为插销式且防抱闸压紧使能开启时生效

- "CheckTorq":0.0

```
{
  "BrakeType":2,
  "CheckDistance":0.0,
  "CheckTorq":0.0,
  "Distance":0,
  "Encode1Resolusion":17,
  "Encode2Resolusion":0,
  "EncodeNum":1,
  "jointNum":1
}
```
- 检测力矩；double类型，范围[0,99999.99]
- 抱闸类型为插销式且防抱闸压紧使能开启时生效

- 上位机查询抱闸参数

- 命令字：0x207A

- "jointNum":1

```
{
  "jointNum":1
}
```
- 查询的关节抱闸参数；int类型，范围[1,6]

- 控制器回复上位机抱闸参数

- 命令字：0x2079

- "jointNum":1

- 当前设置的关节号；int类型，范围[1,6]

- "EncodeNum":1

- 编码器个数；int类型，范围[1,2]

- "Encode1Resolusion":17

- 编码器1位数；int类型，范围[0,99999]

- "Encode2Resolusion":17

- 编码器2分辨率；int类型，范围[0,99999]

- "BrakeType":1

- 抱闸类型；int类型，范围[1,2]

- "Distance":20.5

- 运动距离；double类型，范围[0,99999.99]

- "CheckDistance":0.0

- 检测距离；double类型，范围[0,99999.99]

- "CheckTorq":0.0

```
{
  "BrakeType":2,
  "CheckDistance":0.0,
  "CheckTorq":0.0,
  "Distance":0,
  "Encode1Resolusion":17,
  "Encode2Resolusion":0,
  "EncodeNum":1,
  "jointNum":1
}
```
- 检测力矩；double类型，范围[0,99999.99]

- 上位机查询静态力矩

```
{}
```
- 命令字：0x207C

- 控制器回复上位机静态力矩

- 命令字：0x207D

- "torq":[0.0,0.0,0.0,0.0,0.0,0.0]

```
{
    "torq":[0.0,0.0,0.0,0.0,0.0,0.0]
}
```
- 静态力矩列表；doule类型，长度为6

- 上位机设置协作机器人个数

- 命令字：0x207E

- "cooperativeRobot":1

```
{
  "cooperativeRobot":1
}
```
- 协作机器人个数；int类型，范围[0,4]
- 0时表示无协作机器人

- 上位机查询协作机器人个数

```
{}
```
- 命令字：0x207F

- 控制器回复上位机协作机器人个数

- 命令字：0x2080

- "cooperativeRobot":1

```
{
  "cooperativeRobot":1
}
```
### 外部轴参数

- 协作机器人个数；int类型

- 说明

- 外部轴相关参数的设置与查询，包含有零点、关节参数、点动速度等

- 上位机设置外部轴零点/清多圈值

- 命令字：0x20A0

- "robot": 1

- 当前机器人号；int 类型，范围 [1,4]

- "axis": 1

- 外部轴轴号；int类型，范围[0,5]
- 0时为设置全部轴

- "clearEncoder": false

```
{
  "robot": 1,
  "axis": 1,
  "clearEncoder": false
}
```
- 是否清除多圈值；bool类型

- 控制器回复上位机外部轴零点设置/清多圈值结果

- 命令字：0x20A1

- "robot": 1

- 当前机器人号；int 类型，范围 [1,4]

- "axis": 1

- 外部轴轴号；int类型，范围[0,5]
- 0时为设置全部轴

- "result": 0

```
{
  "robot": 1,
  "axis": 1,
  "result": 0
}
```
- 标零/清多圈值结果；int类型
- 0为标零/清除失败，1为标零/清除成功

- 上位机设置外部轴零点偏移

- 命令字：0x20A2

- "robot": 1

- 当前机器人号；int 类型，范围 [1,4]

- "axis": 1

- 外部轴轴号；int类型，范围[0,5]
- 0时为设置全部轴

- "offset":[6.0,0,0,0,0]

```
{
  "axis":1,
  "offset":[6.0,0,0,0,0],
  "robot":1
}
```
- 轴零点偏移值列表；double类型
- 长度为5，当外部轴轴号非0时，仅对应位置有值，其他轴都该为0

- 上位机设置外部轴单圈值

- 命令字: 0x20A3

- "robot": 1

- 当前机器人号；int 类型，范围 [1,4]

- "axis": 1

- 当前轴号；int 类型，范围[1,5]

- "singleEncoder": 0

```
{
  "robot": 1,
  "axis": 1,
  "singleEncoder": 0
}
```
- 单圈值数值；int类型，范围[0,999999999]

- 上位机查询外部轴单圈值

- 命令字：0x20A4

- "robot": 1
- 当前机器人号；int 类型，范围 [1,4]

- "axis": 1

```
{
  "robot": 1,
  "axis": 1
}
```
- 当前轴号；int 类型，范围[1,5]

- 控制器回复上位机外部轴单圈值

- 命令字：0x20A5

- "robot": 1

- 当前机器人号；int 类型，范围 [1,4]

- "axis": 1

- 当前轴号；int 类型，范围[1,5]

- "singleEncoder": 0

```
{
  "robot": 1,
  "axis": 1,
  "singleEncoder": 0
}
```
- 单圈值数值；int类型，范围[0,999999999]

- 上位机设置外部轴关节参数

- 命令字: 0x20A6

- "robot": 1

- 当前机器人号；int 类型，范围 [1,4]

- "isNotInsideRobot":false

- 当前控制对象是否为外部设备；bool 类型
- 非ide可不发

- "externalGroupNum": 1

- 外部轴组号；int 类型，范围[1,3]
- 该参数最大为当前机器人绑定的外部轴数量
- 当"isNotInsideRobot"为true时，该参数表示总编号，而不是机器人内部的编号

- "joint":

- 关节参数列表，长度为当前外部轴的轴数

- "backLash": 0.0

- 齿轮反向间隙；double 类型，范围[0,10]
- 该功能还需完善，建议填写0.0

- "direction": 1

- 模型方向；int 类型，范围1,-1
- 1为正方向，-1为负方向

- "encoderResolution": 17

- 编码器位数；int 类型，范围[1,100]

- "maxAcc": 1.50

- 关节最大加速度；double 类型，范围[1,10000]

- "maxDec": -1.50

- 关节最大减速度；double 类型，范围[-10000,-1]

- "maxJerkAcc": 1.0

- 最大加加速度；double 类型，范围[1,20000]
- 机器人插补方式为加加速度时生效

- "maxJerkDec": -1.0

- 最大减减速度；double类型，范围[-20000,-1]
- 机器人插补方式为加加速度时生效

- "maxRPM": 1.0

- 最大正转速；double 类型，范围[1,5]

- "maxReverseRPM": -1.0

- 最大反转速；double 类型，范围[-5,-1]

- "positiveLimit": 999.0

- 关节正限位；double 类型，范围[1,3000]°
- 值100000000  表示不限速

- "ratedRPM": 3000.0

- 额定正转速；double 类型，范围[1,10000]rpm

- "ratedReverseRPM": -3000.0

- 额定反转速；double 类型，范围[-10000,-1]rpm
- 数值为额定正速度的负值

- "ratedReverseSpeed": -3600.0

- 关节额定反速度；double 类型，单位°/s
- 旋转外部轴时，公式为 关节额定反速度 = 额定反速度 / 关节减速比 * 6
- 直线外部轴时，公式为 关节额定反速度 = 方向转换比 * (额定反速度 / 关节减速比 * 6) / 360

- "ratedSpeed": 3600.0

- 关节额定正速度；double 类型，单位°/s
- 旋转外部轴时，公式为 关节额定正速度 = 额定正速度 / 关节减速比 * 6
- 直线外部轴时，公式为 关节额定正速度 = 方向转换比 * (额定正速度 / 关节减速比 * 6) / 360

- "reducRatio": 5.0

- 关节减速比；double 类型，范围(0,1000]

- "reverseLimit": -999.0

```
{
  "externalGroupNum": 1,
  "isNotInsideRobot":false,
  "joint":
  [
    {
      "backLash": 0.0,
      "direction": 1,
      "encoderResolution": 17,
      "maxAcc": 1.50,
      "maxDec": -1.50,
      "maxJerkAcc": 1.0,
      "maxJerkDec": -1.0,
      "maxRPM": 1.0,
      "maxReverseRPM": -1.0,
      "positiveLimit": 999.0,
      "ratedRPM": 3000.0,
      "ratedReverseRPM": -3000.0,
      "ratedReverseSpeed": -3600.0,
      "ratedSpeed": 3600.0,
      "reducRatio": 5.0,
      "reverseLimit": -999.0
    }
  ],
  "robot": 1
}
```
- 关节反限位；double 类型，范围[-3000,-1]°
- 值100000000  表示不限速

- 上位机查询外部轴关节参数

- 命令字：0x20A7

- "robot": 1

- 当前机器人号；int类型，范围[1,4]

- "externalGroupNum": 1

- 轴组组合的组号；int类型
- 该参数最大为当前机器人绑定的外部轴数量
- 当"isNotInsideRobot"为true时，该参数表示总编号，而不是机器人内部的编号

- "isNotInsideRobot":false

```
{
  "robot": 1,
  "externalGroupNum": 1,
  "isNotInsideRobot": false
}
```
- 当前控制对象是否为外部设备；bool 类型
- 非ide可不发

- 控制器回复上位机外部轴关节参数

- 命令字：0x20A8

- "robot": 1

- 当前机器人号；int 类型，范围 [1,4]

- "isNotInsideRobot":false

- 当前控制对象是否为外部设备；bool 类型

- "externalGroupNum": 1

- 外部轴组号；int 类型，范围[1,3]
- 该参数最大为当前机器人绑定的外部轴数量
- 当"isNotInsideRobot"为true时，该参数表示总编号，而不是机器人内部的编号

- "joint":

- 关节参数列表，长度为当前外部轴的轴数
- "backLash": 0.0

- 齿轮反向间隙；double 类型，范围[0,10]
- 该功能还需完善，建议填写0.0

- "direction": 1

- 模型方向；int 类型，范围1,-1
- 1为正方向，-1为负方向

- "encoderResolution": 17

- 编码器位数；int 类型，范围[1,100]

- "maxAcc": 1.50

- 关节最大加速度；double 类型，范围[1,10000]

- "maxDec": -1.50

- 关节最大减速度；double 类型，范围[-10000,-1]

- "maxJerkAcc": 1.0

- 最大加加速度；double 类型，范围[1,20000]
- 机器人插补方式为加加速度时生效

- "maxJerkDec": -1.0

- 最大减减速度；double类型，范围[-20000,-1]
- 机器人插补方式为加加速度时生效

- "maxRPM": 1.0

- 最大正转速；double 类型，范围[1,5]

- "maxReverseRPM": -1.0

- 最大反转速；double 类型，范围[-5,-1]

- "positiveLimit": 999.0

- 关节正限位；double 类型，范围[1,3000]°

- "ratedRPM": 3000.0

- 额定正转速；double 类型，范围[1,10000]rpm

- "ratedReverseRPM": -3000.0

- 额定反转速；double 类型，范围[-10000,-1]rpm
- 数值为额定正速度的负值

- "ratedReverseSpeed": -3600.0

- 关节额定反速度；double 类型，单位°/s
- 旋转外部轴时，公式为 关节额定反速度 = 额定反速度 / 关节减速比 * 6
- 直线外部轴时，公式为 关节额定反速度 = 方向转换比 * (额定反速度 / 关节减速比 * 6) / 360

- "ratedSpeed": 3600.0

- 关节额定正速度；double 类型，单位°/s
- 旋转外部轴时，公式为 关节额定正速度 = 额定正速度 / 关节减速比 * 6
- 直线外部轴时，公式为 关节额定正速度 = 方向转换比 * (额定正速度 / 关节减速比 * 6) / 360

- "reducRatio": 5.0

- 关节减速比；double 类型，范围(0,1000]

- "reverseLimit": -999.0

```
{
  "externalGroupNum": 1,
  "isNotInsideRobot":false,
  "joint":
  [
    {
      "backLash": 0.0,
      "direction": 1,
      "encoderResolution": 17,
      "maxAcc": 1.50,
      "maxDec": -1.50,
      "maxJerkAcc": 1.0,
      "maxJerkDec": -1.0,
      "maxRPM": 1.0,
      "maxReverseRPM": -1.0,
      "positiveLimit": 999.0,
      "ratedRPM": 3000.0,
      "ratedReverseRPM": -3000.0,
      "ratedReverseSpeed": -3600.0,
      "ratedSpeed": 3600.0,
      "reducRatio": 5.0,
      "reverseLimit": -999.0
    }
  ],
  "robot": 1
}
```
- 关节反限位；double 类型，范围[-3000,-1]°

- 上位机设置外部轴关节点动速度

- 命令字: 0x20A9

- "robot": 1

- 当前机器人号；int 类型，范围 [1,4]

- "externalGroupNum": 1

- 外部轴组号；int 类型，范围[1,3]
- 该参数最大为当前机器人绑定的外部轴数量
- 当"isNotInsideRobot"为true时，该参数表示总编号，而不是机器人内部的编号

- "isNotInsideRobot":false

- 当前控制对象是否为外部设备；bool 类型
- 非ide可不发

- "externalJogParameter":

- 关节点动速度列表，长度为当前外部轴轴数
- "maxAcc":800.0

- 关节轴点动加速度；double类型，范围[1,1000]°/s^2

- "maxSpeed":40.0

```
{
  "externalGroupNum":1,
  "externalJogParameter":
  [
    {
      "maxAcc":800.0,
      "maxSpeed":40.0
    }
  ],
  "isNotInsideRobot":false,
  "robot":1
}
```
- 关节轴最大点动速度；double类型，范围[1,100]°/s

- 上位机查询外部轴关节点动速度

- 命令字：0x20AA

- "robot": 1

- 当前机器人号；int类型，范围[1,4]

- "externalGroupNum": 1

- 轴组组合的组号；int类型
- 该参数最大为当前机器人绑定的外部轴数量
- 当"isNotInsideRobot"为true时，该参数表示总编号，而不是机器人内部的编号

- "isNotInsideRobot":false

```
{
  "externalGroupNum":1,
  "isNotInsideRobot":false,
  "robot":1
}
```
- 当前控制对象是否为外部设备；bool 类型
- 非ide可不发

- 控制器回复上位机外部轴关节点动速度

- 命令字：0x20AB

- "robot": 1

- 当前机器人号；int 类型，范围 [1,4]

- "externalGroupNum": 1

- 外部轴组号；int 类型，范围[1,3]
- 该参数最大为当前机器人绑定的外部轴数量
- 当"isNotInsideRobot"为true时，该参数表示总编号，而不是机器人内部的编号

- "isNotInsideRobot":false

- 当前控制对象是否为外部设备；bool 类型

- "externalJogParameter":

- 关节点动速度列表，长度为当前外部轴轴数
- "maxAcc":800.0

- 关节轴点动加速度；double类型，范围[1,1000]°/s^2

- "maxSpeed":40.0

```
{
  "externalGroupNum":1,
  "externalJogParameter":
  [
    {
      "maxAcc":800.0,
      "maxSpeed":40.0
    }
  ],
  "isNotInsideRobot":false,
  "robot":1
}
```
- 关节轴最大点动速度；double类型，范围[1,100]°/s

- 上位机查询外部轴单轴标定结果点位

- 命令字：0x20AC

- "syncPositionerNum": 1

- 外部轴号；int 类型，范围[1,3]

- "coordNum": 1

```
{
  "syncPositionerNum":1,
  "coordNum":1
}
```
- 外部轴的坐标系标号；int 类型；取值范围[0,3]

- 控制器回复上位机外部轴单轴标定结果点位

- 命令字：0x20AD

- "syncPositionerNum": 1

- 外部轴号；int 类型，范围[1,3]

- "coordNum": 1

- 外部轴的坐标系标号；int 类型；取值范围[0,3]

- "pos":[0,0,0,0,0,0]

```
{
  "syncPositionerNum":1,
  "coordNum":1,
  "pos":[0,0,0,0,0,0]
}
- 点位数据；double 数组，长度为6

```