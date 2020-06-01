### 传递参数
```
"eslint:fix": "npm run eslint -- --fix"
```
![](https://raw.githubusercontent.com/bazinga-web/images/master/20200601/162434.png)

### npm run 添加命令注释
```
"eslint": "# 运行eslint \n    eslint test/index.js",
```
注意`\n`后的空格是为了保持输出有缩进效果
![](https://i.loli.net/2020/06/01/MiZN4zDYAvSVGQO.png)

### 调整npm script 运行时日志输出
- 默认输出
![](https://i.loli.net/2020/06/01/lsnvaZxGT3wXBOQ.png)

- 静默输出（-s）
`--loglevel silent` 或者 `--silent`
![](https://i.loli.net/2020/06/01/5bZoPDM2YNz7F9c.png)

- 全面输出（-d）
`--loglevel verbose` 或者 `--verbose`
![](https://i.loli.net/2020/06/01/3iV2ZH1QqoJEcjh.png)
