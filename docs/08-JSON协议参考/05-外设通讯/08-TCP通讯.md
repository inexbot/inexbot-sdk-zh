# TCP 通讯

# 1. 概述

纳博特控制器支持 TCP 客户端/服务器两种通讯模式。通过 JSON 协议可以配置 TCP 通讯参数、建立/断开连接、设置数据帧格式（帧头、分隔符、帧尾）等。

---

# 2. 参数配置（0x7320 / 0x7321 → 0x7322）

## 设置 TCP 通讯参数（0x7320）

| 字段 | 类型 | 说明 |
|------|------|------|
| `robot` | int | 机器人号，范围[1,4] |
| `craft` | int | 工艺号，范围[1,9] |
| `type` | int | 通讯方式：0=服务器，1=客户端，2=配置文件 |
| `client` | object | 客户端参数（type=1时存在） |
| `client.ip` | string | 服务器 IP |
| `client.port` | int | 端口号，范围(0,65535] |
| `client.frameHeader` | string | 数据帧头（留空表示无） |
| `client.terminator` | string | 数据帧尾（留空表示无） |
| `client.separator` | string | 数据分隔符 |
| `client.numberSystem` | int | 数据进制：0=十进制，1=十六进制 |
| `server` | object | 服务器参数（type=0时存在） |
| `server.ip` | string | 本机作为服务器的 IP |
| `server.port` | int | 端口号 |
| `server.frameHeader` | string | 数据帧头 |
| `server.terminator` | string | 数据帧尾 |
| `server.separator` | string | 数据分隔符 |
| `server.numberSystem` | int | 数据进制 |

**示例（客户端模式）：**

```json
{
  "robot": 1,
  "craft": 1,
  "type": 1,
  "client": {
    "ip": "192.168.1.111",
    "port": 9000,
    "frameHeader": "@",
    "terminator": "!",
    "separator": ",",
    "numberSystem": 0
  }
}
```

**示例（服务器模式）：**

```json
{
  "robot": 1,
  "craft": 1,
  "type": 0,
  "server": {
    "ip": "192.168.0.229",
    "port": 9001,
    "frameHeader": "@",
    "terminator": "!",
    "separator": ",",
    "numberSystem": 0
  }
}
```

## 查询 TCP 通讯参数（0x7321 → 0x7322）

**请求：**

| 字段 | 类型 | 说明 |
|------|------|------|
| `robot` | int | 机器人号 |
| `craft` | int | 工艺号 |
| `type` | int | 查询类型：0=服务器参数，1=客户端参数，2=配置文件 |

---

# 3. 连接控制（0x7323 / 0x7324）

## 请求连接（0x7323）

```json
{
  "robot": 1,
  "craft": 1
}
```

## 请求断开（0x7324）

```json
{
  "robot": 1,
  "craft": 1
}
```

---

# 4. 数据帧格式说明

| 字段 | 说明 |
|------|------|
| frameHeader | 帧头，如 `"@"` |
| terminator | 帧尾，如 `"!"` |
| separator | 数据分隔符，如 `","` |

示例数据：`@100,200,300!`
- 帧头：`@`
- 数据：`100,200,300`（用逗号分隔）
- 帧尾：`!`

---

# 5. 命令字汇总

| 命令 | 功能 | 方向 |
|------|------|------|
| 0x7320 | 设置 TCP 参数 | 请求 |
| 0x7321 | 查询 TCP 参数 | 请求 |
| 0x7322 | TCP 参数 | 响应 |
| 0x7323 | 请求连接 | 请求 |
| 0x7324 | 请求断开 | 请求 |
