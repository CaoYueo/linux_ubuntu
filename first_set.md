##### 安装ubuntu系统后，需要立刻做的两件事

###### 1.更新国内源

ubuntu系统默认的软件更新源是国外源，在国内使用速度很慢。

打开终端，输入命令后可能需要输入密码，密码就是设置系统时，设置的，而且在ubuntu终端输入密码是不可见的。

```shell
sudo gedit /etc/apt/sources.list
```

删除打开的文件的内容

粘贴国内源

阿里源

```
deb http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse

deb http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse

deb http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse

deb http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse

deb http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
```

清华源

```
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic main restricted universe multiverse

deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic main restricted universe multiverse

deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse

deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse

deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse

deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse

deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-security main restricted universe multiverse

deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-security main restricted universe multiverse

deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse

deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse
```

更新源

```shell
sudo apt-get update
```

修复损坏的软件包，卸载出错的软件包，重新安装正确版本

```shell
sudo apt-get -f install
```

更新软件

```shell
sudo apt-get upgrade
```

###### 2.下载速度过慢

具体原因不明，查资料是DNS域名解析太慢才导致下载速度慢

执行命令

```shell
sudo lshw -numeric -class network
sudo tracepath forum.ubuntu.org.cn
sudo apt-get install traceroute
sudo traceroute forum.ubuntu.org.cn
```

测试网速

首先安装speedtest-cli软件包

```shell
sudo apt install speedtest-cli
```

在终端直接输入

```shell
speedtest-cli
```

等候即可。