# Tcp通讯

- 说明
- 上位机设置上位机Tcp通讯参数

- 命令字：0x7320

- "client":

- 客户端参数，"type"节点为1是该节点存在
- "frameHeader":"@"

- 数据帧头；string类型
- 留空为没有

- "ip":"192.168.1.111"

- 需要连接的服务器IP；string类型

- "numberSystem":0

- 接收到的数据以何种进制解析；int类型，范围[0,1]
- 0表示十进制，1表示十六进制

- "port":9000

- 通讯端口；int类型，范围(0,65535]

- "separator":","

- 数据分隔符；string类型

- "terminator":"!"

- 数据帧尾；string类型

- 留空为没有

- "craft":1

- 工艺号；int类型，范围[1,9]

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "server":

- 服务器参数，"type"节点为0是该节点存在
- "frameHeader":"@"

- 数据帧头；string类型
- 留空为没有

- "ip":"192.168.0.229"

- 当前用作服务器IP；string类型

- "numberSystem":0

- 接收到的数据以何种进制解析；int类型，范围[0,1]
- 0表示十进制，1表示十六进制

- "port":9000

- 通讯端口；int类型，范围(0,65535]

- "separator":","

- 数据分隔符；string类型

- "terminator":"!"

- 数据帧尾；string类型

- 留空为没有

- "type":1

```
{
  "client":
  {
    "frameHeader":"@",
    "ip":"192.168.1.111",
    "numberSystem":0,
    "port":9000,
    "separator":",",
    "terminator":"!"
  },
  "craft":1,
  "robot":1,
  "server":
  {
    "frameHeader":"@",
    "ip":"192.168.0.229",
    "numberSystem":0,
    "port":9001,
    "separator":",",
    "terminator":"!"
  },
  "type":1
}
```
- TCP通讯方式；int类型，范围[0,1]
- 0表示服务器，1表示客户端，2表示配置文件

- 上位机查询Tcp通讯参数

- 命令字：0x7321

- "craft":1

- 工艺号；int类型，范围[1,9]

- "robot":1

- 机器人号；int类型，范围[1,4]

- "type":2

```
{
  "craft":1,
  "robot":1,
  "type":2
}
```
- TCP通讯方式；int类型，范围[0,2]
- 0表示服务器，1表示客户端，2表示配置文件
- 2时控制器发送服务器参数

- 控制器回复上位机Tcp通讯参数

- 命令字：0x7322

- "client":

- 客户端参数，"type"节点为1是该节点存在
- "frameHeader":"@"

- 数据帧头；string类型
- 留空为没有

- "ip":"192.168.1.111"

- 需要连接的服务器IP；string类型

- "numberSystem":0

- 接收到的数据以何种进制解析；int类型，范围[0,1]
- 0表示十进制，1表示十六进制

- "port":9000

- 通讯端口；int类型，范围(0,65535]

- "separator":","

- 数据分隔符；string类型

- "terminator":"!"

- 数据帧尾；string类型

- 留空为没有

- "craft":1

- 工艺号；int类型，范围[1,9]

- "robot":1

- 当前机器人号；int类型，范围[1,4]

- "server":

- 服务器参数，"type"节点为0是该节点存在
- "frameHeader":"@"

- 数据帧头；string类型
- 留空为没有

- "ip":"192.168.0.229"

- 当前用作服务器IP；string类型

- "numberSystem":0

- 接收到的数据以何种进制解析；int类型，范围[0,1]
- 0表示十进制，1表示十六进制

- "port":9000

- 通讯端口；int类型，范围(0,65535]

- "separator":","

- 数据分隔符；string类型

- "terminator":"!"

- 数据帧尾；string类型

- 留空为没有

- "type":1

```
{
  "client":
  {
    "frameHeader":"@",
    "ip":"192.168.1.111",
    "numberSystem":0,
    "port":9000,
    "separator":",",
    "terminator":"!"
  },
  "craft":1,
  "robot":1,
  "server":
  {
    "frameHeader":"@",
    "ip":"192.168.0.229",
    "numberSystem":0,
    "port":9001,
    "separator":",",
    "terminator":"!"
  },
  "type":1
}
```
- TCP通讯方式；int类型，范围[0,1]
- 0表示服务器，1表示客户端，2表示配置文件

- 上位机请求连接Tcp通讯

- 命令字：0x7323

- "craft":1

- 工艺号；int类型，范围[1,9]

- "robot":1

```
{
  "craft":1,
  "robot":1
}
```
- 机器人号；int类型，范围[1,4]

- 上位机请求断开Tcp通讯

- 命令字：0x7324

- "craft":1

- 工艺号；int类型，范围[1,9]

- "robot":1

```
{
  "craft":1,
  "robot":1
}
- 机器人号；int类型，范围[1,4]

```