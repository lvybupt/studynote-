#VNC for Pi3 B

首先在`Pi`安装`VNC`：  
```sudo apt-get install tightvncerver```

安装好之后设置`VNC`密码：  
```vncpasswd```  

确认两次密码。

设置开机启动：
``` sudo vi /etc/init.d/tightvncserver```

`tightvncserver`内容：

```shell 
#!/bin/sh
### BEGIN INIT INFO
# Provides:          tightvncserver
# Required-Start:    $local_fs
# Required-Stop:     $local_fs
# Default-Start:     2 3 4 5
# Default-Stop:      0 1 6
# Short-Description: Start/stop tightvncserver
### END INIT INFO

# More details see:
# http://www.penguintutor.com/linux/tightvnc

### Customize this entry
# Set the USER variable to the name of the user to start tightvncserver under
export USER='pi'
### End customization required

eval cd ~$USER

case "$1" in
  start)
    # 启动命令行。此处自定义分辨率、控制台号码或其它参数。
    su $USER -c '/usr/bin/tightvncserver -depth 16 -geometry 800x600 :1'
    echo "Starting TightVNC server for $USER "
    ;;
  stop)
    # 终止命令行。此处控制台号码与启动一致。
    su $USER -c '/usr/bin/tightvncserver -kill :1'
    echo "Tightvncserver stopped"
    ;;
  *)
    echo "Usage: /etc/init.d/tightvncserver {start|stop}"
    exit 1
    ;;
esac
exit 0

```

`user`为默认用户名`pi`.  
更改`tightvncserver`执行权限：  
```sudo chmod 755 /etc/init.d/tightvncserver ```  
更新开机启动列表：  
```sudo update-rc.d tightvncserver defaults```  
重启树莓派：  
```sudo reboot```

手动启动：  
```tightvncserver -geometry 800x600 :1``` 

终止：
```tightvncserver -kill :1```

下载`VNC`客户端，`IP：1`登录。
