# OPC UA 通讯

# 1. 概述

OPC UA（Open Platform Communications Unified Architecture）是一种跨平台的工业通讯标准。纳博特控制器同时支持 OPC UA 客户端和服务器两种模式，可与不同厂商的 OPC UA 设备进行通讯。

---

# 2. 参数配置（0x7350 / 0x7351 → 0x7352）

## 设置 OPC UA 参数（0x7350）

纳博特控制器可作为客户端连接外部 OPC UA 服务器，也可作为服务器被外部设备连接。

| 字段 | 类型 | 说明 |
|------|------|------|
| `client` | object | 客户端参数 |
| `client.enable` | bool | 连接使能 |
| `client.ip` | string | 服务器 IP 地址 |
| `client.port` | int | 端口号，范围[0,65535] |
| `client.resource` | string | 服务器名称 |
| `server` | object | 服务器参数 |
| `server.enable` | bool | 连接使能 |
| `server.ip` | string | 控制器作为服务器时的 IP 地址 |
| `server.port` | int | 端口号，范围[0,65535] |

**示例：**

```json
{
  "client": {
    "enable": false,
    "ip": "192.168.1.240",
    "port": 49400,
    "resource": "ProsysServer"
  },
  "server": {
    "enable": false,
    "ip": "192.168.0.229",
    "port": 4840
  }
}
```

## 查询 OPC UA 参数（0x7351 → 0x7352）

无请求数据，响应格式同设置参数。

---

# 3. 端口说明

| 模式 | 默认端口 | 说明 |
|------|---------|------|
| 客户端 | 49400 | 连接远程 OPC UA 服务器 |
| 服务器 | 4840 | 被远程客户端连接 |

---

# 4. 使用场景

## 客户端模式
控制器主动连接外部 OPC UA 服务器，读取服务器数据或向服务器写入数据。

## 服务器模式
控制器作为 OPC UA 服务器，允许外部客户端（如 SCADA 系统）连接并访问控制器数据。
