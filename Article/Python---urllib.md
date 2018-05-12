### urllib
urllib是一个URL处理包，这个包中集合了一些处理URL的模块

* urllib.request模块是用来打开和读取URLs的；

* urllib.error模块包含一些有urllib.request产生的错误，可以使用try进行捕捉处理；

* urllib.parse模块包含了一些解析URLs的方法；

* urllib.robotparser模块用来解析robots.txt文本文件.它提供了一个单独的RobotFileParser类，通过该类提供的can_fetch()方法测试爬虫是否可以下载一个页面。

urllib的request模块可以非常方便地抓取URL内容，也就是发送一个GET请求到指定的页面，然后返回HTTP的响应：


我们使用urllib.request.urlopen()这个接口函数就可以很轻松的打开一个网站，读取并打印信息

新建一个run.py的文件代码如下：

![](image/20180511140956.jpeg)

在终端运行命令 `python3 run.py`得到：

![](image/20180511140955.jpeg)

可以看出我们得到了一些信息，这些信息通过浏览器就会解释成我们看到的百度首页

看上去有些乱，可以用decode()函数来按指定编码解析一下

![](image/20180511142451.jpeg)

再执行一次得到：

![](image/20180511142452.jpeg)
