在软件测试工作中，压力测试是一项很重要的工作。比如在一个网站上线之前，能承受多大访问量、在大访问量情况下软件性能怎么样？这些数据指标好坏将会直接影响到用户体验。但是，在压力测试中存在一个共性，那就是压力测试的结果与实际负载结果不会完全相同，就算压力测试工作做的再好，也不能保证100%和线上性能指标相同。面对这些问题，我们只能尽量去想方设法去模拟。所以，压力测试非常有必要，有了这些数据，我们就能对自己做的产品上线做到心中有数。

1、Webbench是一个非常简单又很好用的web压力测试工具

2、Webbench能测试出在相同硬件上，不同服务的性能以及不同硬件上同一个服务的运行状况。

3、webbench的标准测试可以向我们展示服务器的两项内容：每秒钟相应请求数和每秒钟传输数据量。

4、webbench不但能具有便准静态页面的测试能力，还能对动态页面进行测试的能力，也支持对含有SSL的安全网站进行静态或动态的性能测试。

5、Webbench最多可以模拟3万个并发连接去测试网站的负载能力。

6、Webbench的安装

注意：安装的前提：需要安装gcc和make
yum -y install ctags

wget http://home.tiscali.cz/~cz210552/distfiles/webbench-1.5.tar.gz

tar -zvxf webbench-1.5.tar.gz

cd webbench-1.5

make && make install

7、Webbench使用方法：

webbench -c 100 -t 60 http://www.google.com/

100个并发请求，持续60秒

-c 为并发数 -t为时间（秒）

结果：

Benchmarking: GET http://www.google.com/

100 clients, running 60 sec.

Speed=5426 pages/min, 177921 bytes/sec.

Requests: 5426 susceed, 0 failed.

成功数、失败数 及 速度

8、性能测试

压力测试工作应该放到产品上线之前，而不是上线以后

测试时尽量跨公网进行，而不是内网

测试时并发应当由小逐渐加大，比如并发100时观察一下网站负载是多少，网站能否正常操作，并发200时又是多少、网站打开缓慢时并发是多少、网站打不开时并发又是多少
