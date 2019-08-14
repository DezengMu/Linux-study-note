# 使用GitHub时遇到的一些问题

## 1. 由于切换账号，导致本地文件上传失败

* 错误类型：

  > unable to access 'htttp://......' requested URL returned error: 403

* 错误原因：

  windows 默认还保留着旧帐号的信息，所以用新的github账号无法上传

* 解决办法：

  在windows(win10,win7没试过)找到**“控制面板—用户账户—凭据管理器—windows凭据”**，找到下面的**”普通凭据“**.删除掉旧的github 账户信息，就可以重新提交了
  
* 参考博文：[切换Git账号后Push失败403错误的解决过程](https://blog.csdn.net/Aman1984/article/details/77774811)



## 2. 由于修改了网站的GitHub上的文件，导致本地文件上传失败

* 错误类型：

> ![rejected]  master->master........
>
> hit “git pull ...” before pushing again ......

* 错误原因：

  因为之前在线修改过GitHub 上的文件，导致与本地仓库里的文件不一致，所以上传失败

* 解决办法：

  依次输入以下两条命令

  `git pull origin master --allow -unrelated -histories`

  `git push -u origin master -f`

  即可解决。
  
* 参考博文：[Git上传项目提示Push rejected: Push to origin/master was rejected解决办法](https://blog.csdn.net/qq_35733535/article/details/78884454)