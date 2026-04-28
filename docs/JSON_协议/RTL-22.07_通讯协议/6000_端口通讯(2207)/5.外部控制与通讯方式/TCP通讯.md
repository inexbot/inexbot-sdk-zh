# TCP通讯

#### 设置网络参数

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/ShK7YUZh/resources/-14A5nnaLpE3IuUoGbMaqOVeqAvT3zO9j_hHbz24gME.png)

*0x4180  MSGCOMM_PARAM_SET

##### #客户端

{

"client":{  //客户端

"frameHeader":"@",   //帧头

"ip":"192.168.1.111",  //IP

"numberSystem":1,    //0:十进制,1:十六进制

"port":9000,       //端口

"separator":",",    //分隔符

"terminator":"!"   //结束符

},

"craft":1,   //工艺号 1~9

"robot":1,

"type":1     //0: 服务器；1：客户端

}

##### #服务端

{

"craft":3,    //工艺号 1~9

"robot":1,

"server":{   //服务端

"frameHeader":"@A", //帧头

"ip":"192.168.1.14", //IP

"numberSystem":0,   //0:十进制,1:十六进制

"port":9001,    //端口

"separator":"B",   //分隔符

"terminator":"C"  //结束符

},

"type":0  //0: 服务器；1：客户端

}

#### 查询网络参数

*0x4181  MSGCOMM_PARAM_INQUIRE

{

"robot":1,

"craft":1,

"type":2  //0：服务器 ，1：客户端

}

#### 响应网络参数查询

##### #客户端：

*0x4182  MSGCOMM_PARAM_RESPOND

{

"client":{

"frameHeader":"@",  //帧头

"ip":"192.168.1.111",  //IP

"numberSystem":0,  //0:十进制,1:十六进制

"port":9000,    //端口

"separator":",",    //分隔符

"terminator":"!"   //结束符

},

"craft":1,  //工艺号

"netState":false,  //true:连接，false:断开 //比设置多一个状态

"robot":1,

"type":1  //0：服务器，1：客户端

}

##### #服务端

{

"craft":1,  //工艺号

"netState":false,    //true:连接，false:断开 //比设置多一个状态

"robot":1,

"server":{

"frameHeader":"@",   //帧头

"ip":"192.168.1.14",  //IP

"numberSystem":0,   //0:十进制,1:十六进制

"port":22,    //端口

"separator":",",    //分隔符

"terminator":"!"  //结束符

},

"type":0   //0：服务器，1：客户端

}

#### 连接MSGCOMM网络

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/ShK7YUZh/resources/MLpO0ndpaZfngPejXMxZua_TCjNcQXDSFpv5pLotmto.png)

*0x4183  MSGCOMM_DEVICE_CONNECT

{

"robot":1,

"craft":1

}

#### 关闭MSGCOMM网络

*0x4184  MSGCOMM_DEVICE_CLOSE

{

"robot":1,

"craft":1

}
