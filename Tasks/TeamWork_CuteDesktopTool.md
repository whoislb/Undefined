Cute Desktop Tool
---

**Date**: 2015.07.26
**Author**: WX
**Principal**: WX

####限制条件：

 - **难度**：4
 - **限定语言**：N/A
 - **人数限制**：[2, 3]
 - **依赖任务**：[ColorfulBubbles](ColorfulBubbles.md)

####任务描述：

 - **简介**：又到一年毕业季，又到一年分别季，绘理亲和希炭今年也毕业了，她们考去了两个不同的学校，因为课业繁忙学校又距离远两个好朋友几乎没有什么机会见面，于是希炭想做一个自己的桌面宠物送给绘里亲，希望她在看到这个小希炭的时候就像看到自己一样就不会感到寂寞了，你能帮帮她么？一起做一个桌面宠物吧~

 - **需求**：
 	1. 图片人物可自选
    2. `widget`控件的大小请自己设置固定以防止绘出来的桌面宠物变形
	3. 小希炭要求点击的时候有一定动画~
	4. 鼠标*左键双击*小希炭的时候会出现菜单栏，初始的菜单栏包括几个功能：
		- 打开一个时钟
		- 打开命令行程序
		- 打开资源管理器
		- 打开一个新的记事本
		- 打开绘图
		- 关闭菜单栏
	5. 可以实现鼠标：
		- 左键点击拖动小希炭到桌面任意位置
		- 右键点击可以直接退出关闭小希炭程序
	6. 要求对菜单里所有*快捷方式*都可以*移动*、*添加*、*删除*~ 做成鼠标右键菜单的样式就好啦~，可以调整图标更好~
	7. 请注意*CPU*、*内存*占用和*响应速度*，要是绘理亲在打开小希炭后导致电脑运行太慢工作效率下降，希炭也会很伤心的
	8. [选做]把任意程序的快捷方式拖到小希炭上，会在菜单栏里自动生成打开程序的快捷方式
	9. 提示：
		- 可以通过重写`QMainWindow`的成员函数`paintEvent`来实现
		- 鼠标事件可以通过重写`QMouseEvent`和`QMouseMoveEvent`来实现
		- 关于调整控件大小和位置请参考`QWidget`类
		- QT打开文件的方式：
		```
		QFile file3("test/configurefile3.xml"); file3.open(QFile::ReadOnly)；//使用相对路径
		QFile file1("/usr/configurefile1.xml");file1.open(QFile::ReadOnly)；//使用绝对路径
		// 也可以添加资源文件再进行文件打开操作
		```
	10. 符合代码规范：[RobitCppCodingConventions](ref/RobitCppCodingConventions.md)

 - **关键词**：`QPainter`, `QPaintEvent`, `QPen`,` QColor`, `QTimer`, `QTime`, `QLCDNumber`, `QMouseEvent`, `QString`, `QAction`, `QMenu`, `QFile`
 - **参考资料**：
 	- [QMenu & QAction 右键菜单的生成](http://blog.sina.com.cn/s/blog_a6fb6cc90101fxsc.html)
 	- [关于图形绘制,QT提供了比用c++ 更便捷的界面美化方式QML](http://qmlbook.github.io/)
