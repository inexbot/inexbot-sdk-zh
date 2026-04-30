# 指令-FINSTCP类

### 打开FINSTCP连接

- 说明：
- 用于在运行模式下打开FINSTCP通讯连接
- 打开FINSTCP连接
- 指令名：FINSTCP_OPEN
- "ID":5
- FINSTCP主站工艺号；int类型；取值范围[1,9]
- "logout":false
- 是否被注释；bool类型
- true：在作业文件中将不执行该指令；false：未被注释，可执行
- "type":215
- 打开FINSTCP连接在枚举数列type中为210
- "userParamInt":0
- 二次开发中客户自定义，目前无意义
- "userParamString":""

```json
{
  "ID":5,
  "logout":false,
  "type":215,
  "userParamInt":0,
  "userParamString":"",
  "variable":{"data":0.0,"secondvalue":0,"value":0,"varname":""}
}
```
### 断开FINSTCP连接

- 二次开发中客户自定义，目前无意义
- 说明：
- 在运行模式下断开FINSTCP通讯连接
- 断开FINSTCP连接
- 指令名：FINSTCP_CLOSE
- "ID":9
- FINSTCP主站工艺号；int类型；取值范围[1,9]
- "logout":false
- 是否被注释；bool类型
- true：在作业文件中将不执行该指令；false：未被注释，可执行
- "type":216
- FINSTCP_CLOSE在枚举数列type中为216
- "userParamInt":0
- 二次开发中客户自定义，目前无意义
- "userParamString":""

```json
{
  "ID":9,
  "logout":false,
  "type":216,
  "userParamInt":0,
  "userParamString":"",
}
```
### FINSTCP连接状态

- 二次开发中客户自定义，目前无意义
- 说明：
- 在运行模式下获取FINSTCP连接状态
- 断开FINSTCP连接
- 指令名：FINSTCP_CONNECTION_STATUS
- "ID":5
- FINSTCP主站工艺号；int类型；取值范围[1,9]
- "logout":false
- 是否被注释；bool类型
- true：在作业文件中将不执行该指令；false：未被注释，可执行
- "type":216
- FINSTCP_CONNECTION_STATUS在枚举数列type中为216
- "userParamInt":0
- 二次开发中客户自定义，目前无意义
- "userParamString":""
- 二次开发中客户自定义，目前无意义
- "variable":{"data":0.0,"secondvalue":1,"value":6,"varname":"GB[I001]"}

```json
{
  "ID":5,
  "logout":false,
  "type":217,
  "userParamInt":0,
  "userParamString":"",
  "variable":{"data":0.0,"secondvalue":1,"value":6,"varname":"GB[I001]"}
}
```
- FINSTCP的连接状态；bool类型变量或绑定变量，全局或局部
- true：连接；false：未连接
```