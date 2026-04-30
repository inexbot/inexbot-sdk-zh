# 远程IO控制

### IO功能界面设置

#### IO功能界面设置时，示教盒发送下面命令：

*0x2F01  IO_CONTROL_SET

```json
{
  "inPort": {  //远程IO功能 端口绑定
    "clearoutagekeep": 16,  //清除断电保持数据 绑定16端口DIN
    "faultReset": 4,  //清除报警
    "pause": 3,      //暂停
    "start": 1,     //启动
    "stop": 2     //停止
  },
  "inValue": {  //端口值  IO参数，0：低电平有效，1：高电平有效
    "clearoutagekeep": 1,   //清除断电保持数据
    "faultReset": 1,      //清除报警
    "pause": 1,      //暂停
    "start": 1,      //启动
    "stop": 1       //停止
  },
  "program": [  //远程IO程序DIN和value绑定，共10个
    {
      "port": 5,
      "value": 1
    },
    {
      "port": 6,
      "value": 0
    },
    {
      "port": 7,
      "value": 0
    },
    {
      "port": 8,
      "value": 1
    },
    {
      "port": 9,
      "value": 1
    },
    {
      "port": 0,
      "value": 1
    },
    {
      "port": 0,
      "value": 1
    },
    {
      "port": 0,
      "value": 1
    },
    {
      "port": 0,
      "value": 1
    },
    {
      "port": 0,
      "value": 1
    }
  ],
  "robot": 1
}
```
#### IO功能界面查询设置时，示教盒发送下面命令：

*0x2F02  IO_CONTROL_INQUIRE

```json
{
"robot":1
}
```

#### IO功能界面，控制器收到查询时，发送下面命令：

*0x2F03  IO_CONTROL_RESPOND

```json
{
  "inPort": {  //远程IO功能 端口绑定
    "clearoutagekeep": 16,  //清除断电保持数据 绑定16端口DIN
    "faultReset": 4,  //清除报警
    "pause": 3,      //暂停
    "start": 1,     //启动
    "stop": 2     //停止
  },
  "inValue": {  //端口值  IO参数，0：低电平有效，1：高电平有效
    "clearoutagekeep": 1,   //清除断电保持数据
    "faultReset": 1,      //清除报警
    "pause": 1,      //暂停
    "start": 1,      //启动
    "stop": 1       //停止
  },
  "program": [  //远程IO程序DIN和value绑定，共10个
    {
      "port": 5,
      "value": 1
    },
    {
      "port": 6,
      "value": 0
    },
    {
      "port": 7,
      "value": 0
    },
    {
      "port": 8,
      "value": 1
    },
    {
      "port": 9,
      "value": 1
    },
    {
      "port": 0,
      "value": 1
    },
    {
      "port": 0,
      "value": 1
    },
    {
      "port": 0,
      "value": 1
    },
    {
      "port": 0,
      "value": 1
    },
    {
      "port": 0,
      "value": 1
    }
  ],
  "robot": 1
}
```
### 复位点设置

#### 复位点设置 界面设置时，修改复位点位置参数，示教盒发送下面命令：

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/3CBmjv6j/resources/5IF7NsxJ1If6iOHA_Py0Vca61NZDInIkWzWZqRerPXs.png)

*0x2F04  IO_CONTROL_RESETPOS_SET

```json
{
"pos": [ 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0 ],  机器人位置（7）
"posSync": [ 0.0, 0.0, 0.0, 0.0, 0.0 ],   外部轴位置（5）
"robot": 1
}
```
#### 复位点设置界面，修改复位点io参数，示教盒发送下面命令：

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/3CBmjv6j/resources/Hwywg0ljXi2neH9Q7STjXo7yF29t0YD6AdzRTZrv4-0.png)

*0x2F14  IO_CONTROL_RESETPORT_SET

```json
{
"robot":1,			//机器人号
"selectPiontOrFile":0       //0:复位点，1:复位程序
"inPort":0,			//复位开始，IO触发端口
"inValue":1,			//复位开始，IO参数
"outPort":0,			//复位结束，IO输出端口
"safeEnable":true ,
"returnway":0			//0:关节插补，1：直线插补
}
```

#### 设置安全点误差参数

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/3CBmjv6j/resources/bNWUG5DgFZ5dNloFj8dM8_INILqr1HGdlJq8DvZdZ2k.png)

*0x2F15  IO_CONTROL_RESETSAFEDEV_SET​
​{

"deviation":[1.0,2.0,3.0,4.0,5.0,6.0,1.0], //机器人位置（7）

"deviationSync":[1.0,1.0,1.0,1.0,1.0], //外部轴(5)

"robot":1

}

#### 运行模式，运行作业文件时候，开始安全使能,不在安全点时，控制器返回发送：

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/3CBmjv6j/resources/wmi9Eb3kGHcNjlH3bEzLZeZh8xU1Myc0gQO1XNgskH4.png)

*0x2F16  IO_CONTROL_NOTIS_SAFEPOS

```json
{
"robot::1,  //当前机器人
"isSync":false,//false:机器人不在安全区，true:外部轴不在安全区
"currentPos":[0, 0.1, 2, 3.3, 44, 555.55, 6, 7.7, 88],//坐标
"safePos":[0, 0.1, 2, 3.3, 88, 555.55, 6, 7.7, 88]//复位点位
}
```

#### 回复位：

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/3CBmjv6j/resources/njP7H6RL7iGEGYTNSZLA-3M8jFvkaaQgOx5YNJmmkBw.png)

*0x2F17   RECOVERY_SITE

```json
{
"robot":1			//机器人号
}
```

#### 复位点设置界面查询设置时，示教盒发送下面命令：

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/3CBmjv6j/resources/Pvs9dLcUZ9uK4wJ4w2PMNRREYR8926q24ayFGK3D37w.png)

*0x2F05  IO_CONTROL_RESET_INQUIRE

```json
{
"robot":1,			//机器人号
}
```

#### 复位点设置界面，控制器收到查询时，发送下面命令：

*0x2F06  IO_CONTROL_RESET_RESPOND

```json
{
"robot":1,			//机器人号
"selectPiontOrFile":1,			//0选择的是点，1选择的程序
“returnWay”:1         //0表示选择的是movj,1表示的是movl
"inPort":0,			//复位开始，IO触发端口
"inValue":1,			//复位开始，IO参数
"outPort":0,					//复位结束始，IO输出端口
"safeEnable":true,
"pos":[0, 0.1, 2, 3.3, 44, 555.55, 6, 7.7, 88],
//复位点坐标
"posSync":[0, 0.1, 2, 3.3, 44, 555.55, 6, 7.7, 88],  //外部轴复位点坐标
"deviation":[0, 0.1, 2, 3.3, 44, 555.55, 6, 7.7, 88],  //安全点范围
"deviationSync":[1.0,1.0,1.0,1.0,1.0],  //外部轴安全点范围
}
```

#### 复位点设置界面，当前位置查询，示教盒发送下面命令：

*0x2F07  IO_CONTROL_POS_INQUIRE

```json
{
"robot":1,			//机器人号
"coord":0			//坐标模式	-1-控制器当前坐标 0-关节坐标 1-直角坐标 2-工具坐标 							3-用户坐标
}
```

#### 复位点设置界面，控制器收到当前位置查询时，发送下面命令：

*0x2F08  IO_CONTROL_POS_RESPOND

```json
{
"robot":1,			                //机器人号
"coord":1                        //坐标
"pos":[0, 0.1, 2, 3.3, 44, 555.55]              //弧度点位
"posDeg":[0, 0.1, 2, 3.3, 44, 555.55]           //角度点位
"configuration":1                       //形态
}
```

#### MOVJDOUBLE指令在双机下需要同时查询第一和第二个机器人位置，发送下面命令：

*0x2F10  IO_CONTROL_DOUBLE_POS_INQUIRE

```json
{
"robot1":1,         //机器人1
"coord1":1        //机器人1坐标： 1：获取直角坐标 2：获取工具坐标 3：获取用户坐标
"robot2":2         //机器人2
"coord2":1         //同机器人1
}
```

#### 控制器恢复0x2F10查询结果，发送下面命令：

*0x2F11  IO_CONTROL_DOUBLE_POS_RESPOND

```json
{
"pos1Deg":[0 , 1.1 , 2 , 3.3 , 4.4 , 5.5 , 6.6]		 	  //机器人1轴1-7当前位置（角度表示）
"pos1":[0 , 1.1 , 2 , 3.3 , 4.4 , 5.5 , 6.6]		 	  //机器人1轴1-7当前位置（弧度表示）
"pos2Deg":[0 , 1.1 , 2 , 3.3 , 4.4 , 5.5 , 6.6]		 	  //机器人2轴1-7当前位置（角度表示）
"pos2":[0 , 1.1 , 2 , 3.3 , 4.4 , 5.5 , 6.6]        //机器人2轴1-7当前位置（弧度表示）
}
```

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/3CBmjv6j/resources/x3XvvW3u1uHqDRy7t4SJfLvsnAujg4iD5k9iKuM73ks.png)

#### 打开作业文件

0x3114  打开作业文件，复位程序固定是RobotResetProgram，后缀是.ResetPro

```json
{
"jobName":"RobotResetProgram",  //作业文件名称 固定
"robot":1,
"suffixname":".ResetPro"  //作业文件后缀 固定
}​
```
​

#### 插入指令

0x3121​
​

#### 保存作业文件，

0x3120 复位程序固定是RobotResetProgram，后缀是.ResetPro​
​{​
​"jobname":"RobotResetProgram",​
​"robot":1,​
​"suffix":".ResetPro"​
​}

### 状态提示设置界面

#### 状态提示设置界面 设置时，示教盒发送下面命令：

*0x2F09  IO_CONTROL_OUTPUT_SET

```json
{
  "outPut": [
    {  //机器人1
      "IOenable": 1,  //使能DOUT绑定
      "IOenable_value": 1,  //0  1  3:闪烁
      "continuable": 3,  //可继续执行DOUT绑定
      "continuable_value": 1,   //0  1  3:闪烁
      "fault": 5,  //报错提示DOUT绑定
      "faultIsFickler": 1,  //0  1  3:闪烁
      "mainJobFirstLine": 7,  //主程序首行DOUT绑定
      "mainJobFirstLine_value": 1,
      "pause": 9,  //暂停DOUT绑定
      "pause_value": 1,
      "quickStopOut1": 11, //紧急急停1DOUT绑定
      "quickStopOut2": 12,  //紧急急停2DOUT绑定
      "quickStopOutValue1": 1,
      "quickStopOutValue2": 1,
      "running": 15,  //运行DOUT绑定
      "running_value": 1,
      "stop": 17,  //停止DOUT绑定
      "stop_value": 1,
      "teachBoxStateOut": 0,  //拔出示教盒DOUT绑定
      "teachBoxStateOutValue": 1
    },
    {  机器人2
      "IOenable": 0,
       ***略
      "stop_value": 1
    },
    {  机器人3
      "IOenable": 0,
     ***略
      "stop_value": 1
    },
    {  机器人4
      "IOenable": 0,
      ***略
      "stop_value": 1
    }
  ],
  "remoteOut": 1,  //远程模式
  "remoteOut_value": 1,  //0  1  3:闪烁
  "runOut": 2,  //运行模式
  "runOut_value": 1,
  "startUp": 3,  //开机提示
  "startUp_value": 1,
  "teachOut": 4,  //示教模式
  "teachOut_value": 1
}
```
#### 状态提示设置界面 查询设置时，示教盒发送下面命令：

*0x2F0A  IO_CONTROL_OUTPUT_INQUIRE

data : 无

#### 状态提示设置界面，控制器收到查询时，发送下面命令：

*0x2F0B  IO_CONTROL_OUTPUT_RESPOND

data ：同0x2F09

### IO复位设置界面

#### IO输出设置界面 复位设置时，示教盒发送下面命令：

*0x2F0D  IO_CONTROL_IORESET_SET

```json
{
"robot":1.
"type":1,//1：IO复位，2：切模式停止，3：程序报错停止
"enable":[0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],//值为0,1	包含复位值及是否复位
"value":[0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0]//值为0,1		包含复位值及是否复位
}
```

#### IO输出设置界面 查询设置时，示教盒发送下面命令：

*0x2F0E  IO_CONTROL_IORESET_INQUIRE

```json
{
"robot":1,
"type":1,
}
```

#### IO输出设置界面，控制器收到查询时，发送下面命令：

*0x2F0F  IO_CONTROL_IORESET_RESPOND

data ：同0x2F0D

### IO功能状态界面

#### IO功能状态界面，示教盒发送下面命令：

*0x2F12  IO_FUNCTION_INQUIRE

```json
{
"type":1				//数字输入:1，数字输出:2，模拟输入:3，模拟输出:4
}
```

#### IO功能状态界面，控制器收到查询时，发送下面命令：

*0x2F13  IO_FUNCTION_RESPOND

```json
{
"type":1,
"IOFunction":			//数字有16个，模拟有8个
["远程：机器人1启动 机器人1视觉:触发端口","","","","","","","","","","","","","","",""]
}
```

### 远程模式界面

#### 远程模式界面，示教盒查询预约执行状态时，发送：

*0x2F1B  RESERVE_EXE_STATE_INQUIRE

```json
{
"robot":1
}
```

#### 控制器返回：

*0x2F1C  RESERVE_EXE_STATE_RESPOND

```json
{
"robot":1,  //机器人号
"current":
{
"station":1,    //工作站（程序编号）
"name":"Q1",  // 程序名
"runtime":1,//当前运行的已运行次数
"times":3,//当前运行的运行总数
"count":1,//运行总数
"status":2   //运行状态：//状态: 0-无预约，1-预约中，2-运行中，3-已预约，4-程序暂停
},
"queue":   //状态: 0-无预约，1-预约中，2-运行中，3-已预约，4-程序暂停
[
{"station":1,//工作站（程序编号）
"name":"Q4",// 程序名
"times":2,//运行次数
"count":0,//运行总数
"status":1 //状态: 0-无预约，1-预约中，2-运行中，3-已预约，4-程序
},
{"station":1,"name":"Q1","times":6,"count":0,"status":1},
{"station":1,"name":"Q3","times":1,"count":0,"status":1},
{"station":1,"name":"","times":1,"count":0,"status":0},
{"station":1,"name":"","times":2,"count":0,"status":0},
…… //10个
]
}
```

#### 运行总数清零：

*0x2F1D  RESERVE_EXE_STATE_RESPOND

```json
{
"robot":1
}
```

### IO型号设置

#### IO型号设置：示教盒发送，重启生效

*0x2F21  IO_TYPE_SET

```json
{
"simuNum":0,  //虚拟IO数量
"serialAnalog":
{
"type":"SUPER_ANAIO",		//可选"SUPER_ANAIO","DAC_ANAIO"
"port":1,   //端口号
"baudRate":115200   //波特率
}
}
```

#### IO型号查询：示教盒发送

*0x2F22  IO_TYPE_INQUIRE

#### IO型号返回：控制器发送

*0x2F23  IO_TYPE_RESPOND

```json
{
"num":3,
"type":["IO板R1","盟通","虚拟IO"],
"portNum":[[16,16,2,2],[20,16,4,2],[16,16,0,0]],
"simuNum":1,
"serialAnalog":
{
"type":"SUPER_ANAIO",  //可选"SUPER_ANAIO","DAC_ANAIO"
"port":1,
"baudRate":115200,
}
}
```

### 远程状态提示

#### 远程状态提示设置

*0x2F24  IO_REMOTEOUTPUT_SET

```json
{
"outPut": [ {
"outagerecover": 2,  //断电保持数据恢复DOUT1-2端口绑定
"outagerecover_value": 0,   // DOUT1-2端口值 0 ，1，2（2代表闪烁）
"program1": 1,   // //远程IO程序DOUT1-1端口绑定
"program10": 0,
"program2": 2,
"program3": 3,
"program4": 0,
"program5": 0,
"program6": 0,
"program7": 0,
"program8": 63,
"program9": 64,
"program_value1": 1,     //远程IO程序DOUT输出端口值 0 ，1，2（2代表闪烁）
"program_value10": 0,
"program_value2": 1,
"program_value3": 1,
"program_value4": 0,
"program_value5": 0,
"program_value6": 0,
"program_value7": 0,
"program_value8": 0,
"program_value9": 2 } ],
"robot": 1 }
```

#### 远程状态提示查询

*0x2F25  IO_REMOTEOUTPUT_INQUIRE

```json
{
"robot":1,
}
```

#### 控制器恢复0x2F25查询结果

*0x2F26  IO_REMOTEOUTPUT_RESPOND

内容同*0x2F24

### 安全监测设置

#### 安全监测设置：示教盒发送

*0x2F31  IO_SAFE_CHECK_SET

```json
{
"robot":1,
"safeScreen":
{
"enable":false,		//使能安全光幕
"port1":0,			//安全光幕1 DIN序号 每个IO板接口号为1~16
"value1":1,		//IO电平参数 0-低电平 1-高电平
"port2":0,			//安全光幕2 DIN序号 每个IO板接口号为1~16
"value2":1		//IO电平参数 0-低电平 1-高电平
}
"quickStop":
{
"enable":false,
"port1":15,			//紧急停止1 DIN序号 每个IO板接口号为1~16
"value1":1,			//IO电平参数 0-低电平 1-高电平
"port2":15,			//紧急停止2 DIN序号 每个IO板接口号为1~16
"value2":1,			//IO电平参数 0-低电平 1-高电平
"time":60				//快速停止时间 范围50~200整数 单位ms
"shieldFlag1":false;		//屏蔽紧急停止
"shieldFlag2":false;		//屏蔽紧急停止
"shieldTime":30//单位秒，int	10位整数
}
}
```

#### 示教盒查询安全监测时，发送

*0x2F32  IO_SAFE_CHECK_INQUIRE

```json
{
"robot":1
}
```

#### 控制器返回：

*0x2F33  IO_SAFE_CHECK_RESPOND

同0x2F31

### IO触发消息设置

#### IO触发消息设置（DIN）：

*0x2F41  DIN_TRIGGER_MSG_SET

```json
{
"enable":[1,1,0,0,0,0,1,1],	//每有一块IO板增加16个数据		1-使能端口报警 2-不使能
"value":[0,1,1,0,0,1,1],//每有一块IO板增加16个数据	端口电平状态 1-高电平 0-低电平
"msg":["","qwer","","asd",""]//每有一块IO板增加16个数据
}
```

#### 查询

*0x2F42  DIN_TRIGGER_MSG_INQUIRE

data:无

#### 控制器返回

*0x2F43  DIN_TRIGGER_MSG_RESPOND

同 0x2F41

#### IO数字输出DOUT

*0x2F44 DOUT_TRIGGER_MSG_SET

```json
{
"enable":[1,1,0,0,0,0,1,1],//每有一块IO板增加16个数据		1-使能端口报警 2-不使能
"value":[0,1,1,0,0,1,1],//每有一块IO板增加16个数据	端口电平状态 1-高电平 0-低电平
"msg":["","qwer","","asd",""]//每有一块IO板增加16个数据
}
```

#### 查询

*0x2F45  DOUT_TRIGGER_MSG_INQUIRE

data:无

#### 控制器返回

*0x2F46  DOUT_TRIGGER_MSG_RESPOND

同 0x2F44

### 配置文件的修改查询操作

#### 修改din注释配置文件

*0x2F47  DIN_ANNOTATION_NAME_SET

```json
{
“name”：["","qwer","","asd",""]//每有一块IO板增加16个数据
}
```

#### 查询din配置文件

*0x2F48  DIN_ANNOTATION_NAME_INQUIRE

#### 返回din配置文件

*0x2F49  DIN_ANNOTATION_NAME_RESPOND

#### 设置dout

*0x2F4A  DOUT_ANNOTATION_NAME_SET

```json
{
"name" = ["","dsad","wa"...]  //每有一块IO板增加16个数据
}
```

#### 示教器dout查询

*0x2F4B  DOUT_ANNOTATION_NAME_INQUIRE

#### 控制器返回dout数据

*0x2F4C  DOUT_ANNOTATION_NAME_RESPOND

#### 设置ain端口注释名称

*0x2F4D   AIN_ANNOTATION_NAME_SET

```json
{
"name"= ["","asd", "ayt",""...]    //每有一块IO板增加16个数据
}
```

#### 示教器查询ain参数

*0x2F4E   AIN_ANNOTATION_NAME_INQUIRE

data:无

#### 示教器返回查询结果

*0x2F4F  AIN_ANNOTATION_NAME_RESPOND

#### 设置aout端口注释名称

*0x2F50   AOUT_ANNOTATION_NAME_SET

```json
{
"name" = ["","das","dsf","ty"...]  //每有一块IO板增加16个数据
}
```

#### 示教器查询aout参数配置文件

*0x2F51  AOUT_ANNOTATION_NAME_INQUIRE

#### 控制器返会查询结果

*0x2F52  AOUT_ANNOTATION_NAME_RESPOND
