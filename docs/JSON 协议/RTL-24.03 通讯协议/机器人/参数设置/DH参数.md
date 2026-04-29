# DH参数

### 机器人基础参数

- 说明：

- 包含有DH参数、关节参数、笛卡尔参数等机器人基础参数的设置与查询

- 上位机设置当前机器人DH参数

- 命令字: 0x20C0

- 六轴串联机器人（存在耦合时动态限位生效）

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0

- L6杆长；double类型，范围[-4000,4000]

- "L7":0.0

- L7杆长；double类型，范围[-4000,4000]

- "L8":0.0

- L8杆长；double类型，范围[-4000,4000]

- "couplingRatio12":0.0

- 1/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "couplingRatio32":0.0

- 3/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "couplingRatio45":0.0

- 4/5耦合比；double类型，范围[-1000,1000]

- "couplingRatio46":0.0

- 4/6耦合比；double类型，范围[-1000,1000]

- "couplingRatio56":0.0

- 5/6耦合比；double类型，范围[-1000,1000]

- "fiveAxisDirection":90.0

- 五轴方向；double类型，范围0,90 度

- "dynamicLimit":

- J2+J3范围限制
- "max":0.0

- J2+J3最大值；double类型，范围[-500,500]

- "min":0.0

- J2+J3最小值；double类型，范围[-500,500]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":120.0,
  "L7":0.0,
  "L8":0.0,
  "couplingRatio12":0.0,
  "couplingRatio23":0.0,
  "couplingRatio32":0.0,
  "couplingRatio34":0.0,
  "couplingRatio45":0.0,
  "couplingRatio46":0.0,
  "couplingRatio56":0.0,
  "dynamicLimit":
  {
    "max":0.0,
    "min":0.0
  },
  "fiveAxisDirection":90.0,
  "mountAngle":false,
  "robot":1
}    
```
- 当前机器人号；int类型，范围[1,4]

- 六轴协作机器人

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0

- L6杆长；double类型，范围[-4000,4000]

- "L7":0.0

- L7杆长；double类型，范围[-4000,4000]

- "couplingRatio12":0.0

- 1/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "couplingRatio32":0.0

- 3/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "couplingRatio45":0.0

- 4/5耦合比；double类型，范围[-1000,1000]

- "couplingRatio46":0.0

- 4/6耦合比；double类型，范围[-1000,1000]

- "couplingRatio56":0.0

- 5/6耦合比；double类型，范围[-1000,1000]

- "threeAxisDirection":-90.0

- 三轴方向；double类型，范围-90,0 度

- "fiveAxisDirection":90.0

- 五轴方向；double类型，范围0,90 度

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":120.0,
  "L7":120.0,
  "couplingRatio12":0.0,
  "couplingRatio23":0.0,
  "couplingRatio32":0.0,
  "couplingRatio34":0.0,
  "couplingRatio45":0.0,
  "couplingRatio46":0.0,
  "couplingRatio56":0.0,
  "fiveAxisDirection":90.0,
  "mountAngle":false,
  "robot":1,
  "threeAxisDirection":-90.0
}
```
- 当前机器人号；int类型，范围[1,4]

- 六轴喷涂机器人

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":0.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0

- L6杆长；double类型，范围[-4000,4000]

- "L7":0.0

- L7杆长；double类型，范围[-4000,4000]

- "L8":0.0

- L7杆长；double类型，范围[-4000,4000]

- "couplingRatio12":0.0

- 1/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "couplingRatio32":0.0

- 3/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "couplingRatio45":0.0

- 4/5耦合比；double类型，范围[-1000,1000]

- "couplingRatio46":0.0

- 4/6耦合比；double类型，范围[-1000,1000]

- "couplingRatio56":0.0

- 5/6耦合比；double类型，范围[-1000,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":0.0,
  "L4":120.0,
  "L5":120.0,
  "L6":120.0,
  "L7":0.0,
  "L8":0.0,
  "couplingRatio12":0.0,
  "couplingRatio23":0.0,
  "couplingRatio32":0.0,
  "couplingRatio34":0.0,
  "couplingRatio45":0.0,
  "couplingRatio46":0.0,
  "couplingRatio56":0.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 六轴异型二

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0

- L6杆长；double类型，范围[-4000,4000]

- "couplingRatio12":0.0

- 1/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "couplingRatio32":0.0

- 3/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "couplingRatio45":0.0

- 4/5耦合比；double类型，范围[-1000,1000]

- "couplingRatio46":0.0

- 4/6耦合比；double类型，范围[-1000,1000]

- "couplingRatio56":0.0

- 5/6耦合比；double类型，范围[-1000,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":120.0,
  "couplingRatio12":0.0,
  "couplingRatio23":0.0,
  "couplingRatio32":0.0,
  "couplingRatio34":0.0,
  "couplingRatio45":0.0,
  "couplingRatio46":0.0,
  "couplingRatio56":0.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 五轴串联多关节

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0

- L6杆长；double类型，范围[-4000,4000]

- "L7":0.0

- L7杆长；double类型，范围[-4000,4000]

- "couplingRatio12":0.0

- 1/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "couplingRatio32":0.0

- 3/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "couplingRatio45":0.0

- 4/5耦合比；double类型，范围[-1000,1000]

- "couplingRatio46":0.0

- 4/6耦合比；double类型，范围[-1000,1000]

- "fiveAxisDirection":90.0

- 五轴方向；double类型，范围0,90 度

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":120.0,
  "L7":0.0,
  "couplingRatio12":0.0,
  "couplingRatio23":0.0,
  "couplingRatio32":0.0,
  "couplingRatio34":0.0,
  "couplingRatio45":0.0,
  "couplingRatio46":0.0,
  "fiveAxisDirection":90.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 四轴SCARA

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "couplingRatio12":0.0

- 1/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "pitch":80.0

- 螺距；double类型，范围[-1000,0),(0,1000]

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "couplingRatio12":0.0,
  "couplingRatio23":0.0,
  "couplingRatio34":0.0,
  "mountAngle":false,
  "pitch":80.0,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 四轴SCARA异型1

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "pitch":80.0

- 螺距；double类型，范围[-1000,0),(0,1000]

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "couplingRatio34":0.0,
  "mountAngle":false,
  "pitch":80.0,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 四轴连杆码垛

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":0.0

- 偏置值；double类型，范围[-4000,4000]
- 默认为0

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "maxDynamicLimit":0.0
- J2+J3最大值；double类型，范围[-1000,1000]

- "minDynamicLimit":0.0

- J2+J3最小值；double类型，范围[-1000,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":0.0,
  "couplingRatio23":0.0,
  "couplingRatio34":0.0,
  "maxDynamicLimit":0.0,
  "minDynamicLimit":0.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 四轴码垛丝杆

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "amplificationRatio":100.0

- 放大比；double类型，范围[1,1000]

- "conversionRatio2":100.0

- 二轴转换比；double类型，范围[1,1000]

- "conversionRatio3":100.0

- 三轴转换比；double类型，范围[1,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "amplificationRatio":100.0,
  "conversionRatio2":100.0,
  "conversionRatio3":100.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 四轴串联多关节

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "couplingRatio23":0.0,
  "couplingRatio34":0.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 四轴直角机器人

- "conversionRatio_X":100.0

- X轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Y":100.0

- Y轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Z":100.0

- Z轴转换比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "conversionRatio_X":100.0,
  "conversionRatio_Y":100.0,
  "conversionRatio_Z":100.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 四轴极坐标异型

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "conversionRatio2":100.0

- 二轴转换比；double类型，范围[-4000,4000]

- "conversionRatio3":100.0

- 三轴转换比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "conversionRatio2":100.0,
  "conversionRatio3":100.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 三轴SCARA

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "couplingRatio12":0.0

- 1/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "pitch":80.0

- 螺距；double类型，范围[-1000,0),(0,1000]

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "couplingRatio12":0.0,
  "couplingRatio23":0.0,
  "mountAngle":false,
  "pitch":80.0,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 三轴直角机器人

- "conversionRatio_X":100.0

- X轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Y":100.0

- Y轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Z":100.0

- Z轴转换比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "conversionRatio_X":100.0,
  "conversionRatio_Y":100.0,
  "conversionRatio_Z":100.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 三轴直角异型1

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "conversionRatio2":100.0

- 二轴转换比；double类型，范围[-4000,4000]

- "conversionRatio3":100.0

- 三轴转换比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "conversionRatio2":100.0,
  "conversionRatio3":100.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 二轴SCARA

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L2":120.0,
  "L3":120.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 七轴串联多关节

- "Link":

- DH参数列表
- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0

- L6杆长；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "Link":
  {
    "L1":120.0,
    "L2":120.0,
    "L3":120.0,
    "L4":120.0,
    "L5":120.0,
    "L6":120.0
  },
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 龙门焊接模型

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "conversionRatio_X":100.0

- X轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Y":100.0

- Y轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Z":100.0

- Z轴转换比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L4":120.0,
  "L5":120.0,
  "conversionRatio_X":100.0,
  "conversionRatio_Y":100.0,
  "conversionRatio_Z":100.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 四轴并联机器人

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":110.0

- L2杆长；double类型，范围[-4000,4000]
- L2的值需要小于L3的值

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":110.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 酒槽机型

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0
- L6杆长；double类型，范围[-4000,4000]
- "L7":120.0

- L7杆长；double类型，范围[-4000,4000]

- "L8":120.0

- L8杆长；double类型，范围[-4000,4000]

- "L9":120.0

- L9杆长；double类型，范围[-4000,4000]

- "L10":120.0

- L10杆长；double类型，范围[-4000,4000]

- "L11":120.0
- L11杆长；double类型，范围[-4000,4000]
- "L12":120.0

- 滑动电动缸导程；double类型，范围[-4000,4000]

- "L13":120.0

- 顶升电动缸导程；double类型，范围[-4000,4000]

- "L14":120.0

- 喷料距离；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":120.0,
  "L7":120.0,
  "L8":120.0,
  "L9":120.0,
  "L10":120.0,
  "L11":120.0,
  "L12":120.0,
  "L13":120.0,
  "L14":120.0,
  "mountAngle":false,
  "robot":1
}  
```
- 当前机器人号；int类型，范围[1,4]

- 龙门焊接2模型

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "conversionRatio_X":100.0

- X轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Y":100.0

- Y轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Z":100.0

- Z轴转换比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L4":120.0,
  "L5":120.0,
  "conversionRatio_X":100.0,
  "conversionRatio_Y":100.0,
  "conversionRatio_Z":100.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 四轴直角异型一

- "Link":

- DH参数列表
- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "conversionRatio":[100.0,100.0]

- 轴转换比；double类型，范围[1,1000]
- 长度为2，第一个值为一轴转换比，第二个轴为四轴转换比

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "Link":
  {
    "L1":120.0,
    "L2":120.0,
    "conversionRatio":[100.0,100.0]
  },  
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 六轴龙门焊接模型

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0

- L6杆长；double类型，范围[-4000,4000]

- "L7":120.0

- L7杆长；double类型，范围[-4000,4000]

- "conversionRatio_X":100.0

- X轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Y":100.0

- Y轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Z":100.0

- Z轴转换比；double类型，范围[-4000,4000]

- "couplingRatio45":0.0

- 4/5耦合比；double类型，范围[-1000,1000]

- "couplingRatio56":0.0

- 5/6耦合比；double类型，范围[-1000,1000]

- "fiveAxisDirection":0.0

- 五轴方向；double类型，范围-90,0 度
- 0为五轴竖直向下，-90为五轴水平向右

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L4":120.0,
  "L5":120.0,
  "L6":120.0,
  "L7":120.0,
  "conversionRatio_X":100.0,
  "conversionRatio_Y":100.0,
  "conversionRatio_Z":100.0,
  "couplingRatio45":0.0,
  "couplingRatio56":0.0,
  "fiveAxisDirection":0.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 五轴混动机器人

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0
- L6杆长；double类型，范围[-4000,4000]
- "L7":120.0

- L7杆长；double类型，范围[-4000,4000]

- "L8":120.0

- L8杆长；double类型，范围[-4000,4000]

- "L9":0.0

- L9杆长；double类型，范围[-4000,4000]

- "L10":120.0

- L10杆长；double类型，范围[-4000,4000]

- "conversionratio_J1":100.0

- 1轴转换比；double类型，范围[-4000,4000]

- "conversionratio_J2":100.0

- 2轴转换比；double类型，范围[-4000,4000]

- "conversionratio_J3":100.0

- 3轴转换比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
    "L1":120.0,
    "L2":120.0,
    "L3":120.0,
    "L4":120.0,
    "L5":120.0,
    "L6":120.0,
    "L7":120.0,
    "L8":120.0,
    "L9":0.0,
    "L10":120.0,
    "conversionratio_J1":100.0,
    "conversionratio_J2":100.0,
    "conversionratio_J3":100.0,
    "mountAngle":false,
    "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 四轴SCARA异型2

- "L1":100.0
- 1轴螺距；double类型，范围[-1000,0),(0,1000]
- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "pitch":80.0

- 3轴螺距；double类型，范围[-1000,0),(0,1000]

- "robot":1

```
{
  "L1":100.0,
  "L2":120.0,
  "L3":120.0,
  "couplingRatio34":0.0,
  "mountAngle":false,
  "pitch":80.0,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 六轴异型三

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0
- L6杆长；double类型，范围[-4000,4000]
- "L7":120.0

- L7杆长；double类型，范围[-4000,4000]

- "L8":120.0

- L8杆长；double类型，范围[-4000,4000]

- "L9":120.0

- L9杆长；double类型，范围[-4000,4000]

- "L10":120.0

- L10杆长；double类型，范围[-4000,4000]

- "L11":120.0
- L11杆长；double类型，范围[-4000,4000]
- "L12":120.0

- L12杆长；double类型，范围[-4000,4000]

- "L13":120.0

- L13杆长；double类型，范围[-4000,4000]

- "L14":120.0

- L14杆长；double类型，范围[-4000,4000]

- "L15":120.0

- L15杆长；double类型，范围[-4000,4000]

- "L16":120.0
- L16杆长；double类型，范围[-4000,4000]
- "L17":120.0

- L17杆长；double类型，范围[-4000,4000]

- "L18":120.0

- L18杆长；double类型，范围[-4000,4000]

- "L19":120.0

- L19杆长；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":120.0,
  "L7":120.0,
  "L8":120.0,
  "L9":120.0,
  "L10":120.0,
  "L11":120.0,
  "L12":120.0,
  "L13":120.0,
  "L14":120.0,
  "L15":120.0,
  "L16":120.0,
  "L17":120.0,
  "L18":120.0,
  "L19":120.0,  
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 三轴SCARA异型一

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- delta2D并联机器人模型

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":110.0

- L2杆长；double类型，范围[-4000,4000]
- L2的值需要小于L3的值

- "L3":120.0
- L3杆长；double类型，范围[-4000,4000]
- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0
- L5杆长；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":110.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 龙门焊接3模型

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0
- L5杆长；double类型，范围[-4000,4000]
- "conversionRatio_X":100.0

- X轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Y":100.0

- Y轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Z":100.0

- Z轴转换比；double类型，范围[-4000,4000]

- "threeAxisDirection":90.0

- 四轴方向；double类型，范围0,90 度
- 四轴方向为0时，L4应填0

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L4":120.0,
  "L5":120.0,
  "conversionRatio_X":100.0,
  "conversionRatio_Y":100.0,
  "conversionRatio_Z":100.0,
  "mountAngle":false,
  "robot":1,
  "threeAxisDirection":90.0
}
```
- 当前机器人号；int类型，范围[1,4]

- 三轴串联异型一

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0
- L3杆长；double类型，范围[-4000,4000]
- "threeAxisDirection":90.0

- 三轴方向；double类型，范围0,90 度

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "mountAngle":false,
  "robot":1,
  "threeAxisDirection":90.0
}
```
- 当前机器人号；int类型，范围[1,4]

- 五轴协作机器人

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":-120.0

- L2杆长；double类型，范围[-4000,4000]
- L2请填负值

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":-120.0
- L6杆长；double类型，范围[-4000,4000]
- L6请填负值
- "L7":120.0

- L7杆长；double类型，范围[-4000,4000]

- "L8":120.0

- L8杆长；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":-120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":-120.0,
  "L7":120.0,
  "L8":120.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 四轴SCARA异型3

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0
- L3杆长；double类型，范围[-4000,4000]
- "L4":120.0
- L4杆长；double类型，范围[-4000,4000]
- "couplingRatio12":0.0

- 1/2耦合比；double类型，范围[-1000,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "pitch":80.0

- 螺距；double类型，范围[-1000,0),(0,1000]

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "couplingRatio12":0.0,
  "mountAngle":false,
  "pitch":80.0,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 六轴串联-CBBARA

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":-120.0

- L2杆长；double类型，范围[-4000,4000]
- L2请填负值

- "L3":120.0
- L3杆长；double类型，范围[-4000,4000]
- "L4":120.0
- L4杆长；double类型，范围[-4000,4000]
- "L5":120.0
- L5杆长；double类型，范围[-4000,4000]
- "L6":0.0

- L6杆长；double类型，范围[-4000,4000]

- "L7":0.0
- L7杆长；double类型，范围[-4000,4000]
- "L8":120.0
- L8杆长；double类型，范围[-4000,4000]
- "couplingRatio45":0.0

- 4/5耦合比；double类型，范围[-1000,1000]

- "couplingRatio46":0.0

- 4/6耦合比；double类型，范围[-1000,1000]

- "couplingRatio56":0.0

- 5/6耦合比；double类型，范围[-1000,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":-120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":0.0,
  "L7":0.0,
  "L8":120.0,
  "couplingRatio45":0.0,
  "couplingRatio46":0.0,
  "couplingRatio56":0.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 高格立柱旋转四轴

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "conversionRatio1":100.0

- 1轴转换比；double类型，范围[-4000,4000]

- "conversionRatio2":100.0

- 3轴转换比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

```
{
  "L1":120.0,
  "L2":120.0,
  "conversionRatio1":100.0,
  "conversionRatio2":100.0,
  "mountAngle":false,
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 上位机查询当前机器人DH参数

- 命令字：0x20C1

- "robot":1

```
{
  "robot":1
}
```
- 当前机器人号；int类型，取值范围[1,4]

- 控制器回复上位机当前机器人DH参数

- 命令字: 0x20C2

- 六轴串联机器人（存在耦合时动态限位生效）

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0

- L6杆长；double类型，范围[-4000,4000]

- "L7":0.0

- L7杆长；double类型，范围[-4000,4000]

- "L8":0.0

- L8杆长；double类型，范围[-4000,4000]

- "couplingRatio12":0.0

- 1/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "couplingRatio32":0.0

- 3/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "couplingRatio45":0.0

- 4/5耦合比；double类型，范围[-1000,1000]

- "couplingRatio46":0.0

- 4/6耦合比；double类型，范围[-1000,1000]

- "couplingRatio56":0.0

- 5/6耦合比；double类型，范围[-1000,1000]

- "fiveAxisDirection":90.0

- 五轴方向；double类型，范围0,90 度

- "dynamicLimit":

- J2+J3范围限制
- "max":0.0

- J2+J3最大值；double类型，范围[-500,500]

- "min":0.0

- J2+J3最小值；double类型，范围[-500,500]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数

- "angleToDistanceSync":[27.775,27.775,1.0]

- 机器人外部轴角度转距离列表；double类型
- 长度为当前机器人外部轴的总轴数，没有外部轴时该节点不存在
- 旋转轴值都为1，直线轴公式为：1 * 轴方向转换比 / 360

- "distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数

- "distanceToAngleSync":[0.03600360036,0.03600360036,1.0]

- 机器人外部轴距离转角度列表；double类型
- 长度为当前机器人外部轴的总轴数，没有外部轴时该节点不存在
- 旋转轴值都为1，直线轴公式为：1 / 轴方向转换比 * 360

- "robotType":1

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":120.0,
  "L7":0.0,
  "L8":0.0,
  "couplingRatio12":0.0,
  "couplingRatio23":0.0,
  "couplingRatio32":0.0,
  "couplingRatio34":0.0,
  "couplingRatio45":0.0,
  "couplingRatio46":0.0,
  "couplingRatio56":0.0,
  "dynamicLimit":
  {
    "max":0.0,
    "min":0.0
  },
  "fiveAxisDirection":90.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0],
  "angleToDistanceSync":[27.775,27.775,1.0],
  "distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0],
  "distanceToAngleSync":[0.03600360036,0.03600360036,1.0],
  "robotType":1
}    
```
- 当前机器人类型；int类型

- 六轴协作机器人

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0

- L6杆长；double类型，范围[-4000,4000]

- "L7":0.0

- L7杆长；double类型，范围[-4000,4000]

- "couplingRatio12":0.0

- 1/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "couplingRatio32":0.0

- 3/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "couplingRatio45":0.0

- 4/5耦合比；double类型，范围[-1000,1000]

- "couplingRatio46":0.0

- 4/6耦合比；double类型，范围[-1000,1000]

- "couplingRatio56":0.0

- 5/6耦合比；double类型，范围[-1000,1000]

- "threeAxisDirection":-90.0

- 三轴方向；double类型，范围-90,0 度

- "fiveAxisDirection":90.0

- 五轴方向；double类型，范围0,90 度

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数

- "distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数

- "robotType":7

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":120.0,
  "L7":120.0,
  "couplingRatio12":0.0,
  "couplingRatio23":0.0,
  "couplingRatio32":0.0,
  "couplingRatio34":0.0,
  "couplingRatio45":0.0,
  "couplingRatio46":0.0,
  "couplingRatio56":0.0,
  "fiveAxisDirection":90.0,
  "mountAngle":false,
  "robot":1,
  "threeAxisDirection":-90.0,
  "angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0],
  "distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0],
  "robotType":7
}
```
- 当前机器人类型；int类型

- 六轴喷涂机器人

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":0.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0

- L6杆长；double类型，范围[-4000,4000]

- "L7":0.0

- L7杆长；double类型，范围[-4000,4000]

- "L8":0.0

- L7杆长；double类型，范围[-4000,4000]

- "couplingRatio12":0.0

- 1/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "couplingRatio32":0.0

- 3/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "couplingRatio45":0.0

- 4/5耦合比；double类型，范围[-1000,1000]

- "couplingRatio46":0.0

- 4/6耦合比；double类型，范围[-1000,1000]

- "couplingRatio56":0.0

- 5/6耦合比；double类型，范围[-1000,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数

- "distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数

- "robotType":15

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":0.0,
  "L4":120.0,
  "L5":120.0,
  "L6":120.0,
  "L7":0.0,
  "L8":0.0,
  "couplingRatio12":0.0,
  "couplingRatio23":0.0,
  "couplingRatio32":0.0,
  "couplingRatio34":0.0,
  "couplingRatio45":0.0,
  "couplingRatio46":0.0,
  "couplingRatio56":0.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0],
  "distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0],
  "robotType":15
}
```
- 当前机器人类型；int类型

- 六轴异型二

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0

- L6杆长；double类型，范围[-4000,4000]

- "couplingRatio12":0.0

- 1/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "couplingRatio32":0.0

- 3/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "couplingRatio45":0.0

- 4/5耦合比；double类型，范围[-1000,1000]

- "couplingRatio46":0.0

- 4/6耦合比；double类型，范围[-1000,1000]

- "couplingRatio56":0.0

- 5/6耦合比；double类型，范围[-1000,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数

- "distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数

- "robotType":18

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":120.0,
  "couplingRatio12":0.0,
  "couplingRatio23":0.0,
  "couplingRatio32":0.0,
  "couplingRatio34":0.0,
  "couplingRatio45":0.0,
  "couplingRatio46":0.0,
  "couplingRatio56":0.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0],
  "distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0],
  "robotType":18
}
```
- 当前机器人类型；int类型

- 五轴串联多关节

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0

- L6杆长；double类型，范围[-4000,4000]

- "L7":0.0

- L7杆长；double类型，范围[-4000,4000]

- "couplingRatio12":0.0

- 1/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "couplingRatio32":0.0

- 3/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "couplingRatio45":0.0

- 4/5耦合比；double类型，范围[-1000,1000]

- "couplingRatio46":0.0

- 4/6耦合比；double类型，范围[-1000,1000]

- "fiveAxisDirection":90.0

- 五轴方向；double类型，范围0,90 度

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0,1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数

- "distanceToAngle":[1.0,1.0,1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数

- "robotType":6

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":120.0,
  "L7":0.0,
  "couplingRatio12":0.0,
  "couplingRatio23":0.0,
  "couplingRatio32":0.0,
  "couplingRatio34":0.0,
  "couplingRatio45":0.0,
  "couplingRatio46":0.0,
  "fiveAxisDirection":90.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[1.0,1.0,1.0,1.0,1.0],
  "distanceToAngle":[1.0,1.0,1.0,1.0,1.0],
  "robotType":6
}
```
- 当前机器人类型；int类型

- 四轴SCARA

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "couplingRatio12":0.0

- 1/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "pitch":80.0

- 螺距；double类型，范围[-1000,0),(0,1000]

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0,0.222222222222,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第三位公式：1 * 螺距 / 360

- "distanceToAngle":[1.0,1.0,4.5,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第三位公式：1 / 螺距 * 360

- "robotType":2

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "couplingRatio12":0.0,
  "couplingRatio23":0.0,
  "couplingRatio34":0.0,
  "mountAngle":false,
  "pitch":80.0,
  "robot":1,
  "angleToDistance":[1.0,1.0,0.222222222222,1.0],
  "distanceToAngle":[1.0,1.0,4.5,1.0],
  "robotType":2
}
```
- 当前机器人类型；int类型

- 四轴SCARA异型1

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "pitch":80.0

- 螺距；double类型，范围[-1000,0),(0,1000]

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[0.222222222222,1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 * 螺距 / 360

- "distanceToAngle":[4.5,1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 / 螺距 * 360

- "robotType":13

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "couplingRatio34":0.0,
  "mountAngle":false,
  "pitch":80.0,
  "robot":1,
  "angleToDistance":[0.222222222222,1.0,1.0,1.0],
  "distanceToAngle":[4.5,1.0,1.0,1.0],
  "robotType":13
}
```
- 当前机器人类型；int类型

- 四轴连杆码垛

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":0.0

- 偏置值；double类型，范围[-4000,4000]
- 默认为0

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "maxDynamicLimit":0.0
- J2+J3最大值；double类型，范围[-1000,1000]

- "minDynamicLimit":0.0

- J2+J3最小值；double类型，范围[-1000,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数

- "distanceToAngle":[1.0,1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数

- "robotType":3

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":0.0,
  "couplingRatio23":0.0,
  "couplingRatio34":0.0,
  "maxDynamicLimit":0.0,
  "minDynamicLimit":0.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[1.0,1.0,1.0,1.0],
  "distanceToAngle":[1.0,1.0,1.0,1.0],
  "robotType":3
}
```
- 当前机器人类型；int类型

- 四轴码垛丝杆

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "amplificationRatio":100.0

- 放大比；double类型，范围[1,1000]

- "conversionRatio2":100.0

- 二轴转换比；double类型，范围[1,1000]

- "conversionRatio3":100.0

- 三轴转换比；double类型，范围[1,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,0.277777777778,0.277777777778,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第二位公式：1 * 二轴转换比 / 360
- 第三位公式：1 * 三轴转换比 / 360

- "distanceToAngle":[1.0,3.6,3.6,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第二位公式：1 / 二轴转换比 * 360
- 第三位公式：1 / 三轴转换比 * 360

- "robotType":14

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "amplificationRatio":100.0,
  "conversionRatio2":100.0,
  "conversionRatio3":100.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[1.0,0.277777777778,0.277777777778,1.0],
  "distanceToAngle":[1.0,3.6,3.6,1.0],
  "robotType":14
}
```
- 当前机器人类型；int类型

- 四轴串联多关节

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数

- "distanceToAngle":[1.0,1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数

- "robotType":4

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "couplingRatio23":0.0,
  "couplingRatio34":0.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[1.0,1.0,1.0,1.0],
  "distanceToAngle":[1.0,1.0,1.0,1.0],
  "robotType":4
}
```
- 当前机器人类型；int类型

- 四轴直角机器人

- "conversionRatio_X":100.0

- X轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Y":100.0

- Y轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Z":100.0

- Z轴转换比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[0.277777777778,0.277777777778,0.277777777778,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 * X轴转换比 / 360
- 第二位公式：1 * Y轴转换比 / 360
- 第三位公式：1 * Z轴转换比 / 360

- "distanceToAngle":[3.6,3.6,3.6,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 / X轴转换比 * 360
- 第二位公式：1 / Y轴转换比 * 360
- 第三位公式：1 / Z轴转换比 * 360

- "robotType":16

```
{
  "conversionRatio_X":100.0,
  "conversionRatio_Y":100.0,
  "conversionRatio_Z":100.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[0.277777777778,0.277777777778,0.277777777778,1.0],
  "distanceToAngle":[3.6,3.6,3.6,1.0],
  "robotType":16
}
```
- 当前机器人类型；int类型

- 四轴极坐标异型

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "conversionRatio2":100.0

- 二轴转换比；double类型，范围[-4000,4000]

- "conversionRatio3":90.0

- 三轴转换比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,0.277777777778,0.25,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第二位公式：1 * 二轴转换比 / 360
- 第三位公式：1 * 三轴转换比 / 360

- "distanceToAngle":[1.0,3.6,4.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第二位公式：1 / 二轴转换比 * 360
- 第三位公式：1 / 三轴转换比 * 360

- "robotType":17

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "conversionRatio2":100.0,
  "conversionRatio3":90.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[1.0,0.277777777778,0.25,1.0],
  "distanceToAngle":[1.0,3.6,4.0,1.0],
  "robotType":17
}
```
- 当前机器人类型；int类型

- 三轴SCARA

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "couplingRatio12":0.0

- 1/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "pitch":80.0

- 螺距；double类型，范围[-1000,0),(0,1000]

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0,0.222222222222]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第三位公式：1 * 螺距 / 360

- "distanceToAngle":[1.0,1.0,4.5]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第三位公式：1 / 螺距 * 360

- "robotType":9

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "couplingRatio12":0.0,
  "couplingRatio23":0.0,
  "mountAngle":false,
  "pitch":80.0,
  "robot":1,
  "angleToDistance":[1.0,1.0,0.222222222222],
  "distanceToAngle":[1.0,1.0,4.5],
  "robotType":9
}
```
- 当前机器人类型；int类型

- 三轴直角机器人

- "conversionRatio_X":100.0

- X轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Y":90.0

- Y轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Z":80.0

- Z轴转换比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[0.277777777778,0.25,0.222222222222]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 * X轴转换比 / 360
- 第二位公式：1 * Y轴转换比 / 360
- 第三位公式：1 * Z轴转换比 / 360

- "distanceToAngle":[3.6,4.0,4.5]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 / X轴转换比 * 360
- 第二位公式：1 / Y轴转换比 * 360
- 第三位公式：1 / Z轴转换比 * 360

- "robotType":10

```
{
  "conversionRatio_X":100.0,
  "conversionRatio_Y":90.0,
  "conversionRatio_Z":80.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[0.277777777778,0.25,0.222222222222],
  "distanceToAngle":[3.6,4.0,4.5],
  "robotType":10
}
```
- 当前机器人类型；int类型

- 三轴直角异型1

- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "conversionRatio2":100.0

- 二轴转换比；double类型，范围[-4000,4000]

- "conversionRatio3":90.0

- 三轴转换比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,0.277777777778,0.25]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第二位公式：1 * 二轴转换比 / 360
- 第三位公式：1 * 三轴转换比 / 360

- "distanceToAngle":[1.0,3.6,4.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第二位公式：1 / 二轴转换比 * 360
- 第三位公式：1 / 三轴转换比 * 360

- "robotType":11

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "conversionRatio2":100.0,
  "conversionRatio3":100.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[1.0,0.277777777778,0.25],
  "distanceToAngle":[1.0,3.6,4.0],
  "robotType":11
}
```
- 当前机器人类型；int类型

- 二轴SCARA

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数

- "distanceToAngle":[1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数

- "robotType":8

```
{
  "L2":120.0,
  "L3":120.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[1.0,1.0],
  "distanceToAngle":[1.0,1.0],
  "robotType":8
}
```
- 当前机器人类型；int类型

- 七轴串联多关节

- "Link":

- DH参数列表
- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0

- L6杆长；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数

- "distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数

- "robotType":12

```
{
  "Link":
  {
    "L1":120.0,
    "L2":120.0,
    "L3":120.0,
    "L4":120.0,
    "L5":120.0,
    "L6":120.0
  },
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0,1.0],
  "distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0,1.0],
  "robotType":12
}
```
- 当前机器人类型；int类型

- 龙门焊接模型

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "conversionRatio_X":100.0

- X轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Y":90.0

- Y轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Z":80.0

- Z轴转换比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[0.277777777778,0.25,0.222222222222,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 * X轴转换比 / 360
- 第二位公式：1 * Y轴转换比 / 360
- 第三位公式：1 * Z轴转换比 / 360

- "distanceToAngle":[3.6,4.0,4.5,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 / X轴转换比 * 360
- 第二位公式：1 / Y轴转换比 * 360
- 第三位公式：1 / Z轴转换比 * 360

- "robotType":19

```
{
  "L4":120.0,
  "L5":120.0,
  "conversionRatio_X":100.0,
  "conversionRatio_Y":90.0,
  "conversionRatio_Z":80.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[0.277777777778,0.25,0.222222222222,1.0,1.0],
  "distanceToAngle":[3.6,4.0,4.5,1.0,1.0],
  "robotType":19
}
```
- 当前机器人类型；int类型

- 四轴并联机器人

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":110.0

- L2杆长；double类型，范围[-4000,4000]
- L2的值需要小于L3的值

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数

- "distanceToAngle":[1.0,1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数

- "robotType":20

```
{
  "L1":120.0,
  "L2":110.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[1.0,1.0,1.0,1.0],
  "distanceToAngle":[1.0,1.0,1.0,1.0],
  "robotType":20
}
```
- 当前机器人类型；int类型

- 酒槽机型

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0
- L6杆长；double类型，范围[-4000,4000]
- "L7":120.0

- L7杆长；double类型，范围[-4000,4000]

- "L8":120.0

- L8杆长；double类型，范围[-4000,4000]

- "L9":120.0

- L9杆长；double类型，范围[-4000,4000]

- "L10":120.0

- L10杆长；double类型，范围[-4000,4000]

- "L11":120.0
- L11杆长；double类型，范围[-4000,4000]
- "L12":100.0

- 滑动电动缸导程；double类型，范围[-4000,4000]

- "L13":90.0

- 顶升电动缸导程；double类型，范围[-4000,4000]

- "L14":120.0

- 喷料距离；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[0.277777777778,0.25,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 * 滑动电动缸导程 / 360
- 第二位公式：1 * 顶升电动缸导程 / 360

- "distanceToAngle":[3.6,4.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 / 滑动电动缸导程 * 360
- 第二位公式：1 / 顶升电动缸导程 * 360

- "robotType":21

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":120.0,
  "L7":120.0,
  "L8":120.0,
  "L9":120.0,
  "L10":120.0,
  "L11":120.0,
  "L12":100.0,
  "L13":90.0,
  "L14":120.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[0.277777777778,0.25,1.0,1.0],
  "distanceToAngle":[3.6,4.0,1.0,1.0],
  "robotType":21
}  
```
- 当前机器人类型；int类型

- 龙门焊接2模型

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "conversionRatio_X":100.0

- X轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Y":100.0

- Y轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Z":100.0

- Z轴转换比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[0.277777777778,0.25,0.222222222222,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 * X轴转换比 / 360
- 第二位公式：1 * Y轴转换比 / 360
- 第三位公式：1 * Z轴转换比 / 360

- "distanceToAngle":[3.6,4.0,4.5,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 / X轴转换比 * 360
- 第二位公式：1 / Y轴转换比 * 360
- 第三位公式：1 / Z轴转换比 * 360

- "robotType":22

```
{
  "L4":120.0,
  "L5":120.0,
  "conversionRatio_X":100.0,
  "conversionRatio_Y":90.0,
  "conversionRatio_Z":80.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[0.277777777778,0.25,0.222222222222,1.0,1.0],
  "distanceToAngle":[3.6,4.0,4.5,1.0,1.0],
  "robotType":22
}
```
- 当前机器人类型；int类型

- 四轴直角异型一

- "Link":

- DH参数列表
- "L1":120.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "conversionRatio":[100.0,90.0]

- 轴转换比；double类型，范围[1,1000]
- 长度为2，第一个值为一轴转换比，第二个轴为四轴转换比

- "upsideDown":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[0.277777777778,1.0,1.0,0.25]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 * 一轴转换比 / 360
- 第四位公式：1 * 四轴转换比 / 360

- "distanceToAngle":[3.6,1.0,1.0,4.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 / 一轴转换比 * 360
- 第四位公式：1 / 四轴转换比 * 360

- "robotType":23

```
{
  "Link":
  {
    "L1":120.0,
    "L2":120.0,
    "conversionRatio":[100.0,90.0]
  },  
  "upsideDown":false,
  "robot":1,
  "angleToDistance":[0.277777777778,1.0,1.0,0.25],
  "distanceToAngle":[3.6,1.0,1.0,4.0],
  "robotType":23
}
```
- 当前机器人类型；int类型

- 六轴龙门焊接模型

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0

- L6杆长；double类型，范围[-4000,4000]

- "L7":120.0

- L7杆长；double类型，范围[-4000,4000]

- "conversionRatio_X":100.0

- X轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Y":90.0

- Y轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Z":80.0

- Z轴转换比；double类型，范围[-4000,4000]

- "couplingRatio45":0.0

- 4/5耦合比；double类型，范围[-1000,1000]

- "couplingRatio56":0.0

- 5/6耦合比；double类型，范围[-1000,1000]

- "fiveAxisDirection":0.0

- 五轴方向；double类型，范围-90,0 度
- 0为五轴竖直向下，-90为五轴水平向右

- "upsideDown":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[0.277777777778,0.25,0.222222222222,1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 * X轴转换比 / 360
- 第二位公式：1 * Y轴转换比 / 360
- 第三位公式：1 * Z轴转换比 / 360

- "distanceToAngle":[3.6,4.0,4.5,1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 / X轴转换比 * 360
- 第二位公式：1 / Y轴转换比 * 360
- 第三位公式：1 / Z轴转换比 * 360

- "robotType":24

```
{
  "L4":120.0,
  "L5":120.0,
  "L6":120.0,
  "L7":120.0,
  "conversionRatio_X":100.0,
  "conversionRatio_Y":90.0,
  "conversionRatio_Z":80.0,
  "couplingRatio45":0.0,
  "couplingRatio56":0.0,
  "fiveAxisDirection":0.0,
  "upsideDown":false,
  "robot":1,
  "angleToDistance":[0.277777777778,0.25,0.222222222222,1.0,1.0,1.0],
  "distanceToAngle":[3.6,4.0,4.5,1.0,1.0,1.0],
  "robotType":24
}
```
- 当前机器人类型；int类型

- 五轴混动机器人

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0
- L6杆长；double类型，范围[-4000,4000]
- "L7":120.0

- L7杆长；double类型，范围[-4000,4000]

- "L8":120.0

- L8杆长；double类型，范围[-4000,4000]

- "L9":0.0

- L9杆长；double类型，范围[-4000,4000]

- "L10":120.0

- L10杆长；double类型，范围[-4000,4000]

- "conversionratio_J1":100.0

- 1轴转换比；double类型，范围[-4000,4000]

- "conversionratio_J2":90.0

- 2轴转换比；double类型，范围[-4000,4000]

- "conversionratio_J3":80.0

- 3轴转换比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[0.277777777778,0.25,0.222222222222,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 * 一轴转换比 / 360
- 第二位公式：1 * 二轴转换比 / 360
- 第三位公式：1 * 三轴转换比 / 360

- "distanceToAngle":[3.6,4.0,4.5,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 / 一轴转换比 * 360
- 第二位公式：1 / 二轴转换比 * 360
- 第三位公式：1 / 三轴转换比 * 360

- "robotType":25

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":120.0,
  "L7":120.0,
  "L8":120.0,
  "L9":0.0,
  "L10":120.0,
  "conversionratio_J1":100.0,
  "conversionratio_J2":90.0,
  "conversionratio_J3":80.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[0.277777777778,0.25,0.222222222222,1.0,1.0],
  "distanceToAngle":[3.6,4.0,4.5,1.0,1.0],
  "robotType":25
}
```
- 当前机器人类型；int类型

- 四轴SCARA异型2

- "L1":100.0
- 1轴螺距；double类型，范围[-1000,0),(0,1000]
- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "pitch":80.0

- 3轴螺距；double类型，范围[-1000,0),(0,1000]

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[0.277777777778,1.0,0.222222222222,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 * 一轴螺距 / 360
- 第三位公式：1 * 三轴螺距 / 360

- "distanceToAngle":[3.6,1.0,4.5,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 / 一轴螺距 * 360
- 第三位公式：1 / 三轴螺距* 360

- "robotType":26

```
{
  "L1":100.0,
  "L2":120.0,
  "L3":120.0,
  "couplingRatio34":0.0,
  "mountAngle":false,
  "pitch":80.0,
  "robot":1,
  "angleToDistance":[0.277777777778,1.0,0.222222222222,1.0],
  "distanceToAngle":[3.6,1.0,4.5,1.0],
  "robotType":26
}
```
- 当前机器人类型；int类型

- 六轴异型三

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":120.0
- L6杆长；double类型，范围[-4000,4000]
- "L7":120.0

- L7杆长；double类型，范围[-4000,4000]

- "L8":120.0

- L8杆长；double类型，范围[-4000,4000]

- "L9":120.0

- L9杆长；double类型，范围[-4000,4000]

- "L10":120.0

- L10杆长；double类型，范围[-4000,4000]

- "L11":120.0
- L11杆长；double类型，范围[-4000,4000]
- "L12":120.0

- L12杆长；double类型，范围[-4000,4000]

- "L13":120.0

- L13杆长；double类型，范围[-4000,4000]

- "L14":120.0

- L14杆长；double类型，范围[-4000,4000]

- "L15":120.0

- L15杆长；double类型，范围[-4000,4000]

- "L16":120.0
- L16杆长；double类型，范围[-4000,4000]
- "L17":120.0

- L17杆长；double类型，范围[-4000,4000]

- "L18":120.0

- L18杆长；double类型，范围[-4000,4000]

- "L19":120.0

- L19杆长；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数

- "distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数

- "robotType":27

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":120.0,
  "L7":120.0,
  "L8":120.0,
  "L9":120.0,
  "L10":120.0,
  "L11":120.0,
  "L12":120.0,
  "L13":120.0,
  "L14":120.0,
  "L15":120.0,
  "L16":120.0,
  "L17":120.0,
  "L18":120.0,
  "L19":120.0,  
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0],
  "distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0],
  "robotType":27
}
```
- 当前机器人类型；int类型

- 三轴SCARA异型一

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数

- "distanceToAngle":[1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数

- "robotType":28

```
{
  "L1":120.0,
  "L2":120.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[1.0,1.0,1.0],
  "distanceToAngle":[1.0,1.0,1.0],
  "robotType":28
}
```
- 当前机器人类型；int类型

- delta2D并联机器人模型

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":110.0

- L2杆长；double类型，范围[-4000,4000]
- L2的值需要小于L3的值

- "L3":120.0
- L3杆长；double类型，范围[-4000,4000]
- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0
- L5杆长；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数

- "distanceToAngle":[1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数

- "robotType":29

```
{
  "L1":120.0,
  "L2":110.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[1.0,1.0,1.0],
  "distanceToAngle":[1.0,1.0,1.0],
  "robotType":29
}
```
- 当前机器人类型；int类型

- 龙门焊接3模型

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0
- L5杆长；double类型，范围[-4000,4000]
- "conversionRatio_X":100.0

- X轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Y":90.0

- Y轴转换比；double类型，范围[-4000,4000]

- "conversionRatio_Z":80.0

- Z轴转换比；double类型，范围[-4000,4000]

- "threeAxisDirection":90.0

- 四轴方向；double类型，范围0,90 度
- 四轴方向为0时，L4应填0

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[0.277777777778,0.25,0.222222222222,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 * X轴转换比 / 360
- 第二位公式：1 * Y轴转换比 / 360
- 第三位公式：1 * Z轴转换比 / 360

- "distanceToAngle":[3.6,4.0,4.5,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 / X轴转换比 * 360
- 第二位公式：1 / Y轴转换比 * 360
- 第三位公式：1 / Z轴转换比 * 360

- "robotType":30

```
{
  "L4":120.0,
  "L5":120.0,
  "conversionRatio_X":100.0,
  "conversionRatio_Y":90.0,
  "conversionRatio_Z":80.0,
  "mountAngle":false,
  "robot":1,
  "threeAxisDirection":90.0,
  "angleToDistance":[0.277777777778,0.25,0.222222222222,1.0,1.0],
  "distanceToAngle":[3.6,4.0,4.5,1.0,1.0],
  "robotType":30
}
```
- 当前机器人类型；int类型

- 三轴串联异型一

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0
- L3杆长；double类型，范围[-4000,4000]
- "threeAxisDirection":90.0

- 三轴方向；double类型，范围0,90 度

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数

- "distanceToAngle":[1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数

- "robotType":31

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "mountAngle":false,
  "robot":1,
  "threeAxisDirection":90.0,
  "angleToDistance":[1.0,1.0,1.0],
  "distanceToAngle":[1.0,1.0,1.0],
  "robotType":31
}
```
- 当前机器人类型；int类型

- 五轴协作机器人

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":-120.0

- L2杆长；double类型，范围[-4000,4000]
- L2请填负值

- "L3":120.0

- L3杆长；double类型，范围[-4000,4000]

- "L4":120.0

- L4杆长；double类型，范围[-4000,4000]

- "L5":120.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":-120.0
- L6杆长；double类型，范围[-4000,4000]
- L6请填负值
- "L7":120.0

- L7杆长；double类型，范围[-4000,4000]

- "L8":120.0

- L8杆长；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0,1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数

- "distanceToAngle":[1.0,1.0,1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数

- "robotType":32

```
{
  "L1":120.0,
  "L2":-120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":-120.0,
  "L7":120.0,
  "L8":120.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[1.0,1.0,1.0,1.0,1.0],
  "distanceToAngle":[1.0,1.0,1.0,1.0,1.0],
  "robotType":32
}
```
- 当前机器人类型；int类型

- 四轴SCARA异型3

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "L3":120.0
- L3杆长；double类型，范围[-4000,4000]
- "L4":120.0
- L4杆长；double类型，范围[-4000,4000]
- "couplingRatio12":0.0

- 1/2耦合比；double类型，范围[-1000,1000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "pitch":80.0

- 螺距；double类型，范围[-1000,0),(0,1000]

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[0.222222222222,1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 * 螺距 / 360

- "distanceToAngle":[4.5,1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 / 螺距 * 360

- "robotType":33

```
{
  "L1":120.0,
  "L2":120.0,
  "L3":120.0,
  "L4":120.0,
  "couplingRatio12":0.0,
  "mountAngle":false,
  "pitch":80.0,
  "robot":1,
  "angleToDistance":[0.222222222222,1.0,1.0,1.0],
  "distanceToAngle":[4.5,1.0,1.0,1.0],
  "robotType":33
}
```
- 当前机器人类型；int类型

- 六轴串联-CBBARA

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":-120.0

- L2杆长；double类型，范围[-4000,4000]
- L2请填负值

- "L3":120.0
- L3杆长；double类型，范围[-4000,4000]
- "L4":120.0
- L4杆长；double类型，范围[-4000,4000]
- "L5":120.0
- L5杆长；double类型，范围[-4000,4000]
- "L6":0.0

- L6杆长；double类型，范围[-4000,4000]

- "L7":0.0
- L7杆长；double类型，范围[-4000,4000]
- "L8":120.0
- L8杆长；double类型，范围[-4000,4000]
- "couplingRatio45":0.0

- 4/5耦合比；double类型，范围[-1000,1000]

- "couplingRatio46":0.0

- 4/6耦合比；double类型，范围[-1000,1000]

- "couplingRatio56":0.0

- 5/6耦合比；double类型，范围[-1000,1000]

- "upsideDown":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数

- "distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数

- "robotType":34

```
{
  "L1":120.0,
  "L2":-120.0,
  "L3":120.0,
  "L4":120.0,
  "L5":120.0,
  "L6":0.0,
  "L7":0.0,
  "L8":120.0,
  "couplingRatio45":0.0,
  "couplingRatio46":0.0,
  "couplingRatio56":0.0,
  "upsideDown":false,
  "robot":1,
  "angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0],
  "distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0],
  "robotType":34
}
```
- 当前机器人类型；int类型

- 高格立柱旋转四轴

- "L1":120.0
- L1杆长；double类型，范围[-4000,4000]
- "L2":120.0

- L2杆长；double类型，范围[-4000,4000]

- "conversionRatio1":100.0

- 1轴转换比；double类型，范围[-4000,4000]

- "conversionRatio2":100.0

- 3轴转换比；double类型，范围[-4000,4000]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "angleToDistance":[0.277777777778,1.0,0.25,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 * 一轴转换比 / 360
- 第三位公式：1 * 三轴转换比 / 360

- "distanceToAngle":[3.6,1.0,4.0,1.0]

- 机器人距离转角度列表；double类型
- 长度为当前机器人的轴数
- 第一位公式：1 / 一轴转换比 * 360
- 第三位公式：1 / 三轴转换比 * 360

- "robotType":35

```
{
  "L1":120.0,
  "L2":120.0,
  "conversionRatio1":100.0,
  "conversionRatio2":100.0,
  "mountAngle":false,
  "robot":1,
  "angleToDistance":[0.277777777778,1.0,0.25,1.0],
  "distanceToAngle":[3.6,1.0,4.0,1.0],
  "robotType":35
}
```
- 当前机器人类型；int类型

- 上位机请求保存预置机器人参数

- 命令字：0x20C3

- "name":"AAA"

```
{
  "name":"AAA"
}
```
- 预置机器人自定义保存名称；string类型
- 预置文件格式：当前机器人类型+"_"+自定义保存名称

- 控制器回复上位机保存预置机器人参数结果

```
{}
```
- 命令字：0x20C4

- 上位机发送设置机器人关节参数

- 命令字：0x20C5

- "axis":1

- 机器人轴编号；int 类型，范围[1,7]

- "axisDirection":1

- 关节实际方向；int 类型，范围-1,1

- "backLash":0.0

- 齿轮反向间隙；double 类型，范围[0,9999.999]

- "direction":-1.0

- 模型方向；int 类型，范围-1,1

- "encoderResolution":17

- 编码器位数；int 类型，范围[1,100]

- "isReduceRatioEnable":true

- 编码器是否经过减速机；bool 类型

- "maxAcc":6.0

- 最大加速度；double 类型，范围[1,10000]

- "maxDec":-6.0

- 最大减速度；double 类型，范围[-10000,-1]

- "maxJerkAcc":1.0

- 最大加加速度；double 类型，范围[1,20000]
- 机器人插补方式为加加速度时生效

- "maxJerkDec":-1.0

- 最大减减速度；double类型，范围[-20000,-1]
- 机器人插补方式为加加速度时生效

- "maxRPM":1.0

- 最大正转速；double 类型，范围[1,5]

- "maxReverseRPM":-1.0

- 最大反转速；double 类型，范围[-5,-1]

- "positiveLimit":160.0

- 关节正限位；double 类型，范围[1,3000]°

- "ratedRPM":3600.0

- 额定正转速；double 类型，范围[1,10000]rpm

- "ratedReverseRPM":-3600.0

- 额定反转速；double 类型，范围[-10000,-1]rpm
- 数值为额定正速度的负值

- "ratedReverseSpeed":-270.0540

- 额定反速度；double 类型，单位°/s
- 公式为 额定反速度 = 额定反速度 / 减速比 * 6 * 角度转距离值

- "ratedSpeed":270.0540

- 额定正速度；double 类型，单位°/s
- 公式为 额定正速度 = 额定正速度 / 减速比 * 6 * 角度转距离值

- "reducRatio":79.9840

- 减速比；double 类型，范围(0,1000]

- "reverseLimit":-160.0

- 关节反限位；double 类型，范围[-3000,-1]°

- "robot": 1

```
{
  "axis":1,
  "axisDirection":1,
  "backLash":0.0,
  "direction":-1.0,
  "encoderResolution":17,
  "isReduceRatioEnable":true,
  "maxAcc":6.0,
  "maxDec":-6.0,
  "maxJerkAcc":1.0,
  "maxJerkDec":-1.0,
  "maxRPM":1.0,
  "maxReverseRPM":-1.0,
  "positiveLimit":160.0,
  "ratedRPM":3600.0,
  "ratedReverseRPM":-3600.0,
  "ratedReverseSpeed":-270.0540,
  "ratedSpeed":270.0540,
  "reducRatio":79.9840,
  "reverseLimit":-160.0,
  "robot":1
}
```
- 当前机器人；int 类型，范围[1,4]

- 上位机查询机器人关节参数

- 命令字：0x20C6

- "axis":1

```
{
  "axis":1
}
```
- 机器人轴编号；int 类型，范围[1,7]

- 控制器回复上位机机器人关节参数

- 命令字：0x20C7

- "axis":1

- 机器人轴编号；int 类型，范围[1,7]

- "axisDirection":1

- 关节实际方向；int 类型，范围-1,1

- "backLash":0.0

- 齿轮反向间隙；double 类型，范围[0,9999.999]

- "direction":-1.0

- 模型方向；int 类型，范围-1,1

- "encoderResolution":17

- 编码器位数；int 类型，范围[1,100]

- "isReduceRatioEnable":true

- 编码器是否经过减速机；bool 类型

- "maxAcc":6.0

- 最大加速度；double 类型，范围[1,10000]

- "maxDec":-6.0

- 最大减速度；double 类型，范围[-10000,-1]

- "maxJerkAcc":1.0

- 最大加加速度；double 类型，范围[1,20000]
- 机器人插补方式为加加速度时生效

- "maxJerkDec":-1.0

- 最大减减速度；double类型，范围[-20000,-1]
- 机器人插补方式为加加速度时生效

- "maxRPM":1.0

- 最大正转速；double 类型，范围[1,5]

- "maxReverseRPM":-1.0

- 最大反转速；double 类型，范围[-5,-1]

- "positiveLimit":160.0

- 关节正限位；double 类型，范围[1,3000]°

- "ratedRPM":3600.0

- 额定正转速；double 类型，范围[1,10000]rpm

- "ratedReverseRPM":-3600.0

- 额定反转速；double 类型，范围[-10000,-1]rpm
- 数值为额定正速度的负值

- "ratedReverseSpeed":-270.0540

- 额定反速度；double 类型，单位°/s
- 公式为 额定反速度 = 额定反速度 / 减速比 * 6 * 角度转距离值

- "ratedSpeed":270.0540

- 额定正速度；double 类型，单位°/s
- 公式为 额定正速度 = 额定正速度 / 减速比 * 6 * 角度转距离值

- "reducRatio":79.9840

- 减速比；double 类型，范围(0,1000]

- "reverseLimit":-160.0

- 关节反限位；double 类型，范围[-3000,-1]°

- "robot": 1

```
{
  "axis":1,
  "axisDirection":1,
  "backLash":0.0,
  "direction":-1,
  "encoderResolution":17,
  "isReduceRatioEnable":true,
  "maxAcc":6.0,
  "maxDec":-6.0,
  "maxJerkAcc":1.0,
  "maxJerkDec":-1.0,
  "maxRPM":1.0,
  "maxReverseRPM":-1.0,
  "positiveLimit":160.0,
  "ratedRPM":3600.0,
  "ratedReverseRPM":-3600.0,
  "ratedReverseSpeed":-270.05401080216,
  "ratedSpeed":270.05401080216,
  "reducRatio":79.984,
  "reverseLimit":-160.0,
  "robot":1
}
```
- 当前机器人；int 类型，范围[1,4]

- 上位机发送设置机器人笛卡尔参数

- 命令字：0x20C8

- "maxAcc":7.50

- 最大加速度；double类型，范围[1,10000]

- "maxAttitudeVel":500.0

- 姿态运动最大速度；double 类型，范围[1,1000]°/s

- "maxDec":-7.50

- 最大减速度；double 类型，范围[-10000,-1]

- "maxJerk":10000.0

- 最大加加速度；double 类型，范围[1,20000]

- "maxSpeed":2000.0

- 最大速度；double类型，范围[1,5000]mm/s

- "robot": 1

- 当前机器人号；int 类型，范围[1,4]

- "speedLimitMode":0

```
{
  "maxAcc":7.50,
  "maxAttitudeVel":500.0,
  "maxDec":-7.50,
  "maxJerk":10000.0,
  "maxSpeed":2000.0,
  "robot":1,
  "speedLimitMode":0
}
```
- 速度限制方式；int 类型，范围[0,1]
- 0表示位姿，1表示位置

- 上位机查询机器人笛卡尔参数

- 命令字：0x20C9

- "robot":1

```
{
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 控制器回复上位机机器人笛卡尔参数

- 命令字：0x20CA

- "maxAcc":7.50

- 最大加速度；double类型，范围[1,10000]

- "maxAttitudeVel":500.0

- 姿态运动最大速度；double 类型，范围[1,1000]°/s

- "maxDec":-7.50

- 最大减速度；double 类型，范围[-10000,-1]

- "maxJerk":10000.0

- 最大加加速度；double 类型，范围[1,20000]

- "maxSpeed":2000.0

- 最大速度；double类型，范围[1,5000]mm/s

- "robot": 1

- 当前机器人号；int 类型，范围[1,4]

- "speedLimitMode":0

```
{
  "maxAcc":7.50,
  "maxAttitudeVel":500.0,
  "maxDec":-7.50,
  "maxJerk":10000.0,
  "maxSpeed":2000.0,
  "robot":1,
  "speedLimitMode":0
}
```
- 速度限制方式；int 类型，范围[0,1]
- 0表示位姿，1表示位置

- 上位机设置机器人关节多圈值参数

- 命令字：0x20CB

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "robotAxis":

- 关节多圈值参数列表
- 长度为当前机器人轴数
- "axisSlaveSum":0

- 从动轴数量；int类型，范围[0,3]

- "enable":1

- 编码器多圈值溢出计数功能；int类型，范围[0,1]
- 0表示关闭功能，1表示开始功能

- "encode":

- 编码器最大值最小值列表
- 长度为关节从动轴数量+1
- "max":"32768"

- 编码器最大值；int类型，范围[-2^32,2^32]

- "min":"-32768"

```
{
  "robot":1,
  "robotAxis":
  [
    {
      "axisSlaveSum":0,
      "enable":1,
      "encode":
      [
        {
          "max":"32768",
          "min":"-32768"
        }
      ]
    },
    {
      "axisSlaveSum":0,
      "enable":0,
      "encode":
      [
        {
          "max":"32768",
          "min":"-32768"
        }
      ]
    },
    {
      "axisSlaveSum":0,
      "enable":0,
      "encode":
      [
        {
          "max":"32768",
          "min":"-32768"
        }
      ]
    },
    {
      "axisSlaveSum":0,
      "enable":0,
      "encode":
      [
        {
          "max":"32768",
          "min":"-32768"
        }
      ]
    },
    {
      "axisSlaveSum":0,
      "enable":0,
      "encode":
      [
        {
          "max":"32768",
          "min":"-32768"
        }
      ]
    },
    {
      "axisSlaveSum":0,
      "enable":0,
      "encode":
      [
        {
          "max":"32768",
          "min":"-32768"
        }
      ]
    }
  ]
}
```
- 编码器最小值；int类型，范围[-2^32,2^32]
- 编码器最小值不得大于编码器最大值

- 上位机查询机器人编码器多圈值参数

- 命令字：0x20CC

- "robot":1

```
{
  "robot":1
}
```
- 当前机器人号；int类型，范围[1,4]

- 控制器回复上位机机器人编码器多圈值参数

- 命令字：0x20CD

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "robotAxis":

- 关节多圈值参数列表
- 长度为当前机器人轴数
- "axisSlaveSum":0

- 从动轴数量；int类型，范围[0,3]

- "enable":1

- 编码器多圈值溢出计数功能；int类型，范围[0,1]
- 0表示关闭功能，1表示开始功能

- "encode":

- 编码器最大值最小值列表
- 长度为关节从动轴数量+1
- "max":"32768"

- 编码器最大值；int类型，范围[-2^32,2^32]

- "min":"-32768"

```
{
  "robot":1,
  "robotAxis":
  [
    {
      "axisSlaveSum":0,
      "enable":1,
      "encode":
      [
        {
          "max":"32768",
          "min":"-32768"
        }
      ]
    },
    {
      "axisSlaveSum":0,
      "enable":0,
      "encode":
      [
        {
          "max":"32768",
          "min":"-32768"
        }
      ]
    },
    {
      "axisSlaveSum":0,
      "enable":0,
      "encode":
      [
        {
          "max":"32768",
          "min":"-32768"
        }
      ]
    },
    {
      "axisSlaveSum":0,
      "enable":0,
      "encode":
      [
        {
          "max":"32768",
          "min":"-32768"
        }
      ]
    },
    {
      "axisSlaveSum":0,
      "enable":0,
      "encode":
      [
        {
          "max":"32768",
          "min":"-32768"
        }
      ]
    },
    {
      "axisSlaveSum":0,
      "enable":0,
      "encode":
      [
        {
          "max":"32768",
          "min":"-32768"
        }
      ]
    }
  ]
}
```
- 编码器最小值；int类型，范围[-2^32,2^32]
- 编码器最小值不得大于编码器最大值

- 上位机申请另存为预置机器人参数文件

- 命令字：0x20CE

- "name":"R_GENERAL_6S"

- 机器人类型名称；string 类型

- "presetRobotName":"AAA"

```
{
  "name":"R_GENERAL_6S",
  "presetRobotName":"AAA"
}
```
- 预置机器人参数自定义名称；string 类型

- 上位机查询预置机器人文件列表

- 命令字：0x20CF

- "name":"R_GENERAL_6S"

```
{
  "name":"R_GENERAL_6S"
}
```
- 机器人类型名称；string 类型

- 控制器回复上位机预置机器人文件列表

- 命令字：0x20D0

- "listnum":2

- 预置机器人数量；int 类型

- "nameList":["AAA","BBB"]

```
{
  "listnum":2,
  "nameList":["AAA.json", "BBB.json"]
}
```
- 预置机器人自定义名称列表；string 类型

- 上位机发送获取预置参数请求

- 命令字：0x20D1

- "name":"R_GENERAL_6S"

- 机器人类型名称；string 类型

- "presetRobotName":"AAA"

```
{
  "name":"R_GENERAL_6S",
  "presetRobotName":"AAA.json"
}
```
- 预置机器人参数自定义名称；string 类型

- 控制器回复机器人已保存的预置机器人参数

- 命令字：0x20D2

- "DH":

- 保存的预置机器人DH参数
- "L1":390.0

- L1杆长；double类型，范围[-4000,4000]

- "L2":450.872

- L2杆长；double类型，范围[-4000,4000]

- "L3":99.462

- L3杆长；double类型，范围[-4000,4000]

- "L4":471.29

- L4杆长；double类型，范围[-4000,4000]

- "L5":123.0

- L5杆长；double类型，范围[-4000,4000]

- "L6":-0.544

- L6杆长；double类型，范围[-4000,4000]

- "L7":0.0

- L7杆长；double类型，范围[-4000,4000]

- "L8":0.0

- L8杆长；double类型，范围[-4000,4000]

- "angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0]

- 机器人角度转距离列表；double类型
- 长度为当前机器人的轴数

- "couplingRatio12":0.0

- 1/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio23":0.0

- 2/3耦合比；double类型，范围[-1000,1000]

- "couplingRatio32":0.0

- 3/2耦合比；double类型，范围[-1000,1000]

- "couplingRatio34":0.0

- 3/4耦合比；double类型，范围[-1000,1000]

- "couplingRatio45":0.0

- 4/5耦合比；double类型，范围[-1000,1000]

- "couplingRatio46":0.0

- 4/6耦合比；double类型，范围[-1000,1000]

- "couplingRatio56":0.0

- 5/6耦合比；double类型，范围[-1000,1000]

- "fiveAxisDirection":90.0

- 五轴方向；double类型，范围0,90 度

- "dynamicLimit":

- J2+J3范围限制
- "max":20.0

- J2+J3最大值；double类型，范围[-500,500]

- "min":-20.0

- J2+J3最小值；double类型，范围[-500,500]

- "mountAngle":false

- 机器人正装或倒装；bool类型
- false表示正装，true表示倒装

- "robotType":1

- 当前机器人类型；int类型

- "Joint":

- 保存的预置机器人关节参数
- "axisNum":1

- 机器人轴编号；int 类型，范围[1,7]

- "axisDirection":1

- 关节实际方向；int 类型，范围-1,1

- "backLash":0.0

- 齿轮反向间隙；double 类型，范围[0,9999.999]

- "direction":-1.0

- 模型方向；int 类型，范围-1,1

- "encoderResolution":17

- 编码器位数；int 类型，范围[1,100]

- "isReduceRatioEnable":true

- 编码器是否经过减速机；bool 类型

- "maxAcc":6.0

- 最大加速度；double 类型，范围[1,10000]

- "maxDec":-6.0

- 最大减速度；double 类型，范围[-10000,-1]

- "maxJerkAcc":1.0

- 最大加加速度；double 类型，范围[1,20000]
- 机器人插补方式为加加速度时生效

- "maxJerkDec":-1.0

- 最大减减速度；double类型，范围[-20000,-1]
- 机器人插补方式为加加速度时生效

- "maxRPM":1.0

- 最大正转速；double 类型，范围[1,5]

- "maxReverseRPM":-1.0

- 最大反转速；double 类型，范围[-5,-1]

- "positiveLimit":160.0

- 关节正限位；double 类型，范围[1,3000]

- "ratedRPM":3600.0

- 额定正转速；double 类型，范围[1,10000]

- "ratedReverseRPM":-3600.0

- 额定反转速；double 类型，范围[-10000,-1]
- 数值为额定正速度的负值

- "ratedReverseSpeed":-270.0540

- 额定反速度；double 类型

- "ratedSpeed":270.0540

- 额定正速度；double 类型

- "reducRatio":79.984

- 减速比；double 类型，范围(0,1000]

- "reverseLimit":-160.0

```
{
  "DH":
  {
    "L1":390.0,
    "L2":450.872,
    "L3":99.462,
    "L4":471.29,
    "L5":123.0,
    "L6":-0.544,
    "L7":-0.0,
    "L8":0.0,
    "angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0],
    "couplingRatio12":0.0,
    "couplingRatio23":0.0,
    "couplingRatio32":0.0,
    "couplingRatio34":0.0,
    "couplingRatio45":0.0,
    "couplingRatio46":0.0,
    "couplingRatio56":0.0,
    "distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0],
    "dynamicLimit":
    {
      "max":20.0,
      "min":-20.0
    }
    "fiveAxisDirection":90,
    "mountAngle":false,
    "robotType":1
  },
  "Joint":
  [
    {
      "axisDirection":1,
      "axisNum":1,
      "backLash":0.0,
      "direction":-1,
      "encoderResolution":17,
      "isReduceRatioEnable":true,
      "maxAcc":6.0,
      "maxDec":-6.0,
      "maxJerkAcc":1.0,
      "maxJerkDec":-1.0,
      "maxRPM":1.0,
      "maxReverseRPM":-1.0,
      "positiveLimit":160.0,
      "ratedRPM":3600.0,
      "ratedReverseRPM":-3600.0,
      "ratedReverseSpeed":-270.05401080216,
      "ratedSpeed":270.05401080216,
      "reducRatio":79.984,
      "reverseLimit":-160.0
    },
    {
      "axisDirection":1,
      "axisNum":2,
      "backLash":0.0,
      "direction":1,
      "encoderResolution":17,
      "isReduceRatioEnable":true,
      "maxAcc":3.75,
      "maxDec":-3.75,
      "maxJerkAcc":1.0,
      "maxJerkDec":-1.0,
      "maxRPM":1.0,
      "maxReverseRPM":-1.0,
      "positiveLimit":100.0,
      "ratedRPM":3600.0,
      "ratedReverseRPM":-3600.0,
      "ratedReverseSpeed":-196.690858428112,
      "ratedSpeed":196.690858428112,
      "reducRatio":109.817,
      "reverseLimit":-100.0
    },
    {
      "axisDirection":1,
      "axisNum":3,
      "backLash":0.0,
      "direction":1,
      "encoderResolution":17,
      "isReduceRatioEnable":true,
      "maxAcc":7.5,
      "maxDec":-7.5,
      "maxJerkAcc":1.0,
      "maxJerkDec":-1.0,
      "maxRPM":1.0,
      "maxReverseRPM":-1.0,
      "positiveLimit":90.0,
      "ratedRPM":5000.0,
      "ratedReverseRPM":-5000.0,
      "ratedReverseSpeed":-299.604522030919,
      "ratedSpeed":299.604522030919,
      "reducRatio":100.132,
      "reverseLimit":-75.0
    },
    {
      "axisDirection":1,
      "axisNum":4,
      "backLash":0.0,
      "direction":-1,
      "encoderResolution":17,
      "isReduceRatioEnable":true,
      "maxAcc":7.5,
      "maxDec":-7.5,
      "maxJerkAcc":1.0,
      "maxJerkDec":-1.0,
      "maxRPM":1.0,
      "maxReverseRPM":-1.0,
      "positiveLimit":190.0,
      "ratedRPM":5000.0,
      "ratedReverseRPM":-5000.0,
      "ratedReverseSpeed":-252.175009456563,
      "ratedSpeed":252.175009456563,
      "reducRatio":118.965,
      "reverseLimit":-190.0
    },
    {
      "axisDirection":1,
      "axisNum":5,
      "backLash":0.0,
      "direction":1,
      "encoderResolution":17,
      "isReduceRatioEnable":true,
      "maxAcc":7.5,
      "maxDec":-7.5,
      "maxJerkAcc":1.0,
      "maxJerkDec":-1.0,
      "maxRPM":1.0,
      "maxReverseRPM":-1.0,
      "positiveLimit":20.0,
      "ratedRPM":4500.0,
      "ratedReverseRPM":-4500.0,
      "ratedReverseSpeed":-337.491562710932,
      "ratedSpeed":337.491562710932,
      "reducRatio":80.002,
      "reverseLimit":-200.0
    },
    {
      "axisDirection":1,
      "axisNum":6,
      "backLash":0.0,
      "direction":-1,
      "encoderResolution":17,
      "isReduceRatioEnable":true,
      "maxAcc":7.5,
      "maxDec":-7.5,
      "maxJerkAcc":1.0,
      "maxJerkDec":-1.0,
      "maxRPM":1.0,
      "maxReverseRPM":-1.0,
      "positiveLimit":360.0,
      "ratedRPM":4500.0,
      "ratedReverseRPM":-4500.0,
      "ratedReverseSpeed":-337.622388115692,
      "ratedSpeed":337.622388115692,
      "reducRatio":79.971,
      "reverseLimit":-360.0
    }
  ]
}
```
- 关节反限位；double 类型，范围[-3000,-1]

- 上位机发送酒槽机型标记圆心请求

```
{}
- 命令字：0x20D3

```