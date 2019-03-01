NVM是Node.js的版本管理工具，可以创建Node.js不同版本的隔离环境，避免不同版本之间相互干扰。有了NVM就可以方便的进行Node.js的安装、卸载、版本切换等等。  

NVM是一个独立软件包，不同于TJ/N是一个NPM package.  

### 安装NVM
1. 安装&更新  
你可以采用cURL获取安装脚本的方式：  
```bash
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash
```
或者，采用Wget获取安装脚本的方式：
```bash
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash
```

2. 验证安装  
执行‘command -v nvm’命令验证NVM是否安装成功  
```bash
$ command -v nvm
nvm
```

### 安装Node.js
#### 安装指定版本的Node.js  
`nvm install v10.15.1`
#### 查看已安装的Node.js

**查看已安装的版本 nvm ls**  
```
$ nvm ls
         v6.9.1
        v7.10.1
->      v8.10.0
default -> v8.10.0
node -> stable (-> v8.10.0) (default)
stable -> 8.10 (-> v8.10.0) (default)
iojs -> N/A (default)
lts/* -> lts/dubnium (-> N/A)
lts/argon -> v4.9.1 (-> N/A)
lts/boron -> v6.16.0 (-> N/A)
lts/carbon -> v8.15.0 (-> N/A)
lts/dubnium -> v10.15.1 (-> N/A)
```
**也可以通过目录查看 ls -a**
```
$ ls -a ~/.nvm/versions/node
.       ..      v6.9.1  v7.10.1 v8.10.0
```

### 切换Node版本
切换指定版本
```
nvm use v8.10.0
```

查看当前版本
```
node -v
```
### 设置默认Node版本
设置默认的node版本 *nvm alias default <version>*  
```
$ nvm alias default v10.15.1
default -> v10.15.1
```
用 *nvm current* 查看当前Node版本  
$ nvm current
v10.15.1

### 卸载Node
卸载指定版本NodeJS
```
$ nvm uninstall v6.9.1
```
