[图解http](https://book.douban.com/subject/25863515/)   [电子书PDF](https://pan.baidu.com/s/1tYSRQnibqf-1mqnJWUlfBQ) <br>
#### 一、
HTTP（HyperText Transfer Protocol，超文本传输协议）<br>
通常使用的网络（包括互联网）是在 TCP/IP 协议族的基础上运作
的。而 HTTP 属于它内部的一个子集。
#### 二、
下面则是从客户端发送给某个 HTTP 服务器端的请求报文中的内容：

GET /index.htm HTTP/1.1 <br>
Host: hackr.jp

起始行开头的GET表示请求访问服务器的类型，称为方法
（method）。随后的字符串 /index.htm 指明了请求访问的资源对象，
也叫做请求 URI（request-URI）。最后的 HTTP/1.1，即 HTTP 的版本
号，用来提示客户端使用的 HTTP 协议功能。
综合来看，这段请求内容的意思是：请求访问某台 HTTP 服务器上的
/index.htm 页面资源。
请求报文是由请求方法、请求 URI、协议版本、可选的请求首部字段
和内容实体构成的
  
 ![请求报文](https://github.com/hannibal2017/studyRecord/blob/master/picture/1550048364.jpg) <br>
 图：请求报文 <br>
 接收到请求的服务器，会将请求内容的处理结果以响应的形式返回.
 
 HTTP/1.1 200 OK <br>
Date: Tue, 10 Jul 2012 06:50:15 GMT<br>
Content-Length: 362<br>
Content-Type: text/html<br>
<html><br>
……<br>

在起始行开头的 HTTP/1.1 表示服务器对应的 HTTP 版本。
紧挨着的 200 OK 表示请求的处理结果的状态码（status code）和原因
短语（reason-phrase）。下一行显示了创建响应的日期时间，是首部
字段（header field）内的一个属性。
接着以一空行分隔，之后的内容称为资源实体的主体（entity
body）。
响应报文基本上由协议版本、状态码（表示请求成功或失败的数字代
码）、用以解释状态码的原因短语、可选的响应首部字段以及实体主
体构成。

![http响应报文](https://github.com/hannibal2017/studyRecord/blob/master/picture/1550048443(1).jpg) <br>
图：响应报文<br>

#### 三、
http三次握手: <br>
![http三次握手](https://github.com/hannibal2017/studyRecord/blob/master/picture/1550044365.jpg)

#### 四、
https [HTTPS原理和CA证书申请](http://blog.51cto.com/11883699/2160032)<br>
步骤整理如下：<br>
1. 以阿里云的举例，进入[阿里云ssl](https://common-buy.aliyun.com/?spm=5176.7968328.1266638..15c812325jEN1k&commodityCode=cas#/buy) 
2. 选择symantec，免费型DV ssl，购买
3. 到ssl控制台，添加申请信息。域名要先提前申请注册。添加后，等待生效，一般是几个小时。
4. NGINX和Tomcat修改相关的信息，详情查看[HTTPS原理和CA证书申请](http://blog.51cto.com/11883699/2160032)相关的部分

