# 李奇的静态博客
使用 Hugo 搭建的静态网站。

## 下载 Hugo
去官网下载即可。

## 打开本地开发服务器
```bash
../hugo.exe server
```

## 创建一篇文章
```bash
../hugo.exe new directory-name/file-name.md
```

## 打包生成资源
在项目根目录执行此命令即可生成资源到 public/ 目录中
```bash
../hugo.exe
```

## 部署
我是通过腾讯云云开发中的静态网站托管服务进行部署的。

### 下载腾讯云开发 CLI 工具
```bash
npm i -g @cloudbase/cli
tcb -v
tcb login
```
### 部署命令
进入 public/ 目录，执行此命令，envId 通过腾讯云控制台中的云开发-环境总览页面查看
```bash
tcb hosting:deploy . -e envId
```