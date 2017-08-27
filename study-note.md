学习笔记
===================================================
## Sublime Text的Package Control-----install Start
import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())

以上还有重要的一步，需要直接ping http://sublime.wbond.net/，得到ip地址，然后加入到hosts文件中。

依然无法安装其他插件，原因是sublime-settings中的
"channels": [
		"https://packagecontrol.io/channel_v3.json"
	],
地址无法访问。
后下载至本地，在搭建TOMCAT服务器才能成功。未成功GIT
"channels": [
        "http://127.0.0.1:8080/pms/resources/js/channel_v3.json"
    ]
中间有直接ping packagecontrol.io得到ip地址 50.116.34.243 加入hosts中
https://raw.githubusercontent.com/xiaoxinfly/resources/master/sublime/channel_v3.json
这个地址才对

## sublime markdown插件
1.sublime设置高亮的快捷键 shift+ctrl+p 输入ssm “set syntax"
2.之后，按已经设置好的快捷键"alt+m"(preferences-->key binding-->user settings)
3.或者按shift+ctrl+p--> Markdown Preview: preview in browser"
4.shift+ctrl+p-->输入markdown preview-->选择save to html(会在当前目录生成html文件)

## sublime evernote插件
国内：https://app.yinxiang.com/api/DeveloperToken.action 
国际：https://www.evernote.com/api/DeveloperToken.action
Create a developer token
Preferences > Package Settings > Evernote >Settings - User
add以下内容：
{
 "noteStoreUrl": "",
 "token": ""
}
添加快捷键
[
	{ "keys": ["ctrl+e", "ctrl+o"], "command": "open_evernote_note" },
    { "keys": ["ctrl+s"], "command": "save_evernote_note", "context": [{"key": "evernote_note"}, {"key": "evernote_has_guid"}] },
    { "keys": ["ctrl+s"], "command": "send_to_evernote", "context": [{"key": "evernote_note"}, {"key": "evernote_has_guid", "operator": "equal", "operand": false}] }
]
ctrl+e，ctrl+o依次按完后会打开印象笔记
ctrl+s按完后会将笔记保存并且同步到印象笔记

## sublime install theme
1. ctrl+shift+p->install package->搜索"Theme – Soda"->Preferences->settings->user->添加"theme": "Soda Dark.sublime-theme"
2. ctrl+shift+p->install package->搜索"Monokai Extended"->Preferences->Color Theme->Monokai Extended(最后一项)
3. ctrl+shift+p->install package->搜索"Markdown Extended"->标记文档为Markdown Extended即可高亮

## git笔记
1. 创建和切换到新分支 git branch -b [分支名] 相当于 git branch develop(创建新分支)后，git checkout develop(切换到develop分支)
2. git add . 将当前目录下所有已经更改和添加的文件添加到分支中
3. git commit执行后，进入VIM模式，按insert或c键可进行编辑状态，当编辑结束后按ESC键，再按大写状态下的Z键保存编辑信息并提交
4. git status 可查看git当前文件是否已修改，并列出来
5. git commit时message的格式化

> <类型>(可选):<主题>
> //空一行
> <内容>

其中标题是必需的，内容若无需过多描述可以省略。标题部分只有一行，包括字段类型和主题，类型是用于说明commit的类别，只允许使用下面7个标识：

* init：项目初始化（用于项目初始化或其他某种行为的开始描述，不影响代码）
* feat：新功能（feature）
* fix：修补bug
* docs：文档（documentation)
* opt：优化和改善，比如弹窗进行确认提示等相关，不会更改逻辑和具体功能等
* style：格式（不影响代码运行的变动）
* refactor：重构（即不是新增功能，也不是修改bug的代码变动）
* test：增加测试
* other：用于难以分类的类别（不建议使用，但一些如删除不必要的谁的，更新,ignore之类的可以使用

（可选）类型后面可以加括号，括号内填写主要动力的范围，比如按功能模块分

* \# :表示模块
	- \#studet --> 表示学生模块
	- \#all --> 表示所有模块

内容包含两个部分，分别是what和why。


## table editor插件

#### 激活 & 关闭
1. `ctrl` + `shift` + p
2. 输入 `Table Editor`
3. 选择 `Enable for current syntax` (激活)或 `Disable for current syntax` (关闭)

#### 使用
输入
	
	|Name|Phone

然后加快捷键: `ctrl` + `k` , `enter`
得到

	| Name | Phone |
	|------|-------|
	|      |       |

此时光标定位在虚线下那一行

........详细请查看[Table Editor 使用方法](https://segmentfault.com/a/1190000007935021)

其他快捷键如下：

* `tab` 光标跳动下一个单元格
* `enter` 光标跳动到下一行的最后一个单元格
* `ctrl` + `k` , `enter` 插入一行分割线后跳到新一行的第一个单元格
* `ctrl` + `k` , `-` 在光标所在行的下面插入一行分割线
* `alt` + `enter` 拆分行 前提，下面有分割线，另一个功能是移动数据
* `ctrl` + `j` 合并2行
* `alt` + `shift` + `右` 添加一列
* `alt` + `shift` + `左` 删除一列
* `alt` + `shift` + `上` 添加一行
* `alt` + `shift` + `下` 删除一行
* `alt` + `左` 将所在的列换在左边
* `alt` + `右` 将所在的列换在右边
* `ctrl` + `k` , `shift` + `|` 选中后，连按这两个快捷键可将CSV转换为表格

|    Name   | Phone | Age |
|-----------|-------|-----|
| Xiao Mei  |   444 |   4 |
| Xiao Ming |   666 |   6 |

$x^{y^z}=(1+{\rm e}^x)^{-2xy^w}$ 

* * *


  1. ECMAScript 6.0（以下简称 ES6）是 JavaScript 语言的下一代标准，已经在2015年6月正式发布了。它的目标，是使得 JavaScript 语言可以用来编写复杂的大型应用程序，成为企业级开发语言。
  2. 用工具ES-Checker来检查各种运行环境对ES6的支持情况
npm install -g es-checker
es-checker
3.Babel转码器
Babel是一个广泛使用的ES6转码器，可以将ES6代码转为ES5代码，从而在现有环境执行。这意味着，可以用ES6的方式编写程序，又不用担心现有环境是否支持。
例子：
//转码前
input.map(item => item + 1);
//转码后
input.map(function(item){
return item + 1;
});
上面的原始代码用了箭头函数，Babel将其转为普通函数，就能在不支持箭头函数的JavaScript环境执行。
  ● 配置文件.babelrc
位置：Babel的配置文件是.babelrc，存放在项目的根目录下；
功能：用来设置转码规则的插件；
基本格式：
{
"presets":[],
"plugins":[]
}
presets字段设定转码规则 ，可以根据需要安装。
# 最新转码规则
npm install --save-dev babel-preset-latest
#react 转码规则
npm install --save-dev babel-preset-react
除此外还有针对不同阶段的转码规则
npm install --save-dev babel-preset-stage-0
npm install --save-dev babel-preset-stage-1
npm install --save-dev babel-preset-stage-2
npm install --save-dev babel-preset-stage-3
{
"presets":["latest","react","stage-2"],
"plugins":[]
}
  ● 命令行转码bable-cli——Babel提供的babel-cli工具用于命令行转码
安装命令如下

一个tab或者4个空格，markdown会变成代码格式。。。
markdown的文本内容怎么缩进