# 利用python wxpy和requests写一个自动应答微信机器人实例
<a href="/blog/home.html">返回首页</a><a href="/blog/交个朋友.html"  style="float:right;">交个朋友</a>
---

在做测试的过程中，同事们经常需要获取一个账户的token和个人信息，我自己利用spring boot写了一个接口，但是对于APP测试同学来说不是很方便，因为需要复制这个token到APP里面去，所以我做了一个微信自动应答的机器人，来实现这个需求。

思路如下：利用wxpy拿到对方发来的信息，然后简单判断，在用requests去请求我自己写的测试接口，拿到信息，发送给消息来源。

代码如下：

```
#!/usr/bin/python
# coding=utf-8
 
from wxpy import *
import os
import time
import requests
import json
 
 
bot = Bot(cache_path=True)
@bot.register(Friend, TEXT)
def print_group_msg(msg):
    m = msg.text
    friend = msg.sender
    if "@" not in m:
        m = "你发错账号了！"
        print m
        friend.send(m.decode("utf-8"))
        return
    r = requests.post("http://10.10.32.155:8081/uname/"+m)
    b = json.loads(r.text)["data"][u"用户token："]
    friend.send(b)
embed()
```

### 技术类文章精选

1. [java一行代码打印心形](https://mp.weixin.qq.com/s/QPSryoSbViVURpSa9QXtpg)
2. [Linux性能监控软件netdata中文汉化版](https://mp.weixin.qq.com/s/fdXtK-5WwKnxjLZdyg6-nA)
3. [接口测试代码覆盖率（jacoco）方案分享](https://mp.weixin.qq.com/s/D73Sq6NLjeRKN8aCpGLOjQ)
4. [性能测试框架](https://mp.weixin.qq.com/s/3_09j7-5ex35u30HQRyWug)
5. [如何在Linux命令行界面愉快进行性能测试](https://mp.weixin.qq.com/s/fwGqBe1SpA2V0lPfAOd04Q)
6. [图解HTTP脑图](https://mp.weixin.qq.com/s/100Vm8FVEuXs0x6rDGTipw)
7. [如何测试概率型业务接口](https://mp.weixin.qq.com/s/kUVffhjae3eYivrGqo6ZMg)
8. [httpclient处理多用户同时在线](https://mp.weixin.qq.com/s/Nuc30Fwy6-Qyr-Pc65t1_g)
9. [将swagger文档自动变成测试代码](https://mp.weixin.qq.com/s/SY8mVenj0zMe5b47GS9VSQ)
10. [五行代码构建静态博客](https://mp.weixin.qq.com/s/hZnimJOg5OqxRSDyFvuiiQ)
11. [httpclient如何处理302重定向](https://mp.weixin.qq.com/s/vg354AjPKhIZsnSu4GZjZg)
12. [基于java的直线型接口测试框架初探](https://mp.weixin.qq.com/s/xhg4exdb1G18-nG5E7exkQ)
13. [Tcloud 云测平台--集大成者](https://mp.weixin.qq.com/s/29sEO39_NyDiJr-kY5ufdw)


### 非技术文章精选
1. [为什么选择软件测试作为职业道路?](https://mp.weixin.qq.com/s/o83wYvFUvy17kBPLDO609A)
2. [成为杰出Java开发人员的10个步骤](https://mp.weixin.qq.com/s/UCNOTSzzvTXwiUX6xpVlyA)
3. [写给所有人的编程思维](https://mp.weixin.qq.com/s/Oj33UCnYfbUgzsBzEm2GPQ)
4. [自动化测试的障碍](https://mp.weixin.qq.com/s/ZIV7uJp7DzVoKhWOh6lvRg)
5. [自动化测试的问题所在](https://mp.weixin.qq.com/s/BhvD7BnkBU8hDBsGUWok6g)
6. [测试之《代码不朽》脑图](https://mp.weixin.qq.com/s/2aGLK3knUiiSoex-kmi0GA)
7. [成为优秀自动化测试工程师的7个步骤](https://mp.weixin.qq.com/s/wdw1l4AZnPpdPBZZueCcnw)
8. [优秀软件开发人员的态度](https://mp.weixin.qq.com/s/0uEEeFaR27aTlyp-sm61bA)
9. [如何正确执行功能API测试](https://mp.weixin.qq.com/s/aeGx5O_jK_iTD9KUtylWmA)

# [点击查看公众号地图](https://mp.weixin.qq.com/s/CJJ2g-RqzfBsbCCYKKp5pQ)

> 欢迎有兴趣的一起交流：群号:340964272

![](/blog/pic/201712120951590031.png)
<a href="/blog/home.html">返回首页</a><a href="/blog/交个朋友.html"  style="float:right;">交个朋友</a>
---
<script src="/blog/js/bubbly.js"></script>
<script src="/blog/js/article.js"></script>