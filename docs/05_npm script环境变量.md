### 预定义变量

首先我们来看预定义变量，通过运行 `npm run env` 就能拿到完整的变量列表，这个列表非常长，这里我使用 `npm run env | grep npm_package | sort` 拿到部分排序后的预定义环境变量：
![](https://i.loli.net/2020/06/01/9ASbqIRXnh2sVvM.png)

#### 使用
```
"testname": "echo $npm_package_name"
```

### 自定义变量
```json
// package.json

"config": {
    "port": 3000
},
"script": {
    "cover:open": "opn http://localhost:$npm_package_config_port",
}

```
*   新增的命令 `cover:serve` 中同时使用了预定义变量 `$npm_package_version` 和自定义变量 `$npm_package_config_port`；
*   预览覆盖率报告的方式从直接打开文件修改为打开网址： `http://localhost:$npm_package_config_port`；