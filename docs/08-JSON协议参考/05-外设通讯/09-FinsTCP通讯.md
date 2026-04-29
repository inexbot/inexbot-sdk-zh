# FinsTCP 通讯

# 1. 概述

FinsTCP 是欧姆龙（Omron）PLC 的通讯协议。纳博特控制器支持通过 FinsTCP 协议与欧姆龙 PLC 进行数据交换，包括读取/写入 DM 区数据、与 PLC 变量映射等功能。

---

# 2. 参数配置（0x7340 / 0x7341 → 0x7342）

## 设置 FinsTCP 参数（0x7340）

| 字段 | 类型 | 说明 |
|------|------|------|
| `IP` | string | PLC 的 IP 地址 |
| `port` | int | 端口号，范围[0,65535] |
| `craftNum` | int | 工艺号，范围[1,9] |
| `PLCReadAddress` | string | PLC 读取首地址，格式为 DM + 数字，范围[1,9999] |
| `PLCWriteAddress` | string | PLC 写入首地址，格式为 DM + 数字，范围[1,9999] |
| `localReadAddress` | array | 本机读取首地址列表：<br>[0]=全局布尔首地址，<br>[1]=全局整型首地址 |
| `localWriteAddress` | array | 本机写入首地址列表：<br>[0]=全局布尔首地址，<br>[1]=全局整型首地址 |

**示例：**

```json
{
  "IP": "192.168.1.10",
  "port": 9600,
  "craftNum": 1,
  "PLCReadAddress": "DM2000",
  "PLCWriteAddress": "DM1000",
  "localReadAddress": [500, 500],
  "localWriteAddress": [100, 100]
}
```

## 查询 FinsTCP 参数（0x7341 → 0x7342）

```json
{ "craftNum": 1 }
```

**响应：**

| 字段 | 类型 | 说明 |
|------|------|------|
| `IP` | string | PLC IP 地址 |
| `port` | int | 端口号 |
| `craftNum` | int | 工艺号 |
| `PLCReadAddress` | string | PLC 读取首地址 |
| `PLCWriteAddress` | string | PLC 写入首地址 |
| `localReadAddress` | array | 本机读取首地址 |
| `localWriteAddress` | array | 本机写入首地址 |
| `status` | int | 连接状态：0=未连接，1=已连接 |

---

# 3. 连接控制（0x7343 / 0x7344 / 0x7345）

## 请求连接（0x7343）

```json
{}
```

## 请求断开（0x7344）

```json
{}
```

## 连接状态推送（0x7345）

控制器主动推送连接状态：

```json
{
  "status": 0
}
```

---

# 4. 程序名称（0x7346）

控制器发送 FinsTCP 通讯打开的程序名称：

```json
"AAA"
```

---

# 5. 地址映射说明

| 地址类型 | 说明 |
|----------|------|
| PLC 读取地址 | 如 `DM2000`，表示从 PLC 的 DM2000 区开始读取 |
| PLC 写入地址 | 如 `DM1000`，表示写入 PLC 的 DM1000 区 |
| 本机布尔地址 | 机器人端全局布尔变量首地址 |
| 本机整型地址 | 机器人端全局整型变量首地址 |

---

# 6. 命令字汇总

| 命令 | 功能 | 方向 |
|------|------|------|
| 0x7340 | 设置 FinsTCP 参数 | 请求 |
| 0x7341 | 查询 FinsTCP 参数 | 请求 |
| 0x7342 | FinsTCP 参数 | 响应 |
| 0x7343 | 请求连接 | 请求 |
| 0x7344 | 请求断开 | 请求 |
| 0x7345 | 连接状态推送 | 响应 |
| 0x7346 | 程序名称推送 | 响应 |
