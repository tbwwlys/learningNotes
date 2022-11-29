# Git 操作指南

## 第一步 设置git 账号名 和 绑定的邮箱

```js
git config --global user.name "这个双引号里填写的是你在 github 注册的账号"
git config --global user.email "这个双引号里填写的是你在 github 注册的邮箱"
```

## 第二步 生成密钥

```js
ssh-keygen -t rsa  //密钥在 C:\Users\zxx\.ssh 文件夹 
```

<strong style="background:pink">将id_rsa.pub中的密钥绑定到GitHub中</strong>

## 第三步 将更改的代码暂存起来

```js
此命令会把所有更改的文件全部暂存起来。
git add . 

如果要单个来，只需要 . 替换成对应的文件名即可。
git add temp.txt
```

## 第四步将暂存的改动提交到本地的版本库

```js
# -m 参数表示可以直接输入后面的 message，简要说明这次改动。
git commit -m "xxx"
```

## 第五步 将本地分支版本上传到远程并合并

```js
# git push 的命令格式一般是
git push <远程主机名> <本地分支名>：<远程分支名>
例如：git push origin master:master

当然，一般情况下，我们都不用写后面的，直接 git push 即可。
```

此处简要写了git操作，之后需要补充
