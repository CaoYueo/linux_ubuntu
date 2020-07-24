**ubuntu**关机后，屏幕左上角有几行英文，而且长时间为断电。可以**Enter**就可以看到在读秒，到90S。

解决使用watchdog

```shell
sudo apt install watchdog
sudo systemctl enable watchdog.service #开启服务

sudo systemctl start watchdog.service #启动服务
```

