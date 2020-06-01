## 简介
`pre`和`post`
举例来说，运行 npm run test 的时候，分 3 个阶段：

1.  检查 scripts 对象中是否存在 pretest 命令，如果有，先执行该命令；
2.  检查是否有 test 命令，有的话运行 test 命令，没有的话报错；
3.  检查是否存在 posttest 命令，如果有，执行 posttest 命令；

```
"pretest": "node test/01.js",
"test": "node test/02.js",
"posttest": "node test/03.js"
```

![](https://i.loli.net/2020/06/01/TDlUS5OiCyr19cX.png)

## 实际应用
通过钩子将代码检查、测试运行、覆盖率收集这些步骤串起来

```
"lint": "npm-run-all --parallel lint:*",
"pretest": "npm run lint",
"test": "mocha tests/",

// 1.  precover，收集覆盖率之前把之前的覆盖率报告目录清理掉；
// 2.  cover，直接调用 nyc，让其生成 html 格式的覆盖率报告；
// 3.  postcover，清理掉临时文件，并且在浏览器中预览覆盖率报告；

"precover": "rm -rf coverage",
"cover": "nyc --reporter=html npm test",
"postcover": "rm -rf .nyc_output && opn coverage/index.html"
```