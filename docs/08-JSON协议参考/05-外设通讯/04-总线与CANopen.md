# 总线与 CANopen

# 1. 概述

纳博特控制器支持 CANopen 总线通讯和 EtherCAT ENI 文件配置。通过 JSON 协议可以查询总线能力、配置 CAN 参数、查询/切换 ENI 文件、获取从站列表等。

---

# 2. CANopen

## 2.1 查询 CAN 支持的功能（0x7000 → 0x7001）

查询硬件是否支持指定 CAN 功能。

**请求参数：**

| 字段 | 类型 | 说明 |
|------|------|------|
| `canPort` | int | CAN 端口号 |
| `function` | int | 功能类型：0=标准帧，1=扩展帧，2=远程帧，3=过滤ID |

```json
{
  "canPort": 1,
  "function": 0
}
```

**响应：**

```json
{
  "canPort": 1,
  "support": true
}
```

## 2.2 设置 CAN 参数（0x7002）

配置 CAN 通讯参数。

| 字段 | 类型 | 说明 |
|------|------|------|
| `canPort` | int | CAN 端口号 |
| `canBaud` | int | 通讯波特率 |
| `frameFormat` | int | 帧格式：0=标准帧，1=扩展帧 |
| `enableRecvFiltert` | bool | 是否开启过滤ID |
| `recvFilterId` | int | 过滤ID |

```json
{
  "canPort": 1,
  "canBaud": 115200,
  "frameFormat": 0,
  "enableRecvFiltert": true,
  "recvFilterId": 1
}
```

## 2.3 接收 CAN 数据（0x7003 → 0x7004）

**请求接收（0x7003）：**

```json
{ "canPort": 1 }
```

**接收结果（0x7004）：**

| 字段 | 类型 | 说明 |
|------|------|------|
| `canPort` | int | CAN 端口号 |
| `recvCanID` | int | 接收到的帧ID |
| `Length` | int | 数据长度 |
| `data` | array | 接收到的数据 |

```json
{
  "canPort": 1,
  "recvCanID": 1,
  "Length": 1,
  "data": [10]
}
```

## 2.4 发送 CAN 数据（0x7005）

| 字段 | 类型 | 说明 |
|------|------|------|
| `canPort` | int | CAN 端口号 |
| `sendCanID` | int | 发送帧ID |
| `sendLen` | int | 数据长度，范围[1,8] |
| `data` | array | 发送数据 |
| `useRemoteFrame` | bool | 是否使用远程帧 |

```json
{
  "canPort": 1,
  "sendCanID": 1,
  "sendLen": 1,
  "data": [10],
  "useRemoteFrame": true
}
```

---

# 3. EtherCAT ENI 文件

ENI（EtherCAT Network Information）文件是 EtherCAT 从站的配置文件。

## 3.1 查询 ENI 文件列表（0x7010 → 0x7011）

**请求：**

| 字段 | 类型 | 说明 |
|------|------|------|
| `num` | int | 获取方式：1=获取当前ENI文件，10=获取所有ENI文件 |

```json
{ "num": 10 }
```

**响应：**

| 字段 | 类型 | 说明 |
|------|------|------|
| `ENIfilenum` | int | ENI 文件数目 |
| `ENIfilelist` | array | ENI 文件名列表 |
| `absolutepath` | string | ENI 文件所在文件夹 |

```json
{
  "ENIfilenum": 10,
  "ENIfilelist": ["INEXBOT-IO-R4-1.xml", "DST_X503-1.json", "DST_X503-1.xml"],
  "absolutepath": "eni/"
}
```

## 3.2 查询 ENI 参数（0x7012 → 0x7013）

**响应：**

| 字段 | 类型 | 说明 |
|------|------|------|
| `ENIName` | string | ENI 文件名 |
| `isHaveENI` | int | ENI 识别结果：-1=无ENI，0=未识别，1=已识别 |

```json
{
  "ENIName": "eni-RC-6-mecat-1-1000.xml",
  "isHaveENI": 1
}
```

---

# 4. 从站列表（0x7020 → 0x7021）

## 查询从站列表（0x7020 → 0x7021）

```json
{}
```

**响应：**

| 字段 | 类型 | 说明 |
|------|------|------|
| `servoNum` | array | 伺服从站列表 |
| `IONum` | array | IO 从站列表 |
| `slaveType` | array | 从站中文名称列表 |
| `slaveTypeEnglish` | array | 从站英文名称列表 |

```json
{
  "servoNum": [1, 2, 3, 4, 5, 6],
  "IONum": [0, 0, 0, 0, 0, 0],
  "slaveType": ["禾川X3E", "禾川X3E", "禾川X3E", "禾川X3E", "禾川X3E", "禾川X3E"],
  "slaveTypeEnglish": ["hcfa_x3e", "hcfa_x3e", "hcfa_x3e", "hcfa_x3e", "hcfa_x3e", "hcfa_x3e"]
}
```

---

# 5. 系统切换（0x7022）

请求控制器切换系统。

```json
{}
```

---

# 6. 命令字汇总

| 命令 | 功能 | 方向 |
|------|------|------|
| 0x7000 | 查询 CAN 支持的功能 | 请求 |
| 0x7001 | 查询 CAN 支持的功能 | 响应 |
| 0x7002 | 设置 CAN 参数 | 请求 |
| 0x7003 | 请求接收 CAN 数据 | 请求 |
| 0x7004 | 接收 CAN 数据结果 | 响应 |
| 0x7005 | 发送 CAN 数据 | 请求 |
| 0x7010 | 查询 ENI 文件列表 | 请求 |
| 0x7011 | ENI 文件列表 | 响应 |
| 0x7012 | 查询 ENI 参数 | 请求 |
| 0x7013 | ENI 参数 | 响应 |
| 0x7020 | 查询从站列表 | 请求 |
| 0x7021 | 从站列表 | 响应 |
| 0x7022 | 切换系统 | 请求 |
