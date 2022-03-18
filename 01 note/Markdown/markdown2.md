<!-- HTML格式 -->
<font face=“微软雅黑”>
<font size=3>
<font color=black>

# Markdown-基本语法及markdownlint规则

&nbsp; Markdown是一种可以使用普通文本编辑器编写的标记语言，通过简单的标记语法，它可以使普通文本内容具有一定的格式。
Markdown语法包括插入标题、字体、超链接、插入图片、代码、列表及表格等常见使用方法
markdownlint是vscode上一款非常好用的格式检查扩展工具，它规定了许多规则并实时对文档进行检查，防止一些语法错误，同时维持文档风格的统一，使用此工具有助于形成一个良好的写作习惯和规范。
该篇文章也是我自学markdown做的总结，在此记录下来，仍有不足还需努力。
参考：

## 一、基本语法  

  注：本篇使用markdownlint插件中对于markdown语法的规定。
  arkdown的标题分为六级，在标题的文字前使用#来声明
  使用一个#表示一级标题，两个#表示二级标题，以此类推最多六个#表示六级标题
   这是一级标题  （在#符号与文字之间有一个空格）  

# 这是二级标题  

## 这是三级标题  

### 这是四级标题  

#### 这是五级标题  

##### 这是六级标题  （最多六级标题，字体自上而下，由大到小）

一级标题和二级标题还有一种写法（在标题文字下一行用至少三个或多个 = 或 - 来声明）
  这是一级标题
  ==

这是二级标题
  ----------  

使用markdownlint语法规则对于标题的规定如下：(既是报错信息提示)
  ===================================================  

   MD001 - Heading levels should only increment by one level at a time  
   标题级数每次只能扩大1, 也就是不能隔级创建标题（从1级到6级的顺序）  
   MD002 - First heading should be a top level heading  
   文档的第一个标题必须是最高级的标题（标题等级1级到6级逐渐降低）  
   MD003 - Heading style
   整篇文档要采用一致的标题格式  
   MD018 - No space after hash on atx style heading  
   在"atx"格式的标题中，#号和文字间需用一个空格隔开 ****
   MD019 - Multiple spaces after hash on atx style heading  
   在"atx"格式的标题中，#号和文字间只能用一个空格隔开，不能有多余的空格  
   MD020 - No space inside hashes on closed atx style heading  
   在"closed_atx"格式的标题中，文字和前后的#号之间需用一个空格隔开  
   MD021 - Multiple spaces inside hashes on closed atx style heading  
   在"closed_atx"格式的标题中，文字和前后的#号之间只能用一个空格隔开，不能有多余的空格  
   MD022 - Headings should be surrounded by blank lines  
   标题行的上下行必须都是空行  
   MD023 - Headings must start at the beginning of the line  
   标题行不能缩进  
   MD024 - Multiple headings with the same content  
   文档不能有内容重复的标题  
   MD025 - Multiple top level headings in the same document  
   同一文档只能有一个最高级的标题，默认是只能有一个1级标题  
   MD026 - Trailing punctuation in heading  
   标题行末尾不能有以下标点符号：".,;:!?"  
   MD041 - First line in file should be a top level heading  
   文档的第一个非空行应该是文档最高级的标题，默认是1级标题
 二、强调字体
  斜体
  在需要倾斜的文字左右两边分别使用一个 * 号将文字包起来
  加粗
  在需要加粗的文字左右两边分别使用二个 * 号将文字包起来
  斜体加粗
  在需要倾斜加粗的文字左右两边分别使用三个 * 号将文字包起来
  删除线
  在需要删除的文字左右两边分别使用二个 ~ 号将文字包起来
*内容** 　(*与内容之间没有空格)  
内容*(*与内容之间没有空格)
如：  
这是斜体*  
这是加粗**  
*这是斜体加粗***  
这是删除~~  
用markdownlint语法规则，对强调字体的规定如下 (既是报错信息提示)
________________________________
MD036 - Emphasis used instead of a heading  
不能用强调代替标题  
MD037 - Spaces inside emphasis markers  
用于创建强调的符号和强调的的文字之间不能有空格

# 有序列表  

序列表直接使用数字加上 . 即进行了编号  
序列表：（注：在 1. 与文字内容之间要有一个空格 ）  
 有序列表
 有序列表

 1. 内嵌有序列表  （有序列表内嵌列表空三个空格）
 2. 内嵌有序列表
 有序列表  
序列表效果如下：
序列表
嵌有序列表
嵌有序列表
序列表
序列表使用 - 或 + 或 *这三个符号都可以
序列表： （注：在 -，+，*符号与文字内容之间要有一个空格）  
无序列表
无序列表

+ 内嵌无序列表  （无序列表内嵌列表空二个空格）
+ 内嵌无序列表
无序列表
无序列表
序列表效果如下：
序列表1
序列表2
嵌无序列表3
嵌无序列表4
序列表5
序列表6
用markdownlint语法规则，对列表的规定如下(既是报错信息提示)  

_______________________________________________________
MD004 - Unordered list style  
整篇文档定义无序列表的格式要一致(使用-，+，*三个符号中的一个，全篇就用同一个)  
MD005 - Inconsistent indentation for list items at the same level  
同一级的列表缩进必须一致  
MD006-Consider starting bulleted lists at the beginning of the line  
1级列表不能缩进  
MD007 - Unordered list indentation  
无序列表嵌套缩进时默认采用两个空格  
MD029 - Ordered list item prefix  
有序列表的前缀序号格式必须只用1或者从1开始的加1递增数字  
MD030 - Spaces after list markers  
列表（有序、无序）的前缀符号和文字之间用1个空格隔开  
在列表嵌套或者同一列表项中有多个段落时，无序列表缩进两个空格，有序列表缩进3个空格  
MD032 - Lists should be surrounded by blank lines  
列表（有序、无序）前后需要用空行隔开，否则有些解释器不会解释为列表  
列表的缩进必须一致，否则会警告  
在要引用的文字前加上 > 符号即可，引用也可以嵌套两个>>或多个>>>>符号

例如：
> 这是引用
>> 这是引用
>>> 这是引用
效果如下：

使用markdownlint语法规则，对于引用的规定如下(既是报错信息提示)
============================================

+ MD027 - Multiple spaces after blockquote symbol  
  创建引用区块时，右尖括号 ( > ) 和文字之间有且只能有一个空格  

+ MD028 - Blank line inside blockquote  
  两个引用区块间不能仅用一个空行隔开或者同一引用区块中不能有空行，  
  如果一行中没有内容，则这一行要用>开头  
5.分割线
三个或者三个以上的 - 或者 * 都可以

---

例如：()

***

--------------------
效果如下：

使用markdownlint语法规则，对于创建水平线的规则如下(既是报错信息提示)
=================================================

+ MD035 - Horizontal rule style  
  创建水平线时整篇文档要统一(consistent)，要和文档中第一次创建水平线使用的符号一致  
  包括-，*符号的个数都要一致（也就是要一样长度）
6.超链接
语法：  
[超链接名字](超链接的地址  "超链接title")  

注:这个超链接title可以加可以不加，加上的效果是鼠标移到连接上会显示这个title
例如：  
[百度一下](http://www.baidu.com "baidu")
效果如下：
百度一下

语法：  
![图片alt](图片地址  "图片tetle")  

图片alt：就是显示在图片下方的文字，可以理解为图片的名字，或者图片内容的解释
图片地址：可以是网上图片链接，也可以是本地图片路径
图片title：同样可加可不加，鼠标移到图片上时显示这个title
例如：  
![图片](https://img-blog.csdnimg.cn/20200102172526881.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3NTU5MQ==,size_16,color_FFFFFF,t_70)
效果如下：

在这里插入图片描述
使用markdownlint语法规则，对于链接的规定如下(既是报错信息提示)
==============================================

+ MD034 - Bare URL used  
  单纯的链接地址需要用尖括号 (<>) 包裹，否则有些解释器不会解释为链接  

+ MD039 - Spaces inside link text  
  链接名和包围它的中括号之间不能有空格(也就是中括号和园括号之间不能有空格)  

+ MD042 - No empty links  
  链接的地址不能为空

+ MD045 - Images should have alternate text (alt text)  
  图片链接必须包含描述文本（也就是图片alt）  
语法：
不管是哪种方式，第一行为表头，第二行分隔表头和主体部分，第三行开始每一行为一个表格行。
列于列之间用管道符|隔开。原生方式的表格每一行的两边也要有管道符。
第二行可以为不同的列指定对齐方式。默认为左对齐，在-右边加上:就右对齐。

+ 左对齐， :-: 中心对齐，-: 右对齐
  
表头 | 表头  | 表头
---- | :---: | ---:
内容 | 内容  | 内容
内容 | 内容  | 内容

第一行设置表头名称
第二行分割表头和内容。  

+ 有一个就行，为了对齐，多加了几个  
文字默认居左  
-两边加：表示文字居中  
-右边加：表示文字居右  
注：原生的语法两边都要用 | 包起来。此处省略  
安装了Markdown All in One插件可以用Alt+Shift+F给表格两边都加上 | 包起来  
例如：  

| 姓名 | 年龄  | 名族 |
| ---- | :---: | ---: |
| 张三 |  45   | 汉族 |
| 李四 |  78   | 回族 |

效果如下：

姓名 年龄 名族
张三 45 汉族
李四 78 回族

9. 代码块
单行代码块
单行代码块：代码之间用一个反引号包起来（英文状态下左上角数字1前面那个按键）

单行代码块语法：  
`pandoc`
单行代码块效果:  
`pandoc`

将markdown文件转换为PDF文件我们使用pandoc这个工具来实现

多行代码块
代码块语法：(三个反引号抱起来的内容)  

|```java  (在三个反引号后面写上是哪一门编程语言的名字)
|  代码块内容...
|  代码内容...
|```

例如：  

|```C
|# include <stdio.h>
|
|int main(int argc,char **argv)
|{
|    return 0;
|}
|```

代码块效果如下：  

``` c  

# include <stdio.h>

int main(int argc,char **argv)
{
    return 0;
}
```

使用markdownlint语法规则，对于代码块的规定如下(既是报错信息提示)
==============================================

+ MD014 - Dollar signs used before commands without showing output  
  在代码块中，终端命令前不需要有美元符号($)  
  如果代码块中既有终端命令，也有命令的输出，则终端命令前可以有美元符号($)  

+ MD031 - Fenced code blocks should be surrounded by blank lines  
  单独的代码块前后需要用空行隔开（除非是在文档开头或末尾），  
  否则有些解释器不会解释为代码块  

+ MD038 - Spaces inside code span elements  
  当用单反引号创建代码段的时候，单反引号和它们之间的代码不能有空格  
  如果要把单反引号嵌入到代码段的首尾，创建代码段的单反引号和嵌入的  
  单反引号间要有一个空格隔开

+ MD040 - Fenced code blocks should have a language specified  
  代码块（此处是指上下用三个反引号包围的代码块）应该指定代码块的编程语言，  
  这一点有助于解释器对代码进行代码高亮

+ MD046 - Code block style  
  整篇文档采用一致的代码格式  
  指定代码块定义格式，有（"consistent","fenced","indented"）三种，  
  分别代表：文档上下文一致，使用三个反引号隔开，使用缩进，默认是上下文一致

10.流程图
|```mermaid
flowchat
|st=>start: 开始
|op=>operation: My Operation
|cond=>condition: Yes or No?
|e=>end
|st->op->cond
|cond(yes)->e
|cond(no)->op
|&```
效果如下：

11.markdown语法进阶
1.内容目录
在想要加目录的地方加上 [toc] 会自动生成目录预览可见，但是鉴于不同的编辑平台，
如简书的markdown不支持生成目录

markdown的换行是在行尾加两个空格 [空格 + 空格 + 回车]
在自己希望换行的地方使用，不然所有内容只会占一行（当然到达页面边缘会自动换行）

3.图片尺寸控制
图片链接使用markdown的语法完全没问题，但无法控制图片的尺寸和旋转等效果
可以使用html语法对图片尺寸进行设定，html控制图片的语法只有转html文件格式可以正常使用
既是：
md文件使用了该html控制图片尺寸的语法
md文件—>html文件---->pdf文件 可以显示
md文件—>latex文件---->pdf文件 不会显示（pandoc使用latex模板转pdf时）

语法：  
<img src="图片地址" width = "400" height = "260" alt="图片名" align=center>  
width->图片宽度数值  
height->图片高度数值  
align->图片放置位置（左left ， 居中center ， 右right）
markdown的注释可以使用html语法的注释语法：  
<!--这是注释，注释的内容不会呗显示-->
语法：  
这个内容附带一个脚注[^keyword]  
[^keyword]:这是第一个脚注  （在任意位置对脚注进行描述）
效果如下：
这个内容附带一个脚注1
点击脚注会自动跳转到脚注描述位置

6.Latex公式
行内公式使用 $ 符号将公式包起来  
  如：这是一个行内公式$E=mc^2$

行间公式使用 $$ 符号将公式包起来  
如：这样写它也会自动占一行
$$f(x)=\frac{2}{3}x+3$$
这是一个行内公式  
E = m c 2 E=mc^2
这样写它也会自动占一行 
f ( x ) = 2 3 x + 3  
f(x)=\frac{2}{3}x+3  
Latex数学公式语法使用可以参照：Latex数学符号及公式

这是第一个脚注 ↩︎
