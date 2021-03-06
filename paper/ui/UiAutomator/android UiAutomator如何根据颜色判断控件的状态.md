# android UiAutomator如何根据颜色判断控件的状态

本人在用UiAutomator做测试的时候，经常会遇到一些控件因为不同的条件显示不同的颜色，在学习了UiAutomator图像处理之后，自己尝试写了一个方法来处理不同颜色控件的区分。分享代码供大家参考。


```
	//根据颜色判断状态
	public boolean isBlue(UiObject uiObject) throws UiObjectNotFoundException {
		screenShot("test");//截图
		String path = "/mnt/sdcard/123/test.png";
		Bitmap bitmap = BitmapFactory.decodeFile(path);//新建并实例化bitmap对象
		Rect rect = uiObject.getVisibleBounds();
		int x = rect.left;
		int xx = rect.right;
		int y = rect.top;
		int yy = rect.bottom;
		List<Integer> blueColor = new ArrayList<Integer>();
		for (int i = x; i < xx; i++) {
			for (int k = y;k < yy;k++) {
				int color = bitmap.getPixel(i, k);//获取坐标点像素颜色
				int red = Color.blue(color);
				blueColor.add(red);
			}
		}
		int sum = 0;
		for (int i = 0;i<blueColor.size();i++) {
			sum += blueColor.get(i);
		}
//		output(sum/blueColor.size());
		return sum/blueColor.size() > 200?true:false;
	}
```

下面是在选择判定值的过程中快速获取某点颜色值的方法：

```
	public int getRedPixel(int x, int y) {
		screenShot("test");//截图
		String path = "/mnt/sdcard/123/test.png";
		Bitmap bitmap = BitmapFactory.decodeFile(path);//新建并实例化bitmap对象
		int color = bitmap.getPixel(x, y);//获取坐标点像素颜色
//		output(color);//输出颜色值
		int red = Color.red(color);
		return red;
	}
	public int getGreenPixel(int x, int y) {
		screenShot("test");//截图
		String path = "/mnt/sdcard/123/test.png";
		Bitmap bitmap = BitmapFactory.decodeFile(path);//新建并实例化bitmap对象
		int color = bitmap.getPixel(x, y);//获取坐标点像素颜色
//		output(color);//输出颜色值
		int green = Color.green(color);
		return green;
	}
	public int getBluePixel(int x, int y) {
		screenShot("test");//截图
		String path = "/mnt/sdcard/123/test.png";
		Bitmap bitmap = BitmapFactory.decodeFile(path);//新建并实例化bitmap对象
		int color = bitmap.getPixel(x, y);//获取坐标点像素颜色
//		output(color);//输出颜色值
		int blue = Color.blue(color);
		return blue;
	}
```

```
public int[] getRGBcolorPixel(int x, int y) {
		screenShot("testDemo");
		String path = "/mnt/sdcard/123/testDemo.png";
		Bitmap bitmap = BitmapFactory.decodeFile(path);
		int color = bitmap.getPixel(x, y);
		int red = Color.red(color);
		int green = Color.green(color);
		int blue = Color.blue(color);
		int[] rgb = {red, green, blue};
		return rgb;
	}
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

# [点击查看公众号地图](https://mp.weixin.qq.com/s/CJJ2g-RqzfBsbCCYKKp5pQ)


> 欢迎有兴趣的一起交流：群号:340964272

![](/blog/pic/201712120951590031.png)

<script src="/blog/js/bubbly.js"></script>
<script src="/blog/js/article.js"></script>