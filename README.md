# 微信mac/ipad协议，webapi本地部署
首次可以免费试用1天，想要继续租用或购买请联系qq：929918989

# 操作指南
1.新机器首次需要进入cmd，关闭windows数据保护DEP（dep可能会导致不安全代码闪退）：bcdedit.exe/set {current} nx AlwaysOff，重启电脑<br/><br/>
2.下载项目，进入mac/ipad目录，打开WeChatServer.exe.config配置api端口、websocket端口、管理员密码等参数
```  
    <add key="WebApiHost" value="22221" />
    <add key="WebSocketHost" value="22222" />
    <add key="AdminPassword" value="123456" />
```
3.右键管理员运行WeChatServer.exe，看见  开启服务... 证明服务已经开启<br/><br/>
4.在浏览器运行http://localhost:22221/swagger/ 即可查看所有webapi文档<br/><br/>
5.请先仔细阅读Test.html代码，通过websocket创建连接，获取二维码登录后才可调用api。详细信息可以查看浏览器控制台Console和Network<br/><br/>
6.微信登录获取二维码需要参考Test.html中websocket方式创建websocket链接来获取二维码登录。uuid为创建websocket时传入参数<br/><br/>
7.在微信成功登录以后，即可通过Http post的方式传入uuid来操作微信了<br/><br/>
8.有时微信多次非正常退出或者操作频繁时，会造成Api接口异常崩溃，可以运行进程保活工具<br/><br/>
# 奖励计划
每多10个star，则随机赠送1人协议租用！
# 声明
仅供自己学习研究使用，引起任何法律纠纷概不负责
# QQ交流群
<a target="_blank" href="//shang.qq.com/wpa/qunwpa?idkey=c8ba88cf98ceff400b56732220c3b60fdf714b2f79852c854a3d11644b6a10a0">微信mac/ipad/android协议QQ群</a><br/>
![demo3](https://github.com/weixinbao/WeChatXY/blob/master/QQ.png) <br/>
