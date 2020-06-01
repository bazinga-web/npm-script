### 多个命令串行（&&）
```
"test": "npm run lint:js && npm run lint:css && npm run lint:json && npm run lint:markdown && mocha tests/"
```
串行命令失败后，后续的命令无法执行


### 多个命令并行（&）
```
"test": "npm run lint:js & npm run lint:css & npm run lint:json & npm run lint:markdown & mocha tests/"
```

### 更好的方式（npm-run-all）
串行
```
"test": "npm-run-all lint:js lint:css lint:json lint:markdown mocha"
```
串行优化（通配符*）
```
"test": "npm-run-all lint:* mocha"
```

并行
```
 "test": "npm-run-all --parallel lint:* mocha"
```