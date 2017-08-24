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
