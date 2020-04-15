---
title: 从0学习网络编程（一）认识socket
date: 2020-04-14 22:45:45
tags:
---
# 目录
一、网络七层模型

二、TCP/IP协议簇

三、Socket的位置和作用

四、Socket过程详解，三次握手与四次分手

五、TCP连接的状态机

六、常用函数

七、简单例子

八、tcpdump观察

# 一、网络七层模型
 ![7层模型](从0学习网络编程（一）认识socket/7层模型.jpg)

# 二、TCP/IP协议簇
&emsp; TCP/IP协议不仅仅指的是TCP 和IP两个协议，而是指一个由FTP、SMTP、TCP、UDP、IP等协议构成的协议簇， 只是因为在TCP/IP协议中TCP协议和IP协议最具代表性，所以被称为TCP/IP协议。
 ![TCP/IP协议簇](从0学习网络编程（一）认识socket/TCPIP协议簇.png)
 
&emsp; 应用层：应用层是TCP/IP协议的第一层，是直接为应用进程提供服务的。

（1）对不同种类的应用程序它们会根据自己的需要来使用应用层的不同协议，邮件传输应用使用了SMTP协议、万维网应用使用了HTTP协议、远程登录服务应用使用了有TELNET协议。 [1] 

（2）应用层还能加密、解密、格式化数据。 [1] 

（3）应用层可以建立或解除与其他节点的联系，这样可以充分节省网络资源。 [1] 

&emsp; 运输层：作为TCP/IP协议的第二层，运输层在整个TCP/IP协议中起到了中流砥柱的作用。且在运输层中，TCP和UDP也同样起到了中流砥柱的作用。 [1] 

&emsp; 网络层：网络层在TCP/IP协议中的位于第三层。在TCP/IP协议中网络层可以进行网络连接的建立和终止以及IP地址的寻找等功能。 [1] 

&emsp; 网络接口层：在TCP/IP协议中，网络接口层位于第四层。由于网络接口层兼并了物理层和数据链路层所以，网络接口层既是传输数据的物理媒介，也可以为网络层提供一条准确无误的线路。

# 三、Socket的位置和作用
![Socket的位置](从0学习网络编程（一）认识socket/Socket位置.png)
Socket 是应用层与TCP/IP协议簇之间的接口，TCP/IP协议簇的实现细节对于应用层不可见，应用层只需要知道Socket接口就可以组装数据与对端进行通信。

一个标准的简单的建立socket的交互如下所示。
![socket交互](从0学习网络编程（一）认识socket/socket交互图.png)



# 参考
https://blog.csdn.net/pashanhu6402/article/details/96428887
https://blog.csdn.net/weixin_39634961/article/details/80236161
https://www.jianshu.com/p/066d99da7cbd
https://www.cnblogs.com/baiduboy/p/8127913.html
