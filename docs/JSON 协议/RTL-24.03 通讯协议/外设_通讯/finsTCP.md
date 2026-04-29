# finsTCP

- 说明
- 上位机设置finsTCP参数

- 命令字：0x7340

- "IP":"192.168.1.10"

- IP地址；string类型

- "PLCReadAddress":"DM2000"

- PLC读取首地址；string类型
- 值为"DM"开头，数字int类型，范围[1,9999]

- "PLCWriteAddress":"DM1000"

- PLC写入首地址；string类型
- 值为"DM"开头，数字int类型，范围[1,9999]

- "craftNum":1

- 工艺号；int类型，范围[1,9]

- "localReadAddress":[500,500]

- 本机读取首地址列表；int类型，范围[1,990]
- 第一位为全局布尔首地址，第二位为全局整型首地址

- "localWriteAddress":[100,100]

- 本机读取首地址列表；int类型，范围[1,990]
- 第一位为全局布尔首地址，第二位为全局整型首地址

- "port":9600

```
{
  "IP":"192.168.1.10",
  "PLCReadAddress":"DM2000",
  "PLCWriteAddress":"DM1000",
  "craftNum":1,
  "localReadAddress":[500,500],
  "localWriteAddress":[100,100],
  "port":9600
}
```
- 端口号；int类型，范围[0,65535]

- 上位机查询finsTCP参数

- 命令字：0x7341

- "craftNum":1

```
{
  "craftNum":1
}
```
- 查询的工艺号名称；int类型，范围[1,9]

- 控制器回复上位机finsTCP参数

- 命令字：0x7342

- "IP":"192.168.1.10"

- IP地址；string类型

- "PLCReadAddress":"DM2000"

- PLC读取首地址；string类型
- 值为"DM"开头，数字int类型，范围[1,9999]

- "PLCWriteAddress":"DM1000"

- PLC写入首地址；string类型
- 值为"DM"开头，数字int类型，范围[1,9999]

- "craftNum":1

- 工艺号；int类型，范围[1,9]

- "localReadAddress":[500,500]

- 本机读取首地址列表；int类型，范围[1,990]
- 第一位为全局布尔首地址，第二位为全局整型首地址

- "localWriteAddress":[100,100]

- 本机读取首地址列表；int类型，范围[1,990]
- 第一位为全局布尔首地址，第二位为全局整型首地址

- "port":9600

- 端口号；int类型，范围[0,65535]

- "status":0

```
{
  "IP":"192.168.1.10",
  "PLCReadAddress":"DM2000",
  "PLCWriteAddress":"DM1000",
  "craftNum":1,
  "localReadAddress":[500,500],
  "localWriteAddress":[100,100],
  "port":9600,
  "status":0
}
```
- 通讯状态；int类型，范围[0,1]
- 0表示未连接，1表示已连接

- 上位机请求连接通讯

```
{}
```
- 命令字：0x7343

- 上位机请求断开通讯

```
{}
```
- 命令字：0x7344

- 控制器发送finsTCP通讯连接状态

- 命令字：0x7345

- "status":0

```
{
  "status":0
}
```
- 通讯连接状态；int类型，范围[0,1]

- 控制器发送fins打开的程序名称

- 命令字：0x7346

- "AAA"

```
"AAA"
- 打开的程序名称

```