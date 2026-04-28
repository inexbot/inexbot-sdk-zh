# Modbus

- 说明
- 上位机设置modbus主站参数

- 命令字：0x7300

- "masterStation":

- 主站参数，包含有RTU参数和TCP参数
- "RTU":

- RTU参数
- "baudrate":115200

- 波特率；int类型

- "checkBit":"E"

- 校验位；string类型，范围"N","E","O"

- "dataBit":5

- 数据位；int类型，范围[5,8]

- "port":2

- 端口号；int类型

- "slaveId":1

- 从站ID；int类型，范围[0,65535]

- "stopBit":1

- 停止位；int类型，范围[0,1]

- "TCP":

- TCP参数
- "IP":"192.168.1.14"

- IP地址；string类型

- "endian_type":1

- Float大小端；int类型，范围[0,3]
- 0表示AB CD，1表示CD AB，2表示BA DC，3表示DC BA

- "port":503

- 端口号；int类型，范围[0,65535]

- "processNumber":1

- 需要设置的工艺号；int类型，范围[1,9]

- "type":"TCP"

- 主站类型；string类型，范围"TCP","RTU"

- "startAddress":false

```
{
  "masterStation":
  {
    "RTU":
    {
      "baudrate":115200,
      "checkBit":"E",
      "dataBit":5,
      "port":2,
      "slaveId":1,
      "stopBit":1
    },
    "TCP":
    {
      "IP":"192.168.1.14",
      "endian_type":1,
      "port":503
    },
    "processNumber":1,
    "type":"TCP"
  },
  "startAddress":false
}
```
- 地址偏移；bool类型
- true表示地址不变，false表示地址自动-1

- 上位机查询modbus参数

- 命令字：0x7301

- "processNumber":1

```
{
  "processNumber":1
}
```
- 需要查询的工艺号；int类型，范围[1,9]

- 控制器回复上位机modbus参数

- 命令字：0x7302

- "RTU":

- RTU参数
- "baudrate":115200

- 波特率；int类型

- "checkBit":"E"

- 校验位；string类型，范围"N","E","O"

- "dataBit":5

- 数据位；int类型，范围[5,8]

- "port":2

- 端口号；int类型

- "slaveId":1

- 从站ID；int类型，范围[0,65535]

- "stopBit":1

- 停止位；int类型，范围[0,1]

- "TCP":

- TCP参数
- "IP":"192.168.1.14"

- IP地址；string类型

- "endian_type":1

- Float大小端；int类型，范围[0,3]
- 0表示AB CD，1表示CD AB，2表示BA DC，3表示DC BA

- "port":503

- 端口号；int类型，范围[0,65535]

- "modbus_state":false

- Modbus连接状态；bool类型
- true表示已连接，false表示未连接

- "response_time_out":100

- 读写响应时间；int类型，单位ms

- "startAddress":false

- 地址偏移；bool类型
- true表示地址不变，false表示地址自动-1

- "type":"TCP"

```
{
  "RTU":
  {
    "baudrate":115200,
    "checkBit":"E",
    "dataBit":5,
    "port":2,
    "slaveId":1,
    "stopBit":1
  },
  "TCP":
  {
    "IP":"192.168.1.14",
    "endian_type":1,
    "port":503
  },
  "modbus_state":false,
  "response_time_out":100,
  "startAddress":false,
  "type":"TCP"
}
```
- 主站类型；string类型，取值"TCP","RTU"

- 上位机查询modbus连接状态

```
{}
```
- 命令字：0x7303

- 控制器回复上位机modbus连接状态

- 命令字：0x7304

- "ModbusConnect":false

```
{
  "ModbusConnect":false
}
```
- modbus连接状态；bool类型
- true表示已连接，false表示未连接

- 上位机设置modbus从站参数

- 命令字：0x7305

- "RTU":

- RTU参数
- "baudrate":115200

- 波特率；int类型

- "port":2

- 端口号；int类型

- "slaveId":1

- 从站ID；int类型，范围[0,65535]

- "TCP":

- TCP参数
- "IP":"192.168.1.11"

- IP地址；默认值

- "endian_type":0

- Float大小端；int类型，范围[0,3]
- 0表示AB CD，1表示CD AB，2表示BA DC，3表示DC BA

- "port":502

- 端口号；int类型，范围[0,65535]

- "master-slave":1

- modbus通讯的的主从模式；int类型，范围[0,1]
- 0表示主站，1表示从站

- "scancycle":100

- 扫描周期；int类型，范围[8,1000]ms

- "stoprun":0

- 通讯断开时操作；int类型，范围[0,1]
- 0表示不停机，1表示停机

- "type":"TCP"

```
{
  "RTU":
  {
    "baudrate":115200,
    "port":2,
    "slaveId":1
  },
  "TCP":
  {
    "IP":"192.168.1.11",
    "endian_type":0,
    "port":502
  },
  "master-slave":1,
  "scancycle":100,
  "stoprun":0,
  "type":"TCP"
}
```
- 通讯方式；string类型，取值"TCP","RTU"

- 上位机查询modbus从站参数

```
{}
```
- 命令字：0x7306

- 控制器回复上位机modbus从站参数

- 命令字：0x7307
- "RTU":

- RTU参数
- "baudrate":115200

- 波特率；int类型

- "port":2

- 端口号；int类型

- "slaveId":1

- 从站ID；int类型，范围[0,65535]

- "TCP":

- TCP参数
- "IP":"192.168.1.11"

- IP地址；默认值

- "endian_type":0

- Float大小端；int类型，范围[0,3]
- 0表示AB CD，1表示CD AB，2表示BA DC，3表示DC BA

- "port":502

- 端口号；int类型，范围[0,65535]

- "enable":false

- 连接使能；bool类型

- "master-slave":1

- modbus通讯的的主从模式；int类型，范围[0,1]
- 0表示主站，1表示从站

- "scancycle":100

- 扫描周期；int类型，范围[8,1000]ms

- "stoprun":0

- 通讯断开时操作；int类型，范围[0,1]
- 0表示不停机，1表示停机

- "type":"TCP"

```
{
  "RTU":
  {
    "baudrate":115200,
    "port":2,
    "slaveId":1
  },
  "TCP":
  {
    "IP":"192.168.1.11",
    "endian_type":0,
    "port":502
  },
  "enable":false,
  "master-slave":1,
  "scancycle":100,
  "stoprun":0,
  "type":"TCP"
}
```
- 通讯方式；string类型，取值"TCP","RTU"

- 上位机设置modbus从站连接使能

- 命令字：0x7308

- "enanle":true

```
{
  "enanle":true
}
```
- modbus从站连接使能；bool类型

- 上位机设置modbus从站心跳检测使能

- 命令字：0x7309

- "checkheart":true

```
{
  "checkheart":true
}
```
- 心跳检测使能；bool类型

- 上位机查询modbus从站心跳检测使能

```
{}
```
- 命令字：0x703A

- 控制器回复上位机modbus从站心跳检测使能

- 命令字：0x703B

- "checkheart":true

```
{
  "checkheart":true
}
```
- 心跳检测使能；bool类型

- 上位机设置modbus程序

- 命令字：0x703C

- "jobname":"AA"

- 已选程序名称

- "programid":1

- 程序序号；int类型，范围[1,300]

- "robot":1

```
{
  "jobname":"AA",
  "programid":1,
  "robot":1
}
```
- 当前机器人号

- 上位机查询modbus程序

- 命令字：0x703D

- "num":10

- 查询数量；int类型，固定为10

- "robot":1

- 当前机器人号

- "startprogramid":1

```
{
  "num":10,
  "robot":1,
  "startprogramid":1
}
```
- 查询序列起始程序序号；int类型，范围[1,30]

- 控制器回复上位机modbus程序

- 命令字：0x703E

- "jobnamelist":["AA","","","","","","","","",""]

- 程序名称列表；string类型
- 长度为10

- "robot":1

- 当前机器人号

- "startprogramid":1

- 序列起始程序序号；int类型，范围[1,30]

- "sum":300

```
{
  "jobnamelist":["AA","","","","","","","","",""],
  "robot":1,
  "startprogramid":1,
  "sum":300
}
- 可选程序总数；int类型

```