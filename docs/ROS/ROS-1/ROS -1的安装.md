# ROS -1的安装

# 安装ROS -1

##### 本节为ROS的安装教程，在安装Ubuntu18.04 系统安装后，即可安装ROS，下面给出完整的安装步骤，以及出现错误的解决方式。

### 1 .设置 sources.list​

Ubuntu 配置的默认源并不是国内的服务器，下载更新软件都比较慢。并且若直接安装ROS2，可能会失败，因此可尝试对 ubuntu 配置阿里源、清华源等，下面提供一个阿里源的配置方案：

（1）备份源列表文件 sources.list

```
sudo cp /etc/apt/sources.list /etc/apt/sources.list_backup
```
（2）打开 sources.list 文件修改

```
sudo gedit /etc/apt/sources.list
```
（3）编辑/ etc/apt/sources.list 文件, 在文件最前面添加阿里云镜像源：

```
deb http://mirrors.aliyun.com/ubuntu/ bionic main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ bionic-security main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ bionic-updates main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ bionic-proposed main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ bionic-backports main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ bionic main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ bionic-security main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ bionic-updates main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ bionic-proposed main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ bionic-backports main restricted universe multiverse
```
（4）刷新列表​

```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install build-essential
```
### 2.设置安装源

官方默认安装源:

```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main"
    > /etc/apt/sources.list.d/ros-latest.list'
```
或来自国内清华的安装源：

```
sudo sh -c '. /etc/lsb-release && echo "deb http://mirrors.tuna.tsinghua.edu.cn/ros/ubuntu/ `lsb_release -cs` main" > /etc/apt/sources.list.d/ros-latest.list'
```
ps：建议使用国内资源，安装速度更快。

### 3. 设置密钥​

```
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
```
### 4. 安装​ROS

```
sudo apt update
sudo apt install ros-melodic-desktop-full
```
### 5.  安装构建依赖rosdep​

如果没有安装rosdep，可以通过以下命令进行安装。

```
sudo apt update
sudo apt install python-rosdep
```
安装rosdep后，通过以下命令初始化rosdep

```
sudo rosdep init
rosdep update
```
如果一切顺利，rosdep 初始化与更新的打印结果如下

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/2Zt4ARWS/resources/nl9X6UaUezcOgd0oX6mfypC4gKdM5jLISU1-1UcZ9tM.png)

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/2Zt4ARWS/resources/QOaojuwUx40ZElCWBWeT-15sRehIrXBuRncHW1MHVNM.png)

##### 若初始化失败，可先尝试用手机热点连接网络进行 rosdep init,还是不行则按照一下步骤修改（还是不可以就多次执行 sudo rosdep init 直到无报错），初始化完成再去配置环境变量

因为服务器的原因，会遇到下面的问题，需要对配置文件进行修改

```
sudo rosdep init
ERROR: cannot download default sources list from: https://raw.githubusercontent.com/ros/rosdistro/master/rosdep/sources.list.d/20- default.list
Website may be down.
rosdep update
reading in sources list data from /etc/ros/rosdep/sources.list.d ERROR: error loading sources list:
('The read operation timed out')
```
打开包含资源下载函数的文件：

```
sudo gedit /usr/lib/python2.7/dist-packages/rosdep2/sources_list.py
```
添加

```
url="https://ghproxy.com/"+url
```
def download_rosdep_data(url):
    """
    :raises: :exc:`DownloadFailure` If data cannot be
        retrieved (e.g. 404, bad YAML format, server down).


    """
    try:
        url = "https://ghproxy.com/"+url
        f = urlopen_gzip(url, timeout=DOWNLOAD_TIMEOUT)
        text = f.read()
        f.close()
        data = yaml.safe_load(text)
        if type(data) != dict:
            raise DownloadFailure('rosdep data from [%s] is not a YAML dictionary' % (url))
        return data
    except (URLError, httplib.HTTPException) as e:
        raise DownloadFailure(str(e) + '(%s)' % url)
    except yaml.YAMLError as e:
        raise DownloadFailure(str(e))


每个人可能都不一样 "在原本的路径前加https://gexxxxxx.com/"

修改/usr/lib/python2.7/dist-packages/rosdistro/init.py 文件中的 DEFAULT_INDEX_URL

```
sudo gedit /usr/lib/python2.7/dist-packages/rosdistro/init.py
```
DEFAULT_INDEX_URL ='https://ghproxy.com/https://raw.githubusercontent.com/ros/rosdistro/master/index-v4.yaml'

```
"""
第72行
"""
# default file to download with 'init' command in order to bootstrap
# rosdep
DEFAULT_INDEX_URL ='https://ghproxy.com/https://raw.githubusercontent.com/ros/rosdistro/master/index-v4.yaml'
```
改其余（4 个）文件中的地址，在地址http://raw.githubsercontent.com/ 前添加http://ghproxy.com/

```
sudo gedit /usr/lib/python2.7/dist-packages/rosdep2/gbpdistro_support.py


//修改第36行的地址
```
sudo gedit /usr/lib/python2.7/dist-packages/rosdep2/sources_list.py 72行


//修改第72行
```
sudo gedit /usr/lib/python2.7/dist-packages/rosdep2/rep3.py


//修改第39行
```
sudo gedit /usr/lib/python2.7/dist-packages/rosdistro/manifest_provider/github.py


//修改第68行、119行
解决 Hit 第五个地址的报错

```
sudo gedit /usr/lib/python2.7/dist-packages/rosdep2/gbpdistro_support.py
```
在第 204 行添加如下代码（即在该函数块下的第一行处）

```
gbpdistro_url = "https://ghproxy.com/" + gbpdistro_url


# 注意，原网址中代理地址的双引号是中文，直接粘贴复制会报字符识别错误
```
如果依然不能解决 Hit 第五个地址的报错，则修改

```
sudo gedit /etc/resolv.conf
```
将原有的 nameserver 这一行注释，并添加以下两行：

```
nameserver 8.8.8.8 #google域名服务器
nameserver 8.8.4.4 #google域名服务器
```
保存退出，执行

```
sudo apt-get update
```
再执行

```
sudo rosdep init
ERROR: default sources list file already exists:
/etc/ros/rosdep/sources.list.d/20-default.list Please delete if you wish to re-initialize
```
解决办法： 执行以下命令，删除已经存在的初始化文件：

```
sudo rm /etc/ros/rosdep/sources.list.d/20-default.list
```
然后再重新运行

```
sudo rosdep init
```
若一直失败，可参考此教程

### 6.设置环境变量​

```
echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```
### 7. ROS 功能包的安装​

```
sudo apt-get install ros-melodic-moveit
sudo apt-get install ros-melodic-joint-state-publisher
sudo apt-get install ros-melodic-robot-state-publisher
sudo apt install ros-melodic-gazebo-ros-pkgs
sudo apt-get install ros-melodic-gazebo-ros-control
sudo apt-get install ros-melodic-joint-trajectory-controller
sudo apt-get install ros-melodic-industrial-core
```
### 8.测试

ROS 内置了一些小程序，可以通过运行这些小程序以检测 ROS 环境是否可以正常运行

（1）打开一个终端，启动roscore

```
roscore
```
（2）另起一个终端，启动一个小海龟例程

```
rosrun turtlesim turtlesim_node
```
（3）再打开一个终端，输入：

```
rosrun turtlesim turtle_teleop_key
```
将光标悬停在这个终端中，然后使用↑、↓、←、→键来控制小乌龟的移动

![](https://ones.inexbot.com/wiki/api/wiki/external-editor/RnqpQ1Yp/2Zt4ARWS/resources/2zyngnK_Va6EtgP7F5uwSVkJF5oDqW0A_rJxU5adKmk.png)
