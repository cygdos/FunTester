# selenium2java让浏览器停止加载的方法

本人在使用selenium2java的过程中，偶然会遇到一些网页一直在加载，大概是防爬虫的一些东西，或者网速太慢了，或者有一些请求一直没有返回，今天想到一个办法，使用多线程按快捷键esc来使浏览器停止加载。试了效果不错，分享出来，供大家参考。


```
package selenium;
 
import java.awt.AWTException;
import java.awt.event.KeyEvent;
 
public class StopLoading extends Thread{
	public void run() {
		try {
			Thread.sleep(3000);
		} catch (InterruptedException e) {
			e.printStackTrace();
		}
		try {
			Library.getInstance().pressKeyEvent(KeyEvent.VK_ESCAPE);
		} catch (AWTException e) {
			e.printStackTrace();
		}
	}
 
}
```
使用方法就是在访问新页面的操作下面加上这段代码：

```
Thread stop = new StopLoading();
	    	stop.start();
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
10. [未来10年软件测试的新趋势-上](https://mp.weixin.qq.com/s/9XgpIfXQRuKg1Pap-tfqYQ)
11. [未来10年软件测试的新趋势-上](https://mp.weixin.qq.com/s/9XgpIfXQRuKg1Pap-tfqYQ)
12. [自动化测试解决了什么问题](https://mp.weixin.qq.com/s/96k2I_OBHayliYGs2xo6OA)

# [点击查看公众号地图](https://mp.weixin.qq.com/s/CJJ2g-RqzfBsbCCYKKp5pQ)



> 欢迎有兴趣的一起交流：群号:340964272

![](/blog/pic/201712120951590031.png)

<script src="/blog/js/bubbly.js"></script>
<script src="/blog/js/article.js"></script>