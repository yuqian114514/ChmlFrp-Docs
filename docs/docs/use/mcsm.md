

:::tip
本项非 ChmlFrp 官方项目，若有问题请联系 [语千](https://github.com/yuqian114514) 或 加入交流群 [加入群聊MCSM FRP 模板集市吃土豆交流群 | 修BUG！](https://qm.qq.com/q/VV5ZbdmdiO)，官方不接受使用 MCSManager FRP 模板的任何问题反馈
:::


# MCSManager FRP模板集市

- MCSManager FRP模板集市是由 [语千](https://github.com/yuqian114514) 基于各大FRP厂商的命令行工具和 [MCSManager](https://github.com/MCSManager/MCSManager) 面板制作

- ChmlFrp MCSManager 模板使用了由 ChmlFrp 开发的命令行工具 [ChmlFrp Frpc](https://panel.chmlfrp.net/tunnel/download) 及 由 [语千](https://github.com/yuqian114514) 开发的 [专属命令行启动脚本](https://github.com/yuqian114514/mcsm-frp-market-sh_bat) 制作
## MCSManager FRP模板集市项目链接

- [GitHub](https://github.com/yuqian114514/mcsm-frp-market)

- [gitee](https://gitee.com/yuqian114514/mcsm-frp-market)

- [gitea](https://gitea.com/yuqian114514/mcsm-frp-market)


# MCSManager FRP模板集市部署

## 部署MCSManager

没有部署MCSManager可前往 [https://docs.mcsmanager.com/zh_cn/](https://docs.mcsmanager.com/zh_cn/) 查看教程部署

## 安装模板

> 💡 *如果已经安装过可跳过*

1. 前往您的 MCSManager 面板登录
2. 在面板侧边栏或顶部导航中，找到并点击 **「模版市场」** 
3. 点击 **「编辑应用市场」** 按钮
4. 点击 **「操作」** → 选择 **「清空当前模板」** → 弹出确认框后点击 **「确认」** 
5. 点击 **「导入」**→ 选择 **「从链接导入」** → 输入 下方 链接 → 确定
```URL
https://github.nswrz.cn/https://github.com/yuqian114514/mcsm-frp-market/raw/refs/heads/master/%E9%87%8D%E6%9E%84%E7%89%88/market.json
```
6.  点击 **「保存到面板」**

## 安装 ChmlFrp-frpc 模板

1. 在模板市场找到 FRP 专区并选择你的服务器
2. 找到 ChmlFrp-frpc 模板安装

## 启动 ChmlFrp-frpc

1. 打开你的 MCSManager 面板，找到你刚安装的 ChmlFrp-frpc 模板
2. 开启您的实例
3. 启动后会显示下方页面 输入2即可

```shell
================ 授权方式 ================
  1) 本机运行 (自动打开浏览器并接收回调)
  2) 云服务器/远程 (手动把浏览器地址栏 URL 粘贴回来)
=========================================
请选择授权方式 [默认 2]: 
```
4. 现在你应该看到了一串链接
```shell
[*] 请在【你自己电脑】的浏览器中打开以下链接完成授权:
  https://account-api.qzhua.net/oauth2/authorize?xxxxxxxxxxxxxxxxxxxxxxx
```

复制到浏览器打开 登录账号授权

5. 授权后浏览器会跳到 http://127.0.0.1:47902/callback?... 这个打不开的页面 把这一串链接复制到控制台输入

> 💡 *这个页面打不开是正常的*

6. 输入对应要开启的隧道数字 开启隧道

7. 您可通过 `114514.com:1145` 访问您的服务了，恭喜您成功使用 MCSManager FRP模板 启动了 ChmlFrp！


# 如何切换及重新启动

## 如何进行重启启动隧道
1. 打开你的 MCSManager 面板，找到你刚安装的 ChmlFrp-CLI 模板
2. 开启您的实例
3. 您会看见下方页面 此时输入 0 回车即可

```shell
===================================
 上次隧道: xxxxxxxxxxxxxxxxxxxxxxxxxxx
===================================
  1) 启动上一次的隧道
  2) 切换隧道
  0) 退出
===================================
请选择: 
```

## 如何切换隧道

1. 打开你的 MCSManager 面板，找到你刚安装的 ChmlFrp-CLI 模板
2. 开启您的实例
3. 您会看见下方页面 此时输入 2 回车

```shell
===================================
 上次隧道: xxxxxxxxxxxxxxxxxxxxxxxxxxx
===================================
  1) 启动上一次的隧道
  2) 切换隧道
  0) 退出
===================================
请选择: 
```
4. 输入对应要开启的隧道数字 开启隧道
