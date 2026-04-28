# Lua程序

Lua文件存放在~/robot/job/lua目录内

上传文件和查看文件列表用SCP的方式

#### 运行程序

上位机发送:0x2511

```
{
  "fileName":"xxx.lua"
}
```
控制器返回:0x2512

```
{
  "fileName":"xxx.lua",
  "result":true, //false 运行是否成功
  "error":"错误原因" //如果成功则""
}
```
#### 停止程序

上位机发送:0x2513

```
{
  "fileName":"xxx.lua"
}
```
#### 当前运行

上位机发送:0x2515

```
{}
```
控制器回复:0x2516

```
{
  "fileNames":[
    {
      "fileName":"xxx.lua",
      "status":1 //1-暂停,2-运行
    }
  ]
}
```