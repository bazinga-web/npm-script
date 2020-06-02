### 文件系统操作

*   [rimraf](https://github.com/isaacs/rimraf) 或 [del-cli](https://www.npmjs.com/package/del-cli)，用来删除文件和目录，实现类似于 `rm -rf` 的功能；
*   [cpr](https://www.npmjs.com/package/cpr)，用于拷贝、复制文件和目录，实现类似于 `cp -r` 的功能；
*   [make-dir-cli](https://www.npmjs.com/package/make-dir-cli)，用于创建目录，实现类似于 `mkdir -p` 的功能；


### cross-var 引入变量

Linux 和 Windows 下引用变量的方式是不同的，Linux 下直接可以用 `$npm_package_name`，而 Windows 下必须使用 `%npm_package_name%`，我们可以使用 [cross-var](https://www.npmjs.com/package/cross-var) 实现跨平台的变量引用：

```
"echo": "cross-var echo $npm_package_name"
```
### cross-env 设置环境变量

```
npm i cross-env -D

 "scripts": {
     "test": "cross-env NODE_ENV=test mocha tests/",
},
```