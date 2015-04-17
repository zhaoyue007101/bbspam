# bbspam是一款性能非常强劲的敏感词过滤服务 #
### Date: 2010.11 ###
### author: Chancey ###


&lt;hr&gt;



# 说明： #

现今，Web2.0网站往往面临着一件非常窘困的事情。
对于用户的输入内容很难控制，那就意味着随时都有可能遇到"违禁词"、"敏感词"，不是被迫删除信息，就是被强制和谐，或者投入大量的人力进行监控。
为了营造一个和谐的互联网环境，bbspam由此而诞生。

bbspam是一款敏感词过滤服务，对于所有的输入内容进行过滤，过滤后的内容会将敏感词替换为xxx,降低人力成本


# 特点: #

C/C++编写<br><br>
基于ICE，稳定、高效<br><br>
简单的分词算法<br><br>
敏感词列表自定制<br><br>

<h1>客户端支持：</h1>

C++<br><br>
PHP<br>

<h1>使用平台：</h1>

Linux<br>
<br>
<h1>安装说明：</h1>
<pre><code>*******************************************<br>
 Spam Server<br>
 Author: Chancey<br>
*******************************************<br>
==========================<br>
Dependencies<br>
==========================<br>
GCC<br>
C++<br>
ZeroC-ICE 3.4.1<br>
<br>
WEBSITE:<br>
http://www.zeroc.com/<br>
<br>
DOWNLOAD:<br>
http://www.zeroc.com/download/Ice/3.4/Ice-3.4.1.tar.gz<br>
<br>
INSTALL:<br>
aptitude install gcc g++ install libdb4.6++-dev libexpat1-dev libmcpp-dev libbz2-dev libssl-dev<br>
<br>
COMPILE:<br>
cd Ice-3.4.1/cpp<br>
make<br>
make install<br>
cp /opt/Ice-3.4.1/lib/* /usr/lib/<br>
<br>
=======================================<br>
Compilation and Configrue Spam Server:<br>
=======================================<br>
COMPILE:<br>
make<br>
<br>
EDIT CONFIG:<br>
vi conf/spam.conf<br>
<br>
RUN:<br>
./spamserver &amp;<br>
<br>
==========================<br>
Client:<br>
==========================<br>
<br>
PHP: ./client/php/<br>
C++: ./client/cpp/spamclient<br>
<br>
</code></pre>

<h1>性能测试:</h1>
<table><thead><th> <b>测试环境</b> </th><th> <b>吞吐量/s(大文本)</b> </th><th> <b>请求数/s(小文本)</b> </th></thead><tbody>
<tr><td> 虚拟机 Xeon-2 core 2.0 </td><td> 6.43M </td><td> 7000-8000 </td></tr>
<tr><td> Xeon-4 core 2.0 </td><td> 8.6M </td><td> 9000-10000 </td></tr>
<tr><td> Xeon-4 core 2.0 (-O2编译优化)</td><td> 18M </td><td> 9000-10000 </td></tr>