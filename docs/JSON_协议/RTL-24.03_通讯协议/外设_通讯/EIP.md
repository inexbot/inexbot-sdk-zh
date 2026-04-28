# EIP

- 说明
- EIP参数设置

- 命令字：0x7360

- "type":1

- 几路输出(入)；int类型；取值1||4||8||12||16

- "grouptype":0

- 组号的方式；int类型；取值范围[0,2]
- 0:手填，1：全局int类型变量，2：全局int类型绑定变量

- "group":4

- 组号中的数字；int类型

- "addtype":0

- 数值存入的方式；int类型；取值范围[0,3]
- 0：全局int类型变量；1：全局int类型绑定变量；2：全局double类型变量；3：全局double类型绑定变量

- "add":1

- 数值存入的数字；int类型

- "num":8

- 编号；int类型；取值范围[1,20]
- 1-10:输出；11-20：输入

- "value"

- 值

- "able":true

```
{
  "type": 4,
  "grouptype": 1,
  "group": 3,
  "addtype": 2,
  "add": 100,
  "num": 5,
  "value": 1,
  "able": true
}
```
- 使能开关；bool类型
- true：使能，false：不使能

- 上位机获取设备参数配置

- 命令字：0x7361

- data：无

- 控制器响应并返回设备参数

- 命令字：0x7362

- 同0x7360

- 上位机设置连接参数

- 命令字：0x7363

- "enable":true

- 连接开关；bool类型
- true：打开连接开关；false关闭连接开关

- "writenum":34

- 写入长度；int类型；取值范围[0,256]

- "readnum":45

- 读取长度；int类型；取值范围[0,256]

- "scancycle"

- 扫描周期

- "outtimecycle"

- 超时周期

- "networkname"

- 选取的网口的名称

- "writetype":0

- 本机写的类型;int类型；取值范围[0,1]
- 0:全局bool类型变量；1：全局bool类型绑定变量

- "writeadd"

- 本机写的位置

- "readtype":0

- 本机读的类型;int类型；取值范围[0,1]

- 0:全局bool类型变量；1：全局bool类型绑定变量

- "readadd"

```
{
  "enable": true,
  "writenum": 0,
  "readnum": 0,
  "scancycle": 0,
  "outtimecycle": 0,
  "networkname": "",
  "writetype": 0,
  "writeadd": 0,
  "readtype": 0,
  "readadd": 0
}
```
- 本机读的位置

- 上位机获取连接参数配置

- 命令字：0x7364

- data：无

- 控制器响应并返回连接参数

- 命令字：0x7365

- 同0x7363

- 上位机向控制器获取连接状态

- 命令字：0x7366

- data：无

- 响应并返回连接状态

- 命令字：0x7367

- 控制器响应并返回读取数据的状态

- 命令字：0x7368

- "num":2
- 编号信息；int类型；取值范围[0,19]
- 0-9:输出；10-19：输入

- "value":1

- 值

- 读取数据的状态设置

- 命令字：0x7369

- "state":false

```
{
  "state":false
}
- true:EIP设定界面的参数会随着EIP接收数据的变化而变化；false:EIP设定界面的参数不会随着EIP接收数据的变化而变化

```