# This is a md file about linux learn!

##  ubuntu软件包升级

在ubuntu系统中，如果`apt-get update` 和`apt-get upgrade` 不能使所有软件包升级成功的话，尝试使用  `apt-get dist-upgrade`

	apt-get dist-upgrade

产生的原因是，`apt-get update` 和 `apt-get upgrade` 不能升级正在运行的或未安装的软件包。

## ssh 自动登录

在`/home/usernamer/.ssh`下的，`authorized_keys`中复制公钥。没有该目录或文件，则新建一个。