[清华大学开源软件镜像站](https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/)

找到对应版本的anaconda下载

在Anaconda3~.sh处打开终端

运行.sh文件：

```shell
bash (file_name)
```

进入注册信息页面，输入yes,之后一直Enter，在安装信息中注意查看安装位置，例如

```shell
[/home/user/anaconda3]>>>
#同意路径enter即可
#更换路径在>>>后输入新路径
```

安装完成后是否加入环境变量信息 yes

提示信息“Do you wish to proceed with the installation of Microsoft VSCode? [yes|no]”，输入no；



环境变量配置

```
sudo gedit ~/.bashrc
export PATH="/home/user/anaconda3/bin:$PATH"
source ~/.bashrc
```

进入conda 控制台

```shell
conda activate
#有时会出现CommandNotFoundError: Your shell has not been properly configured to use 'conda activate'.的情况
#使用 source activate 也可以进入控制台
#推出控制台
conda deactivate

```

打开spyder

```shell
#进入anaconda3/bin 打开终端
./spyder
```

打开jupyter notebook

```shell
#直接在目标位置打开终端输入
jupyter notebook
#若终端无法识别jupyter,使用conda控制台打开jupyter notebook
source activate
jupyter notebook
```

