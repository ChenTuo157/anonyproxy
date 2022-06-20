###  tor浏览器+clash 匿名上网

爬取地址：https://limbopro.com/archives/torproject.html



本文目录

- [I. 主理人说](https://limbopro.com/archives/torproject.html#主理人说)
- [II. 关于 Tor](https://limbopro.com/archives/torproject.html#关于_Tor)
- [III. Tor 下载及安装](https://limbopro.com/archives/torproject.html#Tor_下载及安装)
- [IV. Tor 速度之谜（取决于代理速度）](https://limbopro.com/archives/torproject.html#Tor_速度之谜（取决于代理速度）)
- [V. Tor 的匿名性（挺好）](https://limbopro.com/archives/torproject.html#Tor_的匿名性（挺好）)
- [VI. Tor 必要设置（为Tor设置代理 - clash）](https://limbopro.com/archives/torproject.html#Tor_必要设置（为Tor设置代理_-_clash）)
- [VII. Tor 实用技巧](https://limbopro.com/archives/torproject.html#Tor_实用技巧)
- 实测

------



## I. 主理人说

本文于 [Tor 浏览器](https://www.torproject.org/zh-CN/) 内撰写与发布。

**洋葱**浏览器，顾名思义：像洋葱一样，剥开一层还有一层。

洋葱链路

[![洋葱浏览器-毒奶博客](https://limbopro.com/usr/uploads/2020/07/1455317164.png)](https://limbopro.com/usr/uploads/2020/07/1455317164.png)



关于匿名上网这件事，并非绝对可靠，有待检验；另外墙外并非法外；一定程度上来说，使用 Tor 上网还是有些许好处的，不想被网站记录你的真实（或代理）IP，倒是个很棒的方法。损失隐私换取便利，损失便利换取隐私。

谷歌等一些知名社交媒体对 Tor 中继IP似乎不是很友好，会放出大量验证码；



## II. 关于 Tor

https://www.torproject.org/zh-CN/ Tor 项目中文页
https://github.com/torproject GitHub 源码托管
https://tb-manual.torproject.org/zh-CN/about/ Tor 完全使用说明

Tor 是一个由虚拟通道组成的网络，可以提高自己在互联网上的隐私和安全性。Tor 会将您的流量通过 Tor 网络内的三个随机的服务器（也称节点）发送。链路中的最后一个中继（即“出口节点”）将流量发送到公共互联网。





## III. Tor 下载及安装

下载页面：https://www.torproject.org/zh-CN/download/



## IV. Tor 速度之谜（取决于代理速度）

[![Tor Speedtest.png](https://limbopro.com/usr/uploads/2020/03/115970289.png)](https://limbopro.com/usr/uploads/2020/03/115970289.png)



**如何能使 Tor 运行得更快? Tor 浏览器比其他的浏览器更慢吗?**

使用 Tor 浏览器有时会比其他浏览器慢。 Tor 的网络每日有超过一百万的用户浏览，但只有6000多个中继站来路由所有的通信，所以服务器有时会因过载造成延迟。此外，根据我们的设计，您的通信是在世界各地的志愿者服务器上不断传输的，所以一些堵塞和网络延迟总是不可避免的会出现。 您可以通过 [运行您自己的中继](https://community.torproject.org/relay/) 或鼓励他人这样做来帮助提高网络速度。 想要获取更多深入的回答，请参阅 [Roger 的话题博客文章](https://blog.torproject.org/blog/why-tor-is-slow) 和 [Tor 的公开研究专题：2018年版](https://blog.torproject.org/tors-open-research-topics-2018-edition) 关于网络性能的部分。 也就是说， Tor 比以前快的多了，你未必会注意到和其它浏览器相比的速度变化。

主理人建议使用非`深/沪港`之类与`香港`相关的节点，速度还是非常OK的（对等速率）。一家之言，具体还是得自己多试试几个节点；



## V. Tor 的匿名性（挺好）

[![Tor-limbopro.com.png](https://limbopro.com/usr/uploads/2020/03/635167558.png)](https://limbopro.com/usr/uploads/2020/03/635167558.png)



[![Tor security -ipv4.png](https://limbopro.com/usr/uploads/2020/03/1991381808.png)](https://limbopro.com/usr/uploads/2020/03/1991381808.png)



[![Tor security -ipv6.png](https://limbopro.com/usr/uploads/2020/03/1707965949.png)](https://limbopro.com/usr/uploads/2020/03/1707965949.png)



Tor 的一些特性使得`其匿名性略高于普通浏览器的无痕浏览模式`：参考 [Chrome 无痕浏览的工作原理](https://support.google.com/chrome/answer/7440301?co=GENIE.Platform%3DAndroid&hl=zh-Hans)；以及 Tor 安全设置说明：https://tb-manual.torproject.org/zh-CN/security-settings/；

访问 https://ip.sb/ 或 https://whoer.net/zh 查看你的IP；既不是你的真实IP（[网络运营商](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=13&cad=rja&uact=8&ved=2ahUKEwjx2IH10JToAhVRAxAIHagUDkAQmhMwDHoECA4QAg&url=https%3A%2F%2Fzh.wikipedia.org%2Fzh-cn%2F%E7%A7%BB%E5%8A%A8%E7%BD%91%E7%BB%9C%E8%BF%90%E8%90%A5%E5%95%86&usg=AOvVaw1AtwE1ePLSMYY47h2LaQzU)分配的IP），也不是你的代理IP（[机场](https://limbopro.com/865.html)），而是 Tor 的三层叠加的最后一层 IP；



## VI. Tor 必要设置（为Tor设置代理 - clash）

[![ClashX-端口.png](https://limbopro.com/usr/uploads/2021/04/1759662145.png)](https://limbopro.com/usr/uploads/2021/04/1759662145.png)



如果你跟博主一样也是使用 Clash，如ClashX，则可点击 ClashX 任务栏图标 - 展开 - 找到帮助按钮 - 端口 - sock，本地IP一般为：`127.0.0.1`（你可复制`127.0.0.1`到浏览器打开，提示 It's Works. 就是对的）；

**使用代理访问互联网**
[![Tor - Proxy.jpg](https://limbopro.com/usr/uploads/2020/03/947733436.jpg)](https://limbopro.com/usr/uploads/2020/03/947733436.jpg)



如上图，在设置中为你的 Tor 浏览器设置代理；个人不建议使用网桥，会非常慢。
**下载中文语言包**
[![Tor language.png](https://limbopro.com/usr/uploads/2020/03/1869202099.png)](https://limbopro.com/usr/uploads/2020/03/1869202099.png)



如上图，在设置中为你的 Tor 浏览器下载中文语言包；
*以上两步或需遵循先后次序，不然可能导致网速过慢而无法下载。



## VII. Tor 实用技巧

[![Switch tor relay ip.png](https://limbopro.com/usr/uploads/2020/03/1935296017.png)](https://limbopro.com/usr/uploads/2020/03/1935296017.png)

随时切换中继与伪造新[Uer-Agent](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/User-Agent)（身份标识）；





## 实测：

![241655692243_.pic](/Users/chentuo/Library/Containers/com.tencent.xinWeChat/Data/Library/Application Support/com.tencent.xinWeChat/2.0b4.0.9/6257f5817ba6ff01ee2d37b75255016a/Message/MessageTemp/ac337b5a84bb6e0402c4451562d565c3/Image/241655692243_.pic.jpg)



特点：隐秘性强，访问速度较慢