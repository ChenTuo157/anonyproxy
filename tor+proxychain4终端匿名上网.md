### tor+proxychains-ng终端匿名上网

安装地址：https://www.meiwen.com.cn/subject/qkgwwftx.html

mac m1因架构问题编译解决方法：https://blog.csdn.net/sanqima/article/details/123158915



实测：

![截屏2022-06-20 14.41.02](/Users/chentuo/Public/redteam/annoy/截屏2022-06-20 14.41.02.png)

第一个会话：tor

第二个会话：proxychains4 curl ifconfig.me 采用代理之后的公网ip地址

第三个会话：curl cip.cc 本地对网站进行测试时的公网ip



如上：本地终端ip地址为上海的ip，使用tor+proxychains之后变成了tor的ip

特点：访问速度一般





![](https://gitee.com/gitFlutterStudent/images/blob/master/%E6%88%AA%E5%B1%8F2022-06-20%2015.21.26.png)

注意：tor+proxychains使用起来访问速度比较慢，需要延迟timeout

修改配置文件：将原来的延时从15s和8s改为150s和80s

tcp_read_time_out 15000
tcp_connect_time_out 80000

经过这个设置后，便可以通过proxychains来访问到cip.cc