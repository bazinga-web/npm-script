## Build Setup

```bash
# Install dependencies
npm install

# 建议不要用cnpm  安装有各种诡异的bug 可以通过如下操作解决npm速度慢的问题
npm install --registry=https://registry.npm.taobao.org

# Serve with hot reload at localhost:9528
npm run dev

# Build for production with minification
npm run build

# Build for production and view the bundle analyzer report
npm run build --report
```

## git commit 规范

### Header
Header部分只有一行，包括三个字段：type（必需）、scope（可选）和subject（必需）。

### type
用于说明 commit 的类别，只允许使用下面7个标识。

- feat：新功能（feature）
- fix：修补bug
- docs：文档（documentation）
- style： 格式（不影响代码运行的变动）
- refactor：重构（即不是新增功能，也不是修改bug的代码变动）
- test：增加测试
- chore：构建过程或辅助工具的变动

### scope
- scope用于说明 commit 影响的范围，比如数据层、控制层、视图层等等，视项目不同而不同。
- 如果你的修改影响了不止一个scope，你可以使用*代替。

### subject
subject是 commit 目的的简短描述，不超过50个字符。
其他注意事项：

- 以动词开头，使用第一人称现在时，比如change，而不是changed或changes
- 第一个字母小写
- 结尾不加句号（.）

## Feature

- check version(node, npm)
    - postinstall、preinstall、semver