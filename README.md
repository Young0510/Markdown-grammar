# Markdown-基本语法
## 目录  
- **[分级标题](#1分级标题)**  
- **[斜体粗体](#2斜体粗体)**  
- **[超链接](#3超链接)**  
- **[区块引用](#4区块引用)**  
- **[锚点](#5锚点)**  
- **[插入图像](#6插入图像)**  
- **[注脚](#7注脚)**  
- **[分隔线](#8分隔线)**  

### 1.分级标题
两种形式：
+ 使用'-'和'='标记一级二级标题
  > 一级标题  
  > '======='  
  > 二级标题  
  > '-------'  

  效果：
  > 一级标题  
  > ========  
  > 二级标题  
  > --------  

+ 使用'#'，表示1-6级标题
  > \# 一级标题  
  > \## 二级标题  
  > \### 三级标题  
  > \#### 四级标题  
  > \##### 五级标题  
  > \###### 六级标题  

  效果：
  > # 一级标题
  > ## 二级标题
  > ### 三级标题
  > #### 四级标题
  > ##### 五级标题
  > ###### 六级标题

### 2.斜体粗体

> \*斜体\*，\_斜体\_  
> \*\*粗体\*\*，\_\_粗体\_\_  
> \*\*\*加粗斜线\*\*\*   
> \~\~删除线\~\~

效果：
> *斜体*，_斜体_  
> **粗体**，__粗体__  
> ***加粗斜线***  
> ~~删除线~~

### 3.超链接
Markdown 支持两种形式的链接语法： 行内式和参考式两种形式，行内式一般使用较多。  
+ **行内式**  
  语法：[]里写链接文字，()里写链接地址, ()中的“”中可以为链接指定title属性，title属性可加可不加。title属性的效果是鼠标悬停在链接上会出现指定的 title文字。链接地址与链接标题前有一个空格。
  > 欢迎star\[Markdown-grammar\]\(https://github.com/Young0510/Markdown-grammar\)  
  > 欢迎star\[Markdown-grammar\]\(https://github.com/Young0510/Markdown-grammar "Markdown-grammar"\)  

  效果：
  > 欢迎star[Markdown-grammar](https://github.com/Young0510/Markdown-grammar)  
  > 欢迎star[Markdown-grammar](https://github.com/Young0510/Markdown-grammar "Markdown-grammar")  
+ **参考式**  
  语法：参考式链接分为两部分，文中的写法 [链接文字][链接标记]，在文本的任意位置添加[链接标记]:链接地址 “链接标题”，链接地址与链接标题前有一个空格。  

  如果链接文字本身可以做为链接标记，你也可以写成[链接文字][] [链接文字]：链接地址的形式，见代码的最后一行。

  > 欢迎关注我的\[知乎\]\[1\]，\[掘金\]\[2\]，\[stackoverflow\]\[3\]，\[github\]\[\]  
  > \[1\]:https:://www.zhihu.com/people/zhang-liu-ping-55   
  > \[2\]:https:://juejin.im/user/5c1780926fb9a049ca37436c   
  > \[3\]:https:://stackoverflow.com/users/10556742/liuping-zhang   
  > \[github\]:https:://github.com/Young0510  

  效果：
  > 欢迎关注我的[知乎][1]，[掘金][2]，[stackoverflow][3]，[github][]  


  [1]:https:://www.zhihu.com/people/zhang-liu-ping-55  
  [2]:https:://juejin.im/user/5c1780926fb9a049ca37436c  
  [3]:https:://stackoverflow.com/users/10556742/liuping-zhang  
  [github]:https:://github.com/Young0510  

  **注意**：上述的`[1]:https://www.zhihu.com/people/zhang-liu-ping-55`不出现在区块中。  

+ 自动链接
  > \<http://baidu.com>  
  > \<zlpyde@163.com> 

  效果：
  > <http://baidu.com>  
  > <zlpyde@163.com> 
 
### 4.区块引用
语法：引用需要在被引用的文本前加上'>'符号  
>\> 这是一段引用

>\> 这是多行引用  
>\> 引用文字1  
>\> 引用文字2  

效果：  
> 这是一段引用

> 这是多行引用  
> 引用文字1  
> 引用文字2  

+ 引用的多层嵌套  
  语法：区块引用可以嵌套（例如：引用内的引用），只要根据层次加上不同数量的'>'  
  > \>请问如何学习前端？  
  > \>\>看书  
  > \>\>\>看视频  

  效果：  
  > 请问如何学习前端？
  >> 看书
  >>> 看视频

+ 引用其他要素  
  引用的区块内也可以使用其他Markdown语法，包括标题、列表、代码区块等  

  > \> 1.  这是第一行  
  > \> 2.  这是第二行  
  > \> 代码例子：  
  > \>print("hello world!")  

  效果：  
  > 1.  这是第一行  
  > 2.  这是第二行  
  > 代码例子：  
  > print("hello world!")  

### 5.锚点  
Github 并不支持 HTML 形式的锚点链接，它有自己的规则  
+ 任意 1-6 个 # 标注的标题都会被添加上同名的锚点链接  
  > \[标题1\]\(\#标题1\)  
  > \[标题2\]\(\#标题2\)  
  > \[标题3\]\(\#标题3\)  

  > \# 标题1  
  > \#\# 标题2  
  > \#\#\# 标题3  

  效果：  
  > [标题1](#标题1)  
  > [标题2](#标题2)  
  > [标题3](#标题3)

  > # 标题1  
  > ## 标题2  
  > ### 标题3  

+ 锚点跳转的标识名称，可使用任意字符，大写字母要转换成小写  
  > \[Github\]\(\#github标题1\)  
  > \#\#\# Github标题1  

  效果：  
  > [Github](#github标题1)  
  > ### Github标题1  

+ 多单词锚点的空格用 - 代替  
  > \[Github 标题2 Test\]\(\#github-标题2-test\)  
  > \#\#\# Github 标题2 Test  

  效果：  
  > [Github 标题2 Test](#github-标题2-test)  
  > ### Github 标题2 Test  

+ 多级序号需要去除  
  > \[2.3. Github 标题\]\(\#23-github-标题\)  
  > \#\#\# 2.3. Github 标题  

  效果：  
  > [2.3. Github 标题](#23-github-标题)  
  > ### 2.3. Github 标题  

**注意**：非英文的锚点字符，在单击跳转时，在浏览器的 url 中会按照规则进行 encode 和 decode  

### 6.插入图像  
图片的创建方式与超链接相似，而且和超链接一样也有两种写法，行内式和参考式写法。这里只展示行内式一种写法，参考式可以根据超链接的语法推导出来，就不再复述。  
语法：在文档要插入图片的地方写!\[图片Alt\](图片URL "title"),图片Alt的意思是如果图片因为某些原因不能显示，就用定义的图片Alt文字来代替图片，图片Alt和title都可以省略，但建议写上  

> 我的Github：
> ！\[zhanglp的Github\]\(https://github.com/Young0510/Markdown-grammar/blob/master/Capture1.PNG "我的Github"\)  

效果：  
> 我的Github：
> ！[zhanglp的Github](https://github.com/Young0510/Markdown-grammar/blob/master/Capture1.PNG "我的Github")  

### 7.注脚  
语法：  
脚注是在需要标记脚注文字的后面增加一个方括号，方括号中的内容必须以 ^ 开头，再接着是数字、字符串标记,在文件的任意地方，你可以把这个脚注的内容定义出来  

**注意**：注脚与注脚之间必须空一行，不然会失效。成功后会发现，即使你没有把注脚写在文末，经Markdown转换后，也会自动归类到文章的最后。  
> 使用Markdown\[^1\]可以效率的书写文档，直接转换成HTML\[^2\]。

> \[^1\]Markdown是一种纯文本标记语言
> \[^2\]HyperText Markup Language 超文本标记语言  

效果：  
> 使用Markdown[^1]可以效率的书写文档，直接转换成HTML[^2]。

> [^1]Markdown是一种纯文本标记语言
> [^2]HyperText Markup Language 超文本标记语言  

### 8.分隔线  
你可以在一行中用三个以上的星号(*)、减号(-)、底线(_)来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格  
> \* \* \*  
> \*\*\*  
> \- \- \-  
> \-\-\-\-\-\-\-\-\-\-\-\-

效果：  
> * * *  
> ***
> - - -  
> ------------  

### 9