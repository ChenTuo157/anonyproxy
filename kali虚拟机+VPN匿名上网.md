# How to install a VPN on Kali Linux

爬取地址：https://protonvpn.com/support/official-linux-vpn-kali/

Our Linux app officially supports Kali Linux. If you are using the community-developed version of our Linux app, please uninstall it before installing this app.

![Proton VPN on Kali Linux](https://protonvpn.com/support/wp-content/uploads/2021/07/protonvpn-on-kali-linux.png)

**1. Our DEB package installs the Proton VPN repository on your system.**

[*Download the Proton VPN DEB package*](https://protonvpn.com/download/protonvpn-stable-release_1.0.1-1_all.deb)

**2. Install the Proton VPN repository**

Open a terminal and run the following:

```
sudo apt-get install {/path/to/}protonvpn-stable-release_1.0.1-1_all.deb
```

Replace {/path/to/} with the path to where you download the file. For example:

```
sudo apt-get install ~/Downloads/protonvpn-stable-release_1.0.1-1_all.deb
```

**3. Update the apt-get package list**

Then enter:

```
sudo apt-get update
```

**4. Install the app**

And finally:

```
sudo apt-get install protonvpn
```

Once installed, simply log in with your Proton account credentials. If you do not yet have an account, you can [sign up for a Free Proton VPN plan for Linux](https://protonvpn.com/free-vpn/linux).

The Proton VPN Linux app is now ready to secure your internet browsing and allow you to access the internet without censorship blocks. However, **please note that the system tray icon may not work on Kali Linux**. This is because the system tray icon requires dependencies that have been deprecated. 

[*Learn how to use the Proton VPN Linux app*](https://protonvpn.com/support/knowledge-base/official-linux-client/)





#### 实测（环境有问题，还没有解决）：

![](http://www.chentuo.asia/images/5.png)

proton免费节点信号太差了，连不上



![](http://www.chentuo.asia/images/kali.png)

windows10上的kali与宿主机之间通讯有问题







