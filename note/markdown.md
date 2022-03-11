# **MARKDOWN**

<font face=微软雅黑>
<!-- <font size=4>   -->

**Markdownlint**  

* 配置  
    在项目任意目录创建 *.markdownlint.json* 可屏蔽部分功能
```
{
    "md033": false
    // 文档中不允许使用html语句
    "md041": false
    // 文档的第一个非空行应该是文档最高级的标题，默认是1级标题
  }
```

[**Markdown All in One 地址**](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)

### Markdown All in One使用教程  

目录

- 1. 特点
- 2. 常用快捷键
- 3. 常用命令  
  
### 1. 特点

提供常用操作的快捷键  
支持目录  
支持同步预览(ctrl+shift+v)  
轻松转换html和pdf文件  
可格式化table(alt+shift+f)和task list(altvv+c)  
支持特殊数学符号渲染
  
### 2. 常用快捷键

粗体 ctrl+b  
斜体 ctrl+i  
删除线 alt+s  
切换数学环境 ctrl+m  
同步预览 ctrl+shift+v
检查任务列表项 alt+c
格式化表格 alt+shift+f
格式化任务列表 alt+c

### 3. 常用命令

先按F1进入VSCode命令面板  
自动创建目录 Create Table of Contents  
更新目录 Update Table of Contents  
添加/更新标题编号 Add/Update Section numbers  

<details>
  <summary><mark><font color=GRAY>点击查看详细内容</font></mark></summary>
  <p> - 测试 测试测试</p>
  
  <code>  
   for i in a:
    print(i)
  </code></pre>
</details>

<details><summary><font size=5 color=red>test</font></summary>

   dd  
aaa
</details>

[~]: 注释

| 表头   | 表头     |
| ------ | -------- |
| 单元格 | *单元格* |
| 单元格 | *单元格* |
---

```c#
  for i in a:
    print(i)
```

&nbsp;
</br>

| 水果 | 价格 | 数量  |
| ---- | ---: | :---: |
| 香蕉 |   $1 |   5   |
| 苹果 |   $1 |   6   |
| 草莓 |   $1 |   7   |
---
<h3 id=t>  触发点 <h3>

[点击跳到链接一](#1)、[点击跳到链接二](#2)、[点击跳到链接三](#3) &nbsp; &nbsp; &nbsp; &nbsp; [脚注^](脚注^)

<p id=1>链接一</p>

<a id=2>[链接二](https://baidu.com)</a>

<a id=3>链接三</a>  
（[回到触发点](#t)）  

这是一个链接到谷歌的[脚注]  

[脚注]: http://www.google.com  

[鏈接1]: commentted-out contents  

[鏈接1]: https://baidu.com  

使用 Markdown[^1]可以效率的书写文档, 直接转换成 HTML[2^], 你可以使用 Typora[^T] 编辑器进行书写。  
[^1]:Markdown是一种纯文本标记语言  
[2^]: HyperText Markup Language 超文本标记语言  
[^T]:NEW WAY TO READ & WRITE MARKDOWN.  

`1. test`  

1. test

---
    行内代码

C语言的`字符`串格式化函数是：`printf` `input`  
‘測試’文字'紅色'

```
print "Hello, world!\n";
```

```python
print "Hello, world!\n";
```

**粗體**

茅盾[^1]
[^1]: 我国著名的文学作家
[toc]
[1.一级目录](#1m)  
　[1.1二级目录](#1m.1)
　　[1.1.1三级目录](#1m.1.1)

<h1 id='1m'> 一级目录 </h1>

<h2 id='1m.1'> 二级目录 </h2>  
<p id='1m.1.1'> 三级目录 </p>
---

I get 10 times more traffic from [Google] than from [Yahoo][2] or [MSN][3].  

[Google]: http://google.com/        "Google"
[yahoo]: https://baidu.com
[2]: http://search.yahoo.com/  "Yahoo Search"
[3]: http://search.msn.com/    "MSN Search"

[2.17]

[2.17]:http://192.168.2.17

这是一个链接到谷歌的[^脚注]。

[^脚注]: http://www.google.com

---
**链接**  
>[**baidu**](http://baidu.com)

![test](https://www.baidu.com/img/flexible/logo/pc/result.png)  

[W3Cschool](http://www.w3cschool.cn/)   

[链接文字][33]
[33]: http://www.w3cschool.cn/ "链接文字"

---
</br>

设置图片大小
>[**baidu**](http://baidu.com)
<image src=https://www.baidu.com/img/flexible/logo/pc/result.png height="10%" width="10%">  

键盘图标  
> <kbd>**ctrl**</kbd>**+**<kbd>alt</kbd>+<kbd>del</kbd>
---
