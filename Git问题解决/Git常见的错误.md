## 1、error: failed to push some refsto‘远程仓库地址’

> <font style="background: pink">出现原因：我们在创建仓库的时候，都会勾选“使用Reamdme文件初始化这个仓库”这个操作初识了一个README文件并配置添加了忽略文件。因为github中的README.md文件不在本地代码目录中</font>

<font color=blue>解决办法：</font>

```js
git pull --rebase origin master
```

## 2、fatal: unable to access 'https://github.com/tbwwlys/learningNotes.git/': OpenSSL SSL_read: Connection was reset, errno 10054

<font color=blue>解决办法：</font>

```js
git config --global http.sslVerify "false"
```

