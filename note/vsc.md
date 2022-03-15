# VSC 笔记

## github屏蔽解决

### 墙屏蔽
<!-- markdownlint-disable md013 -->
1. 访问 [http://github.global.ssl.fast...](http://github.global.ssl.fastly.net.ipaddress.com/#ipinfo)获取cdn域名以及IP地址
2. 访问 [http://github.com.ipaddress.c...](https://github.com.ipaddress.com/#ipinfo) 获取cdn域名以及IP地址

3. 修改hosts

    ```hosts
    # fix git clone github project failed
    ---------------------------------------------
    199.232.69.194 github.global.ssl.fastly.net
    140.82.112.3 github.com
    140.82.114.10 codeload.Github.com
    ```

4. 刷新DNS缓存
  
## 快捷键

* 行复制：Ctrl + c

  >当你没有选中行中任意字符时，复制出来的实际上是整行的内容；

* 行复制：Shift + Alt + ↑/↓

  >想在某行的基础上修改？复制粘贴？Shift 加 Alt 加方向键一步到位！
当然，对于受支持的代码文件，一般还会支持别的操作，比如：

* 行移动：Alt + ↑/↓

  >想整体移动一行怎么办？剪切粘贴？Alt 加方向键轻松移动一行！注意，如果你扩选多行时，相应地会移动多行；

* 行注释：Ctrl + /；  
* 块注释：Alt + Shit + A；  
* 格式化：Alt + Shit + F。

* Ctrl + ]/[

  >即可完成整行的向右缩进一个单位 / 向左缩进一个单位。缩进完成后，会显示列对齐线帮助你把握缩进信息。同样地，选择多行的时候，可以同时对多行进行缩进。  

* Alt + → / ←
  >切换到下一个 / 上一个编辑点。  

* Ctrl + Shift + \
  >代码编辑器能够解析代码！它已经知道了另一个括号的位置！那它为什么不提供给我们接口，让我们直接跳到另一个括号那里去？？
这就是 Ctrl + Shift + \了。点击一个括号，在使用这个快捷键后，光标就能跳转到相应括号位置。

* Alt + F12：代码定义以浮窗的形式覆盖在当前页面上；
* F12：直接跳转到代码定义的位置。
* Ctrl + H 查找替换
  >点击“全部替换”或者按Ctrl+Alt+Enter键就可以替换全部内容

* vsc 同步
  >登录  
  上传：Shift+Alt+U、  
  下载：Shift+Alt+D