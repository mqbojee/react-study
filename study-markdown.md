Markdown语法快速入门
===============
#### 一、标题语法
1. **一级标题：** `=` 或 `#` 。`=` 写在标题文字的下一行，`#` + 空格 + 标题文字，如：`# 一级标题`；
2. **二级标题：** `-` 或 `##` 。`-` 写在标题文字的下一行，`##` + 空格 + 标题文字，如：`## 二级标题`；
3. **三级标题：** `###` 。`###` + 空格 + 标题文字，如：`### 三级标题`。

	备注：`#` 的个数表示几级标题，按个人需求决定使用 `=` 或 `-` 或 `#`，最高为6级，即 `###### 六级标题`。

#### 二、段落语法
一个段落是由一个以上的连接的行句组成，而一个以上的空行则会划分出不同的段落（空行的定义是显示上看起来像是空行，就被视为空行，例如有一行只有空白和 tab，那该行也会被视为空行），一般的段落不需要用空白或换行缩进。

	备注：如果一行的前后只有空白，且此行的开头是4个空格或tab，没有排序的语法，那么接下来，会被渲染成代码块，就像现在这个备注。

#### 三、区块引用语法
**语法：** `>` + 空格 + 文字
**案例：** 代码与效果依次如下

    > 这是一个区块引用
    > ### 这是一个区块引用

> 这是一个区块引用
> ### 这是一个区块引用

#### 四、修辞和强调语法
**语法：** MarkDown可使用 `*` 号和 `__` （底线）来标记需要强调的区段。
**用法：** `*文字*` 即 *文字*，`**文字**` 即 **文字**，`__文字__` 即 __文字__。
**案例：** 代码及效果依次如下
	
	This is a *apple*.
	This is a big _apple_.
	This is a **big** apple.
	This is a big __apple__.

> This is a *apple*.
> This is a big _apple_.
> This is a **big** apple.
> This is a big __apple__.

#### 五、列表语法
**语法：** MarkDown可使用 `*` 或 `+` 或 `-` 来添加无序列表，使用 `1. ` (数字 + 点号) 来添加有序列表。
**案例：** 代码及效果依次如下

	* This is a apple.
	* This is a pear.

> * This is a apple.
> * This is a pear.

	+ This is a apple.
	+ This is a pear.
	
> + This is a apple.
> + This is a pear.

	- This is a apple.
	- This is a pear.
	
> - This is a apple.
> - This is a pear.

	1. This is a apple.
	2. This is a pear.
	
> 1. This is a apple.
> 2. This is a pear.

#### 六、链接语法
**语法：** Markdown的链接语法有两种，分别是 行内 形式：`[链接展示的文字](链接的地址 链接的标题)` ，其中“链接的标题”可不填写；参考 形式：`[链接展示的文字][序号]` ，其中序号对应自己定义的内容 `[序号]: 链接地址 链接标题` 。
**案例：** 代码及效果依次如下

	This is an [example link](http://baidu.com).
	This is an [example link](http://baidu.com "百度").

	[Google][1]
	[BaiDu][2]
	[1]: http://google.com/ "Google"
	[2]: http://baidu.com "BaiDu"

> This is an [example link](http://baidu.com).
> This is an [example link](http://baidu.com "百度").
> [Google][1]
> [BaiDu][2]

[1]: http://google.com/ "Google"
[2]: http://baidu.com "BaiDu"

#### 七、图片语法
**语法：** MarkDown的图片语法和链接语法很相似。同样有 行内 和 参考 两种形式，行内形式：`![提示用的文本](图片的地址 图片的标题)` ，参考形式：`![提示用的文本][序号]` 。
**案例：** 代码及效果依次如下

	![测试1](https://raw.githubusercontent.com/xiaoxinfly/resources/master/images/image1.jpeg "测试1")
	![测试2][3]
	[3]: https://raw.githubusercontent.com/xiaoxinfly/resources/master/images/totoro-1.jpg "测试2" 


> ![测试1](https://raw.githubusercontent.com/xiaoxinfly/resources/master/images/image1.jpeg "测试1")
> ![测试2][3]

[3]: https://raw.githubusercontent.com/xiaoxinfly/resources/master/images/totoro-1.jpg "测试2" 

#### 八、代码语法
**语法：** MarkDown的代码语法，用 “``” 来标记一部分文字可标识代码，除此之外，如果前后都有空行，中间行的缩进4个空格或者一个tab，就能标识为代码块。
**案例：** 代码及效果依次如下

标识input框标签：`<input/>`

	`<input/>`

标识代码块示意：

	<div>
		<input type="text" title="代码块案例" />
	</div>

[文档源码所在GitHub地址，点击查看](https://raw.githubusercontent.com/xiaoxinfly/react-study/master/study-markdown.md)