错乱原因：Windows把计算机硬件时间当作本地时间，显示时间与BIOS中的时间三一样的。而ubuntu把计算机时间当作UTC（协调世界时），所以在此基础上在加上电脑设置的时区数，所以ubuntu显示的是正确的时间。

解决方法

```shell
#先更新ubuntu时间，确保时间正确
sudo apt install ntpdate
sudo ntpdate time.windows.com
#将时间更新到新的硬件上
sudo hwclock --localtime --systohc
#完成
```

