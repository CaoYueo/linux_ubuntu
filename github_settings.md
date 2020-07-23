###### 关于如何在ubuntu上安装配置github

###### 1. github和本地的连接

导入git

```shell
sudo apt install git
```

设置git

```shell
git config --global user.name "你的用户名"
git config --global user.email "你的邮箱地址"
```

**配置SSH Key**

打开终端

```shell
ssh-keygen -t rsa -C "你的邮箱地址"
```

一直**Enter**，直至完成，在途中注意查看.ssh文件的位置。

.ssh文件下有id_rsa和id_rsa.pub这两个文件。这两个就算SSH Key的秘匙对，id_rsa是私匙不可泄露，id_rsa.pub是公匙，是要使用的。

.ssh是隐藏文件，一般是不可见的，在刚刚查看的.ssh所在的目录下，ctrl+h，可以显示出隐藏文件。

复制id_rsa.pub内容。

进入github,settings ->SSH and GPG keys 点击New SSH key ,复制内容粘贴key内-> Add SSH Key,完成。

###### 2.创建本地仓库

在想要创建仓库的位置打开终端

```shell
 git init "仓库名字"
```

```shell
cd "库名" #进入仓库
```

使用gedit在库内创建文件

```shell
gedit test.md
```

你可以选择在本地库内创建README.md，也可以在github网页的库内创建。README.md是用来描述库的，内容自定。建议从本地创建README.md,防止出现一些不同布的问题。

将库内文件加入到缓冲区

```shell
git add file_name
git add ./ #仓库下所有文件
```

上传

```shell
git commit -m "some_message" 
#上传 add的文件 some_message 内容任意
```

在github上创建库，获得仓库的SSH或HTTPS

使本地仓库和github仓库建立连接

```shell
git remote add origin https://github.com/user_name/test.git
#以HTTPS为例
```

上传缓冲区的内容

```shell
git push origin master
```

###### 3.从github下载到本地仓库

仓库地址，打开github仓库，点击**Code**

```shell
git clone "仓库地址"
```

