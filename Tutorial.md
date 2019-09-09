# 入门基础

这里只简单介绍如何快速开发一个 `CLI`，具体业务需要根据实际来开发，以下主要通过三个例子渐进式学习

- 从 0 到 1 开发命令行工具
- 命令帮助文档
- 命令行交互（input、confirm、list、checkbox 等等）


## 创建一个 `CLI`，例子 [xcli](./packages/xcli)

一个可以本地运行的 `CLI`，只需要两个文件即可：

- xcli/bin/xcli

```js
#!/usr/bin/env node
console.log('Welcome to awesome-cli')
```

- xcli/package.json

```json
{
  "name": "xcli",
  "version": "0.1.0",
  "bin": {
    "xcli": "bin/xcli"
  }
}
```

通过 `npm link` 为此工具创建链接，方面调试和测试。

```bash
# 进入 xcli 目录
$ cd xcli
# 创建链接
$ npm link
# 执行 xcli 命令
$ xcli
Welcome to awesome-cli
```

## 命令帮助文档，例子 [xnpm](./packages/xnpm)

一个命令行工具最基本就是工具界面，执行一个命令，输出帮助文档  
[commander](https://github.com/tj/commander.js#commands) 是一个命令行界面的解决方案，我们将使用它，结果如下：

```bash
$ xnpm 
Usage: xnpm <command>

Options:
  -v, --version      output the version number
  -h, --help         output usage information

Commands:
  install|i [name]   install packages
  run [script-name]  run script
  help [cmd]         display help for [cmd]
$ xnpm install --save
xnpm install success ; use --save
```

## 命令行交互，例子 [xvue-cli](./packages/xvue-cli)

除了帮助文档，命令还需交互，如 input、confirm、list、checkbox 等等。

[inquirer](https://github.com/SBoudrias/Inquirer.js) 是一个用户与命令行交互的工具，我们将使用它，结果如下：

```bash
$ xvue create project
Xvue CLI v0.1.0

? Please pick a preset: (Use arrow keys)
> default (babel, eslint)
  Manually select features
? Check the features needed for your project 
  ◉ Babel
❯ ◉ TypeScript
  ◯ Progressive Web App (PWA) Support
  ◯ Router
  ◯ Vuex
  ◯ CSS Pre-processors
  ◉ Linter / Formatter
```
