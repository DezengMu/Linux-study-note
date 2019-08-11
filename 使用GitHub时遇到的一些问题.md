# 使用GitHub时遇到的一些问题

## 1. 由于切换账号，导致本地文件上传失败

* 错误类型：

  > unable to access 'htttp://......' requested URL returned error: 403

* 错误原因：

  windows 默认还保留着旧帐号的信息，所以用新的github账号无法上传

* 解决办法：

  在windows(win10,win7没试过)找到**“控制面板—用户账户—凭据管理器—windows凭据”**，找到下面的**”普通凭据“**.删除掉旧的github 账户信息，就可以重新提交了