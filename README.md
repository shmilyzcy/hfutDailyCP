<div align="center">
<h1 align="center">HFUT今日校园自动签到</h1>
<img src="https://img.shields.io/github/issues/choya-lee/hfutDailyCP?color=green">
<img src="https://img.shields.io/github/stars/choya-lee/hfutDailyCP?color=yellow">
<img src="https://img.shields.io/github/forks/choya-lee/hfutDailyCP?color=orange">
    <img src="https://img.shields.io/github/license/choya-lee/hfutDailyCP?color=red">
</div>

### 使用必读

1. 本项目仅适用于`合肥工业大学`的今日校园打卡

2. 以下账号、密码即`新信息门户`的账号(学号)和密码

### 实现功能

1. 支持单人、多人打卡推送，格式见 `使用说明步骤4`
2. 脚本在每天14：30左右自动签到，可自行更改签到时间
3. 添加微信文本推送 **（可选功能，如需使用请参照企业微信开放API）**

<details>
<summary><b>企业微信开放API</b></summary>

##### 1. 推送展示

**推送结果将于脚本签到完成后通过微信发给你，如下图**

![push](https://gitee.com/choyalee/fig_bed/raw/master/img/202201311801776.png)

##### 2. 介绍

​	本项目采用**纯文本模式**推送，更加直观

​	接口参考地址：https://www.52pojie.cn/thread-1338005-1-1.html

1. 接口说明：利用企业微信开放api，与普通微信即时通讯。 无需下载企业微信，只是借用企业微信api！是一款类似于`server酱`的一款「程序员」和「服务器」之间的通信软件。能够让服务器即时找到负责它的沙雕程序员！

2. 对比server酱：能够`更直观`的获取服务器传递过来的信息，而不是`server酱`关注公众号后进来的<u>`卡片消息`</u>，还需要点一下才能看到。

3. 接口地址：https://api.htm.fun/api/Wechat/text_card/

   请求方式：GET/POST

##### 3. 注册指南

1. 【注册企业微信】，[点击这里](https://work.weixin.qq.com/)注册企业微信，无需企业认证！

2. 【创建程序】，获取AgentId&Secret，点击[应用管理]-[创建应用]根据提示创建一个新应用。保存好你的AgentId&Secret

3. 【获取corpid企业ID】，点击[我的企业]-[企业信息] 在最下方获取企业ID 

4. 【启用微信插件】，点击[我的企业]-[微信插件] 用普通微信扫码二维码。

   |    参数    | 必须 |        说明        |
   | :--------: | :--: | :----------------: |
   |   corpid   |  是  |       企业ID       |
   | corpsecret |  是  |   应用的凭证密钥   |
   |  agentid   |  是  |       应用ID       |
   |    text    |  是  | 推送内容，支持HTML |

   </details>

### 使用说明

1. 右上角fork本仓库

![fork](https://github.com/choya-lee/hfutDailyCP/raw/master/img/fork.png)

2. 点击导航栏Action，启用workflow


![action](https://github.com/choya-lee/hfutDailyCP/raw/master/img/action.png)

​	[下图采用其他仓库做演示]

![workflow](https://github.com/choya-lee/hfutDailyCP/raw/master/img/workflow.png)



3. 点击setting -> secret -> 新建一个secret

![secret](https://github.com/choya-lee/hfutDailyCP/raw/master/img/secret.png)

4. **非微信推送：**在`name`栏中填`INFO`，`value`中填入`账号`和`密码`，用空格隔开

   **微信推送：**在`name`栏中填`INFO`，`value`中填入`账号`、`密码`、`corpid`、`corpsecret`和`agentid`，用空格隔开

![info](https://github.com/choya-lee/hfutDailyCP/raw/master/img/info.png)


---

### 常见问题

1. 若脚本无法运行，请检查action中workflow是否启用
2. 如脚本有bug，请自行研究；若无法自行解决，请发issue描述你的问题
2. 如有其他问题，请通过邮箱反馈：lzyfrwk@163.com

### 声明

1. 此脚本仅供学习交流，**禁止个人盈利**

2. 脚本使用过程中，若存在瞒报误报所造成的损失由使用者个人承担

