# 激光切割工艺

## IO端口设置

io端口设置

*0x4401 LASER_IOPORT_SET

{

"IO":

{

"DO_backMiddle":0,		//回中

"DO_liftUp":0,			//上抬

"DO_follow":0,			//跟随

"DO_lightGate":0,			//光闸

"DO_aspiration":0,			//吹气

"DOFeedCoolGas":0,          //冷却气

"DOCleanNozzle":0，         //喷嘴清洁

"DI_liftUpArrival":0,		//停靠到位

"DI_backMiddleArrival":0,		//回中到位

"DI_followArrival":0,		//跟随到位

"DI_perforateArrival":0,		//穿孔到位

"DI_laserFault":0,			//激光故障

"DI_regulatorFault":0,		//调高器故障

"DI_watercoolerFault":0,		//水冷机故障

"DI_pressureFault":0,		//气压故障

"AO_pressure":0,			//气压

"AO_laserPower":0		//激光功率

}

}

IO端口查询：

*0x4402 LASER_IOPORT_INQUIRE

data：无

控制器返回：

*0x4403 LASER_IOPORT_RESPOND

同0x4401

## 全局参数设置

*0x4404 LASER_EQUIPMENT_SET

{

"equipment":

{

"arrivalOutLightMode":0,	//0:到位出光模式、1:直接出光模式,int型

"preAspiratedTime":0,	//提前送气时间,double型

"waitLiftUpTime":0,	//等待上抬时间,double型

"waitFollowTime":0,	//等待跟随时间,double型

"RetreatDistance":0,	//回退距离,double型

"delAspiratedMode":0,	//关气模式,0:延后关气,1:提前关气,int型

"delAspiratedTime":0	//关气时间,double型

},

"perforate":

{

"time":0,			//穿孔时间,double型

"pressure":0,		//穿孔气压,double型

"power":0,		//穿孔功率,int型

"freq":0,			//穿孔频率,int型

"dutyRatio":0		//穿孔占空比,int型

}

}

全局参数查询：

*0x4405 LASER_EQUIPMENT_INQUIRE

data：无

控制器返回：

*0x4406 LASER_EQUIPMENT_RESPOND

同0x4404

## 模拟量匹配设置

*0x4407 LASER_ANALOGMATCH_SET

{

"analogMatch":

{

"laserPower":		    //激光功率

{

"x1":0,			//x轴第1个参数，double型

"x2":0,			//x轴第2个参数，double型

"y1":0,			//y轴第1个参数，double型

"y2":0			//y轴第2个参数，double型

},

"pressure":		    //气压

{

"x1":0,			//x轴第1个参数，double型

"x2":0,			//x轴第2个参数，double型

"y1":0,			//y轴第1个参数，double型

"y2":0			//y轴第2个参数，double型

}

}

}

模拟量匹配查询：

*0x4408 LASER_ANALOGMATCH_INQUIRE

data：无

控制器返回：

*0x4409 LASER_ANALOGMATCH_RESPOND

{

"IO":

{

"laserPower":0,		    //激光功率端口号，int型

"pressure":0		    //气压端口号，int型

},

"analogMatch":

{

"laserPower":		    //激光功率

{

"x1":0,			//x轴第1个参数，double型

"x2":0,			//x轴第2个参数，double型

"y1":0,			//y轴第1个参数，double型

"y2":0			//y轴第2个参数，double型

},

"pressure":		    //气压

{

"x1":0,			//x轴第1个参数，double型

"x2":0,			//x轴第2个参数，double型

"y1":0,			//y轴第1个参数，double型

"y2":0			//y轴第2个参数，double型

}

}

}

## 切割参数设置

*0x440A LASER_CUTPARM_SET

{

"num":1,				//工艺号，int型

"cut":

{

"pressure":0,			//气压，double型

"power":0,			//功率，int型

"freq":0,				//频率，int型

"dutyRatio":0			//占空比，int型

}

}

切割参数查询：

*0x440B LASER_CUTPARM_INQUIRE

{

"num":1,				//工艺号

}

控制器返回：

*0x440C LASER_CUTPARM_RESPOND

同0x440A

## 状态查看查询

*0x440E LASER_STATE_INQUIRE

data：无

控制器返回：

*0x440F LASER_STATE_RESPOND

{

"liftUpArrival":false,		//停靠到位，bool型

"backMiddleArrival":false,		//回中到位，bool型

"followArrival":false,		//跟随到位，bool型

"perforateArrival":false,		//穿孔到位，bool型

"lightGateEnable":false,		//光闸使能，bool型

"laserFault":false,			//激光故障，bool型

"regulatorFault":false,		//调高器故障，bool型

"watercoolerFault":false,		//水冷机故障，bool型

"pressureFault":false,		//气压故障，bool型

"currentPressure":0,		//当前气压，double型

"currentPower":0,			//当前功率，int型

"currentFreq":0,			//当前频率，int型

"currentDutyRatio":0		//当前占空比，int型

}

## 点射参数设置

*0x4410 LASER_SHOTPARM_SET

{

"shotPower":0,			//点射功率，int型

"shotTime":0.1			//点射时间，取值范围为0-1，double型

}

手动操作：

*0x4411 LASER_HANDOP_SET

{

"type":1,

//手动操作类型：1：光闸开关，2：点射，3：气体检测，4：上抬，5：回中，6：跟随

"value":1				//1为开，0为关，对于点射只有1

}

手动操作当前状态：

*0x4412 LASER_HANDOP_INQUIRE

data：无

控制器返回：

*0x4413 LASER_HANDOP_RESPOND

{

"lightGate":0,			//光闸,int型

"shotPower":0,			//点射功率,int型

"shotTime":0.1,			//点射时间,double型

"aspiration":0,			//气体检测,int型

"liftUp":0,			//上抬,int型

"backMiddle":0,			//回中,int型

"follow":0,			//跟随,int型

}

模拟量匹配中的发送：

*0x4417 LASER_FACTCURVOL_SET

{

"type":1,				//从第1个发送到第4个发送分别为1到4

"value":5.5			//发送的值，0-10，double型

}

控制器返回：

*0x4419 LASER_FACTCURVOL_RESPOND

{

"result":1				//1：设置成功，0：设置失败

}

喷嘴清洁：

0x4423 LASER_CUT_NOZZLE_CLEAN

{

"cleanNozzleTime":  0, //发送大于0的数，打开运行设定秒数之后自动关闭，单位ms

}

冷却气：

0x4422 LASER_CUT_FEED_COOL_GAS

{

"feedCoolGas":  0, //1:打开，0：关闭

}
