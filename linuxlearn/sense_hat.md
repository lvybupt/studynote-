#Raspberrypi  Sense_Hat

安装
```
sudo apt-get install sense-hat 
```

更多的资料 [Sense HAT](https://pythonhosted.org/sense-hat/)

树莓派`python` 语言中有相应的模块

```python3
from sense_hat import SenseHat
```
ed点阵输出

```python3
sense = SenseHat()
sense.show_message("Hello world!")
```

以下代码会返回一个含有rgb信息的数组，并且再led阵列中显示


```python3
sense = SenseHat()
sense.load_image("smile.png")

```

