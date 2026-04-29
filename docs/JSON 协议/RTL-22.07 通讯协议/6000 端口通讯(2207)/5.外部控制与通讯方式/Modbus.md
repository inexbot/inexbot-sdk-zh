# Modbus

#### 设置Modbus程序 发送下列命令：

*0x5701 EXTERN_PROGRAM_SET

{

"robot":1			//机器人1-4

"programid":1			//程序id  1-300

"jobname":xxxx			//作业文件名 没有后缀

}

#### 查询Modbus程序 发送下列命令：

*0x5702 EXTERN_PROGRAM_INQUIRE

{

"robot":1			//机器人1-4

"startprogramid":1		//程序起始id

"num":10			//需要获取的程序个数  1-10

}

#### 查询Modbus程序时，控制器返回的值

*0x5703 EXTERN_PROGRAM_RESPOND

{

"robot":1			//机器人1-4

"startprogramid":1		//程序起始id

"jobnamelist":["xxx","","yyyy"]	//十个数据 一个都没有就发10个""

}

#### 设置控制器的modbus的类型

- 命令字：0x5711

- "baudrate": 115200

- string 类型
- Modbus RTU通信的波特率

- "port": 2

- int 类型
- Modbus RTU通信的串口号

- "slaveId": 1

- int 类型
- Modbus RTU通信的从设备ID

- "IP": "192.168.1.11"

- string 类型
- Modbus TCP通信的服务器IP地址

- "port": 502

- int 类型
- Modbus TCP通信的端口号

- "master-slave": 1

- string 类型
- Modbus通信的主从模式，0表示主模式，1表示从模式

- "scancycle": 100

- int 类型
- Modbus通信的扫描周期，单位毫秒

- "stoprun": 0

- Bool 类型
- Modbus通信的运行停止标志，0表示未停止，1表示停止

- "type": "TCP"

```
{
    "RTU": {
        "baudrate": 115200,  
        "port": 2,           
        "slaveId": 1         
    },
    "TCP": {
        "IP": "192.168.1.11",  
        "port": 502            
    },
    "master-slave": 1,    
    "scancycle": 100,     
    "stoprun": 0,         
    "type": "TCP"         
}
```
#### 控制器的modbus类型查询

- string 类型
- Modbus通信的类型，可以是RTU或TCP

- 命令字：0x5712

```
{
}
```
#### 控制器类型查询后像上位机发送

- "date": 无

- 命令字：0x5713

- "baudrate": 115200

- string 类型
- Modbus RTU通信的波特率

- "port": 2

- int 类型
- Modbus RTU通信的串口号

- "slaveId": 1

- int 类型
- Modbus RTU通信的从设备ID

- "IP": "192.168.1.11"

- string 类型
- Modbus TCP通信的服务器IP地址

- "port": 502

- int 类型
- Modbus TCP通信的端口号

- "enable": true

- bool 类型
- 是否启用Modbus通信

- "master-slave": 1

- string 类型
- Modbus通信的主从模式，0表示主模式，1表示从模式

- "scancycle": 100

- int 类型
- Modbus通信的扫描周期，单位毫秒

- "stoprun": 0

- Bool 类型
- Modbus通信的运行停止标志，0表示未停止，1表示停止

- "type": "TCP"

```
{
    "RTU": {
        "baudrate": 115200,     
        "port": 2,              
        "slaveId": 1            
    },
    "TCP": {
        "IP": "192.168.1.11",   
        "port": 502             
    },
    "enable": true,            
    "master-slave": 1,         
    "scancycle": 100,          
    "stoprun": 0,             
    "type": "TCP"             
}
```
#### 控制器modbus使能

- string 类型
- Modbus通信的类型，可以是RTU或TCP

- 命令字：0x5714

- "enable":false

```
{
  "enable":false
}
```
#### modbus 设置心跳检测

*0x5715  MODBUS_CHECKHEART_SET

{

"checkheart":true   //modbus心跳检测

}

#### Modbus查询心跳检测

*0x5716    MODBUS_CHECKHEART_INQUIRE

{

}

#### 控制器回复Modbus心跳检测

*0x5717    MODBUS_CHECKHEART_RESPOND

{

"checkheart":true    //modbus心跳检测

}

#### 控制器作为从站是否连接查询

- bool 类型
- 是否启用Modbus通信

```
{
}
```
date:  无

#### 控制器作为从站在上位机查询是否连接时发送

- 命令字：0x5718

```
{
  "ModbusConnect":false
}
```
"ModbusConnect":    false未连接/true连接

#### 控制器作为主站的参数设置

- 命令字：0x5719

```
{
    "masterStation": {
        "RTU": {
            "baudrate": 115200,
            "checkBit": "E",
            "dataBit": 5,
            "port": 2,
            "slaveId": 1,
            "stopBit": 1
        },
        "TCP": {
            "IP": "192.168.10.56",
            "port": 503
        },
        "processNumber": 1,
        "type": "TCP"
    },
    "startAddress": false
}


```
"masterStation": {                           // 主站配置信息

"RTU": {                                // RTU通信配置

"baudrate": 115200,                 // 波特率为115200

"checkBit": "E",                    // 校验位为偶校验

"dataBit": 5,                       // 数据位为5

"port": 2,                          // 串口号为2

"slaveId": 1,                       // 从设备ID为1

"stopBit": 1                        // 停止位为1

},

"TCP": {                                // TCP通信配置

"IP": "192.168.10.56",              // IP地址为192.168.10.56

"port": 503                         // 端口号为503

},

"processNumber": 1,                     //工艺号为1

"type": "TCP"                           // 通信类型为TCP

},

"startAddress": false                       // 起始地址为假，即未启用起始地址

#### 查询控制器作为主站时的信息

- 命令字：0x5744

```
{
  "processNumber":2
}
```
"processNumber":  工艺号

#### 查询之后控制器向上位机发送

- 命令字：0x5745

```
{
    "RTU": {
        "baudrate": 115200,
        "checkBit": "E",
        "dataBit": 5,
        "port": 3,
        "slaveId": 56,
        "stopBit": 1
    },
    "TCP": {
        "IP": "192.168.1.14",
        "port": 503
    },
    "modbus_state": false,
    "response_time_out": 100,
    "startAddress": true,
    "type": "RTU"
}


```
"RTU": {                                    // RTU通信配置

"baudrate": 115200,                     // 波特率为115200

"checkBit": "E",                        // 校验位为偶校验

"dataBit": 5,                           // 数据位为5

"port": 3,                              // 串口号为3

"slaveId": 56,                          // 从设备ID为56

"stopBit": 1                            // 停止位为1

},

"TCP": {                                    // TCP通信配置

"IP": "192.168.1.14",                   // IP地址为192.168.1.14

"port": 503                             // 端口号为503

},

"modbus_state": false,                      // MODBUS状态为假，即未启用MODBUS

"response_time_out": 100,                   // 响应超时时间为100毫秒

"startAddress": true,                       // 启用起始地址

"type": "RTU"                               // 通信类型为RTU

- 命令字：0x5746
