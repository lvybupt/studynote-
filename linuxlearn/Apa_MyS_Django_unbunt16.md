#ubuntu16 配置 Apache+MySql+Django

##软件版本号
Ubuntu 16.04.1  
python 3.5.2 `python3`  
Django 1.8.7 `import django` `print(django.VERSION)`  
MySQL 5.7.15 `mysql -V`  
Apache 2.4.18 `appchectl -v`

----
##安装过程
```
sudo apt-get update
sudo apt-get upgrade

sudo apt-get install apache2
sudo apt-get install libapache2-mod-wsgi
sudo apt-get install python3-django
sudo apt-get install mysql-server mysql-client
sudo apt-get install python3-mysqldb
```


