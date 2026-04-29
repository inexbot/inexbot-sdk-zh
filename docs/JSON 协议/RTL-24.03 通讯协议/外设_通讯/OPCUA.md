# OPCUA

- 说明
- 上位机设置OPCUA参数

- 命令字：0x7350

- "client":

- 客户端参数
- "enable":false

- 连接使能；bool类型

- "ip":"192.168.1.240"

- 服务器IP地址；string类型

- "port":49400

- 端口号；int类型，范围[0,65535]

- "resource":"ProsysServer"

- 服务器名称；string类型

- "server":

- 服务器参数
- "enable":false

- 连接使能；bool类型

- "ip":"192.168.0.229"

- 控制器用作服务器时的IP地址；string类型

- "port":4840

```
{
  "client":
  {
    "enable":false,
    "ip":"192.168.1.240",
    "port":49400,
    "resource":"ProsysServer"
  },
  "server":
  {
    "enable":false,
    "ip":"192.168.0.229",
    "port":4840
  }
}
```
- 端口号；int类型，范围[0,65535]

- 上位机查询OPCUA参数

```
{}
```
- 命令字：0x7351

- 控制器回复上位机OPCUA参数

- 命令字：0x7352

- "client":

- 客户端参数
- "enable":false

- 连接使能；bool类型

- "ip":"192.168.1.240"

- 服务器IP地址；string类型

- "port":49400

- 端口号；int类型，范围[0,65535]

- "resource":"ProsysServer"

- 服务器名称；string类型

- "server":

- 服务器参数
- "enable":false

- 连接使能；bool类型

- "ip":"192.168.0.229"

- 控制器用作服务器时的IP地址；string类型

- "port":4840

```
{
  "client":
  {
    "enable":false,
    "ip":"192.168.1.240",
    "port":49400,
    "resource":"ProsysServer"
  },
  "server":
  {
    "enable":false,
    "ip":"192.168.0.229",
    "port":4840
  }
}
- 端口号；int类型，范围[0,65535]

```