# Awesome-cli
如何更好的开发命令行工具

## 入门教程

[极简的 CLI 入门教程](Tutorial.md)

## 第三方库介绍

第三方库能让我们解放生产力，让我们专注于命令行工具的开发

### 脚手架

- [commander](https://github.com/tj/commander.js) 一个命令行界面的解决方案
- [inquirer](https://github.com/SBoudrias/Inquirer.js) 命令行交互工具
- [chalk](https://github.com/chalk/chalk) 改变字体颜色，背景颜色
- [cli-spinners](https://github.com/sindresorhus/cli-spinners) loading 显示
- [update-notifier](https://github.com/yeoman/update-notifier) 版本号更新提示器
- [boxen](https://github.com/sindresorhus/boxen) 在命令行创建盒子界面

### 配置文件

常见格式有：ini、toml、yaml、json、xml、hocon 等等，可以根据自己实际项目选择自己需要的格式。

以上格式皆可用来读取配置数据，但同时支持读写的还是使用 json 方便。

- [confman](https://github.com/Houfeng/confman) 配置文件加载器（支持多种解析器）
- [toml-require](https://github.com/BinaryMuse/toml-require) toml 加载器
- [js-yaml](https://github.com/nodeca/js-yaml) yarm 解析器
- [hocon](https://github.com/lightbend/config) hocon 解析器
- [iniparser](https://github.com/shockie/node-iniparser) ini 解析器

### 文件管理

- [fs-extra](https://github.com/jprichardson/node-fs-extra) 扩展 fs 模块
- [vinyl-fs](https://github.com/gulpjs/vinyl-fs) 读取多个文件，支持正则
- [rimraf](https://github.com/isaacs/rimraf) 删除文件

### 工具库

- [lodash](https://github.com/lodash/lodash) 开发工具库
- [url-polyfill](https://github.com/lifaon74/url-polyfill) 解析 url
- [path-to-regexp](https://github.com/pillarjs/path-to-regexp) url 正则表达式，匹配 url
- [think-helper](https://github.com/thinkjs/think-helper) 辅助函数（is*、md5、extend、uuid、chmod）
- [dayjs](https://github.com/iamkun/dayjs) 日期时间处理器

### 代码压缩

- [uglify-js](https://github.com/mishoo/UglifyJS2) 压缩 js
