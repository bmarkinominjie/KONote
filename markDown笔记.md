
<h1 align = "center">MD笔记</h1>
[TOC]
##<span id = "jumpTest">1.斜体和粗体</span>
```
*斜体*
**粗体** 
~~删除线~~
```
*斜体* **粗体** ~~删除线~~
##2.标题
```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```
##3.超链接

####1.基本链接
```
欢迎来到[梵居闹市](http://blog.leanote.com/freewalk)
```
 欢迎来到[梵居闹市](http://blog.leanote.com/freewalk)
####2.参考链接
```
这篇笔记参考了[梵居闹市的博客][1]、[ingood的博客][2]、请关注[我的Github][]。
	[1]:http://blog.leanote.com/post/freewalk/Markdown-语法手册#title "ingood的博客"
	[2]:https://segmentfault.com/a/1190000006247465#articleHeader4 "segmentfault"
	[我的Github]:https://github.com/bmarkinominjie "我的Github"
```
这篇笔记参考了[梵居闹市的博客][1]、[ingood的博客][2]、请关注[我的Github][]。
[1]:http://blog.leanote.com/post/freewalk/Markdown-语法手册#title "ingood的博客"
[2]:https://segmentfault.com/a/1190000006247465#articleHeader4 "segmentfault"
[我的Github]:https://github.com/bmarkinominjie "我的Github"
####3.自动链接
```
<http://example.com/>
```
<http://example.com/>
##4.锚点
```
//先设置
##<span id = "jumpTest">1.斜体和粗体</span>
跳转到[1.斜体和粗体](#jumpTest)
```

跳转到[1.斜体和粗体](#jumpTest)
##5.列表
####1.无序列表
```
+ 第一行（+符号后面注意加空格）
- 第二行（-符号后面注意加空格）
* 第三行（*符号后面注意加空格）
```
+ 第一行
- 第二行
* 第三行

####2.有序列表
```
1. 第一行
2. 第二行
3. 第三行
```
1. 第一行
2. 第二行
3. 第三行

####3.定义列表
 ```
**Markdown**
轻量级文本标记语言，可以转换成html，pdf等格式
 ```
**Markdown**
轻量级文本标记语言，可以转换成html，pdf等格式
####4.列表缩进
```
* 轻量级文本标记语言，可以转换成html，pdf等格式（*加上空格）
```
* 轻量级文本标记语言，可以转换成html，pdf等格式轻量级文本标记语言（*加上空格）

####5.文本缩进
* 轻量级文本标记语言，可以转换成html，pdf等格式

  轻量级文本标记语言，可以转换成html(隔一行，缩进4空格)
  
  轻量级文本标记语言，可以转换成html
  
* 轻量级文本标记语言，可以转换成html，pdf等格式

##6.引用
```
> 教程在哪？ - 小白
>> 自己看教程！ - 愤青
>>> 请问 Markdwon 怎么用？ - 小白
```
> 教程在哪？ - 小白
>> 自己看教程！ - 愤青
>>> 请问 Markdwon 怎么用？ - 小白
	
##7. 插入图像
```
![美女](http://userhead-10001315.image.myqcloud.com/7c9234b6-5093-4e30-8201-83c5047bf919/thumb)
```
![美女](http://userhead-10001315.image.myqcloud.com/7c9234b6-5093-4e30-8201-83c5047bf919/thumb)
##8.注脚
```
使用 Markdown[^1]可以效率的书写文档, 直接转换成 HTML[^2], 你可以使用 Leanote[^Le] 编辑器进行书写。你可以使用 Leanote[^kon] 编辑器进行书写。
[^1]:	Markdown是一种纯文本标记语言
[^2]:	HyperText Markup Language 超文本标记语言
[^Le]: 开源笔记平台，支持Markdown和笔记直接发为博文
[^kon]: he is a kind man;
```
使用 Markdown[^1]可以效率的书写文档, 直接转换成 HTML[^2], 你可以使用 Leanote[^Le] 编辑器进行书写。你可以使用 Leanote[^kon] 编辑器进行书写。
[^1]:	Markdown是一种纯文本标记语言
[^2]:	HyperText Markup Language 超文本标记语言
[^Le]: 开源笔记平台，支持Markdown和笔记直接发为博文
[^kon]: he is a kind man;
##9.表格
```
学号 |姓名  |分数
--- |:-:   |--:
bar | bar  | bar
baz | baz  | baz

dog | bird | cat 
---|---|----
foo | foo  | foo
bar | bar  | bar
```
学号 |姓名  |分数
--- |:-:   |--:
bar | bar  | bar
baz | baz  | baz

dog | bird | cat 
---|---|----
foo | foo  | foo
bar | bar  | bar
⚠️"-"或者":"至少共有三个
##10.流程图
####1.系统Demo
```flow
st=>start: Start:>http://www.baidu.com
e=>end
op1=>operation: My Operation
sub1=>subroutine: My Subroutine
cond=>condition: Yes
or No?:>http://www.google.com
io=>inputoutput: catch something...

st->op1->cond
cond(yes)->io->e
cond(no)->sub1(right)->op1
```
```flow
开始=>start: 开始
结束=>end: 结束

操作1=>operation: 操作1
操作2=>subroutine: 操作2
条件=>condition: 是否大于0
结果=>inputoutput: 输出结果

开始->操作1->条件
条件(yes)->结果->结束
条件(no)->操作2(right)->操作1
```
####2.原理
*	标签：start end operation subroutine condition inputoutput

tag=>type: content:>url
*	tag 是流程图中的标签，在第二段连接元素时会用到。名称可以任意，一般为流程的英文缩写和数字的组合。
*	type 用来确定标签的类型，=>后面表示类型。由于标签的名称可以任意指定，所以要依赖type来确定标签的类型
*	content 是流程图文本框中的描述内容，: 后面表示内容，中英文均可。⚠️冒号与文本之间一定要有个空格
*	url是一个连接，与框框中的文本相绑定，:>后面就是对应的 url 链接，点击文本时可以通过链接跳转到 url 指定页面
####3.Demo
```flow
开始=>start: 开始
结束=>end: 结束

操作1=>operation: 操作1
操作2=>subroutine: 操作2
条件A=>condition: 条件A yes or no?:
条件B=>condition: 条件B yes or no?:
条件C=>condition: 条件C yes or no?:
条件C=>condition: yes or no?:

结果=>inputoutput: 输出结果

开始->操作1->条件A
条件A(yes)->结果->结束
条件A(no)->条件B
条件B(yes)->结果->结束
条件B(no)->条件C
条件C(yes)->结果->结束
条件C(no)->操作2(right)->操作1
```




