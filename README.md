# 4ksj-checkin

2024/10/18 修复4ksj签到，弃用hao4k签到

TODO : 修复推送

### 建议提取 cookie 用该浏览器插件复制  把cookie列表先勾上 然后点击cookie列表 直接点copy all  （自己复制cookie会有问题！）
https://chrome.google.com/webstore/detail/header-cookie-qrcode/echlhpliefhchnkmiomfpdnehakfmpfl/related?hl=zh-CN


#### 脚本功能：

1、通过Github Action自动定时运行 app.js 脚本。

2、通过cookies自动登录（[https://www.4ksj.com/](https://www.4ksj.com/))，脚本会自动进行签到。

3、可以通过“推送加” （[http://www.pushplus.plus](http://www.pushplus.plus))，自动发通知到微信上。

4、可以通过“PushDeer” （[http://www.pushdeer.com](http://www.pushdeer.com))，自动推送到**手机通知**上。 请使用**官方在线版**。 

5、可以通过“Server酱”（[http://sc.ftqq.com/3.version](http://sc.ftqq.com/3.version))，自动发通知到微信上。

6、可以通过“bark”（[https://github.com/Finb/Bark](https://github.com/Finb/Bark))，自动发通知到ios上。


#### 食用姿势：

1. 先“Fork”本仓库。（不需要修改任何文件！）

2. 注册4ksj

3. 登录4ksj后获取cookies。（简单获取方法：用上面的浏览器插件直接获取）。

4. 在自己的仓库“Settings”里根据需要创建“Secrets => Actions => New repository secret”，分别是：（不开启通知，只需要创建一个COOKIE即可）

   - COOKIE （**必填**； **填写Hao4K的cookie**）  已弃用！!!
   - SJCOOKIE （**选填**； **填写4K视界的cookie**；不设置会尝试用Hao4K的cookie签到）
   - PPTOKEN （填写推送加的token, 不开启不用填）
   - PDKEY （填写PushDeer的key, 不开启不用填）
   - SCKEY （填写server酱sckey，不开启server酱则不用填）
   - BARKKEY (填写bark的key，不开启bark推送则不用填，默认使用官方服务器发送，如需自定义请通过BARKSERVER配置)
   - BARKSERVER (填写bark的服务器地址，不开启bark推送则不用填)

5. 以上设置完毕后，每天0点和6点会自动触发，并会执行自动签到（**0点4ksj经常抽风**，故多增加一次执行,可自行改时间）。


