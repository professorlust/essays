微信API接口接入
=================

![wechat](https://farm4.staticflickr.com/3716/11872041935_032fee59b9_o.png)

今晚，打开微信公众平台的网页时突然想试试微信开发者的API，毕竟这个比较火嘛，很多企业甚至是个人都接入了微信的API接口开展业务。

正当要申请时，看到微信提供了测试帐号，于是就申请了一个来测测（有效期只有1天），首先借着某某服务器（=.=）来进行了验证，这个很简单，马上就通过了。然后在界面那里看到了不少接口，想试试「自定义菜单」的接口，照着例子弄了一下，嗯，还挺不错的，如果有个自定义菜单的话估计能更好玩。

接下来我就想拿我这个公众号（没有认证）来试试，这尼玛，认证是通过了，但是就只有三个接口可以使用，一个接收你们的消息，另一个就是接收后给你们回复了，还有一个事件推送（比如添加/取消关注时触发的）。哎，基本上没有太多用呢=.=

然后分别试了试这三个接口，都可以了，就是功能太少了。突然有个想法，**假如你有微信公众号API接入的需要可以联系我（目前只支持非认证号），我可以免费提供这样一个程序和服务器资源（这不是广告）** 当然，如果是认证号，更欢迎联系我哦^_^

最后，真的很想吐槽一下微信的接口，其实做得并不好。文档写得比较糟糕，不够详细，有些东西没说清楚；代码区域没有格式化；字段使用的编码风格又不统一（这让服务端写得很难受）；最讨厌的就是一会用json，一会用xml，看不懂（因为我的程序始终用json，然而java自带的xml解析简直是灭绝师太，而我又不想再添加一个库）；另外，错误处理的时候返回200的状态码，这实际上是不符合http协议的规范的。btw，已经上传到微信的图片还不能从微信那里获得，还得另外上传一个到别处╮(╯_╰)╭

以上，技术贴。今晚码了一晚上代码，原谅我再码这一坨大家看不懂的狗屁文字。

---
2014-01-10


### EOF
```yaml
background: /assets/images/default.jpg
date: 2014-01-10T23:30:39+08:00
hide: false
license: cc-40-by
location: Nanning
summary: 假如你有微信公众号 API 接入的需求可以联系我，我可以免费提供这样的程序和服务器资源 :)
tags:
- Campus
weather: ""
```
