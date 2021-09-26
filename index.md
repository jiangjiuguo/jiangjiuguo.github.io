## 蒋九国
[登录页面](https://jiangjiuguo.github.io/Login)

### （第一步）新建仓库
- 新建仓库步骤省略，最后我们得到一个仓库地址：
```
https://github.com/wangle1218/×××××××××.git
```
### （第二步）进入要上传的文件夹，初始化上传文件夹仓库
```
$ cd ../python/machineLearningCode/
$ git init
```
### （第三步）添加所有文件到git
```
$ git add .
$ git commit -m "first commit
```
### （第四步）连接到guthub仓库
```
$ git remote add origin https://github.com/wangle1218/********.git
```
- 如果不是第一次上传，可能会提示一下信息：
```
fatal: 远程 origin 已经存在。
```
- 这时只需要将远程配置删除，重新添加即可；
```
$ git remote rm origin
$ git remote add origin https://github.com/wangle1218/********.git
```
### （第五步）输入“git push -u origin master”，上传项目到Github。
- 这里会要求输入Github的账号密码，按要求输入就可以。
```
$ git push -u origin master
```
- 如果提示错误：
```
error: 无法推送一些引用到 'https://github.com/wangle1218/*********.git'
提示：更新被拒绝，因为远程仓库包含您本地尚不存在的提交。这通常是因为另外
提示：一个仓库已向该引用进行了推送。再次推送前，您可能需要先整合远程变更
提示：（如 'git pull ...'）。
提示：详见 'git push --help' 中的 'Note about fast-forwards' 小节。
```
- 则可以尝试强行上传：
```
$ git push -u origin +master
```
