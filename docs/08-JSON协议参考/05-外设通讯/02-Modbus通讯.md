# Modbus 通讯

# 1. 概述

Modbus 是一种通用的工业通讯协议，纳博特控制器支持 Modbus RTU 和 Modbus TCP 两种模式。通过 JSON 协议可以配置主站/从站参数、查询连接状态、管理 Modbus 程序等。

---

# 2. 主站配置（0x7300 / 0x7301）

## 设置 Modbus 主站参数（0x7300）

**请求参数：**

| 字段 | 类型 | 说明 |
|------|------|------|
| `masterStation` | object | 主站参数配置 |
| `masterStation.type` | string | 主站类型：`"TCP"` 或 `"RTU"` |
| `masterStation.processNumber` | int | 工艺号，范围[1,9] |
| `masterStation.startAddress` | bool | 地址偏移：true=地址不变，false=自动-1 |
| `masterStation.RTU` | object | RTU 参数（type="RTU"时有效） |
| `masterStation.RTU.port` | int | 端口号 |
| `masterStation.RTU.baudrate` | int | 波特率 |
| `masterStation.RTU.dataBit` | int | 数据位，范围[5,8] |
| `masterStation.RTU.stopBit` | int | 停止位，范围[0,1] |
| `masterStation.RTU.checkBit` | string | 校验位：`"N"`(无校验)、`"E"`(偶校验)、`"O"`(奇校验) |
| `masterStation.RTU.slaveId` | int | 从站ID，范围[0,65535] |
| `masterStation.TCP` | object | TCP 参数（type="TCP"时有效） |
| `masterStation.TCP.IP` | string | IP 地址 |
| `masterStation.TCP.port` | int | 端口号，范围[0,65535] |
| `masterStation.TCP.endian_type` | int | Float 大小端：0=ABCD, 1=CDAB, 2=BADC, 3=DCBA |

**响应：** 0x7302

## 查询 Modbus 主站参数（0x7301 → 0x7302）

**请求参数：**

```json
{
  "processNumber": 1
}
```

**响应参数：** 同设置参数，额外包含：
- `modbus_state`：连接状态（bool）
- `response_time_out`：读写响应时间（ms）

## 查询 Modbus 连接状态（0x7303 → 0x7304）

**响应：**

```json
{
  "ModbusConnect": false
}
```

---

# 3. 从站配置（0x7305 / 0x7306）

## 设置 Modbus 从站参数（0x7305）

| 字段 | 类型 | 说明 |
|------|------|------|
| `type` | string | 通讯方式：`"TCP"` 或 `"RTU"` |
| `master-slave` | int | 模式：0=主站，1=从站 |
| `scancycle` | int | 扫描周期，范围[8,1000]ms |
| `stoprun` | int | 通讯断开操作：0=不停机，1=停机 |
| `RTU` | object | RTU 参数 |
| `RTU.port` | int | 端口号 |
| `RTU.baudrate` | int | 波特率 |
| `RTU.slaveId` | int | 从站ID |
| `TCP` | object | TCP 参数 |
| `TCP.IP` | string | IP 地址（默认 `192.168.1.11`） |
| `TCP.port` | int | 端口号，范围[0,65535] |
| `TCP.endian_type` | int | Float 大小端 |

## 查询 Modbus 从站参数（0x7306 → 0x7307）

响应格式同设置，额外包含：
- `enable`：连接使能（bool）

## 设置/查询从站连接使能（0x7308 / 0x703A → 0x703B）

```json
{ "enanle": true }   // 注意：原文档拼写为 "enanle"
```

## 心跳检测（0x7309 / 0x703A → 0x703B）

```json
{ "checkheart": true }
```

---

# 4. Modbus 程序管理（0x703C / 0x703D → 0x703E）

## 设置 Modbus 程序（0x703C）

| 字段 | 类型 | 说明 |
|------|------|------|
| `robot` | int | 机器人号，范围[1,4] |
| `programid` | int | 程序序号，范围[1,300] |
| `jobname` | string | 程序名称 |

```json
{
  "robot": 1,
  "programid": 1,
  "jobname": "AA"
}
```

## 查询 Modbus 程序列表（0x703D → 0x703E）

**请求：**

| 字段 | 类型 | 说明 |
|------|------|------|
| `robot` | int | 机器人号 |
| `startprogramid` | int | 起始程序号，范围[1,30] |
| `num` | int | 查询数量（固定10） |

**响应：**

| 字段 | 类型 | 说明 |
|------|------|------|
| `robot` | int | 机器人号 |
| `startprogramid` | int | 起始程序号 |
| `sum` | int | 可选程序总数（300） |
| `jobnamelist` | array | 程序名称列表（长度10） |

---

# 5. 参数说明

## 大小端类型

| 值 | 格式 | 说明 |
|----|------|------|
| 0 | ABCD | Big-Endian（高位在前） |
| 1 | CDAB | Little-Endian（低位在前） |
| 2 | BADC | 混合字节序 |
| 3 | DCBA | 反转字节序 |

## 通讯参数默认值

| 参数 | TCP 默认值 | RTU 默认值 |
|------|-----------|-----------|
| 端口 | 502 | - |
| 波特率 | - | 115200 |
| 数据位 | - | 8 |
| 停止位 | - | 1 |
| 校验位 | - | 无校验(N) |
| 从站ID | - | 1 |
