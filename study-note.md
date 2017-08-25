# Sublime Text的Package Control-----install Start
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
# Sublime Text的Package Control-----install End

# sublime markdown插件 start
1.sublime设置高亮的快捷键 shift+ctrl+p 输入ssm “set syntax"
2.之后，按已经设置好的快捷键"alt+m"(preferences-->key binding-->user settings)
3.或者按shift+ctrl+p--> Markdown Preview: preview in browser"
4.shift+ctrl+p-->输入markdown preview-->选择save to html(会在当前目录生成html文件)
# sublime markdown插件 end

# sublime evernote插件 start
国内：https://app.yinxiang.com/api/DeveloperToken.action 
国际：https://www.evernote.com/api/DeveloperToken.action
Create a developer token
Preferences > Package Settings > Evernote >Settings - User
add以下内容：
{
 "noteStoreUrl": "",
 "token": ""
}
# sublime evernote插件 end
#------------------------------->>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
#------------------------------->>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>



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
