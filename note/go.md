# 2019秋招 | golang的面经 秋招总结一 （七牛云、360、京东）

[![牛客网](https://pic4.zhimg.com/v2-5072d494cf599bff95e2803681d9cb58_xs.jpg)](https://www.zhihu.com/org/niu-ke-wang-53)

[牛客网](https://www.zhihu.com/org/niu-ke-wang-53)



已认证的官方帐号



31 人赞了该文章

作者：打代码啦啦啦

链接：[https://www.nowcoder.com/discuss/145338](http://link.zhihu.com/?target=https%3A//www.nowcoder.com/discuss/145338%3Ftype%3D2%26order%3D3%26pos%3D15%26page%3D1)

来源：牛客网



戳 -> [校招-面经](http://link.zhihu.com/?target=https%3A//chasiny.github.io/) 我主要用的还是go，虽然语言不是很重要，但投的基本上是跟go有关的公司，也有一些c++的公司，想往go发展的可以参考我的面经

## **春招**

春招基本上是过完年回来开始，建议寒假开始复习然后回来就可以找实习了。我春招投的比较晚，后面投的公司不是很多，基本被刷简历，能面试的只有七牛云，然而第一次面试被各种吊打，春招后面去了深圳一家小公司实习了两个月

## **七牛云**

七牛云的技术还是不错的，虽然实习不想去上海（建议实习不要看地点，实习很短不要介意地点）

**一面**

- go的调度
- go struct能不能比较
- go defer（for defer）
- select可以用于什么
- context包的用途
- client如何实现长连接
- 主协程如何等其余协程完再操作
- slice，len，cap，共享，扩容
- map如何顺序读取
- 实现set
- 实现消息队列（多生产者，多消费者）
- 大文件排序
- 基本排序，哪些是稳定的
- http get跟head
- http 401,403
- http keep-alive
- http能不能一次连接多次请求，不等后端返回
- tcp与udp区别，udp优点，适用场景
- time-wait的作用
- 数据库如何建索引
- 孤儿进程，僵尸进程
- 死锁条件，如何避免
- linux命令，查看端口占用，cpu负载，内存占用，如何发送信号给一个进程
- git文件版本，使用顺序，merge跟rebase



------



## **秋招**

实习到八月底就回来参加秋招了，然而还是被吊打，我的秋招一直持续到十一月初，主要还是想找深圳的公司，最终签了字节跳动。

## **360**

360是秋招第一个面试的公司，在实习期间请假面试的，一天基本就面完所有流程，但最终还是进入备胎池（巨深），虽然也不想去北京，但还是点名批评360的备胎池

**一面**

一面是个小胖小胖的面试官，说我的实习经历挺丰富的（几个校内项目跟一个小公司实习项目），基本上问项目跟场景，中间穿插一些基础知识

- 讲实习项目的简单业务流程，数据库有水平拆分什么的吗？没有，数据量还没到，然后没啥问的
- Slice与数组区别，Slice底层结构
- 项目里的微信支付这块，在支付完微信通知这里，收到两次微信相同的支付通知，怎么防止重复消费（类似接口的幂等性），说了借助Redis或者数据库的事务
- 项目里的消息推送怎么做的（业务有关）
- Go的反射包怎么找到对应的方法（这里忘记怎么问的，直接说不会，只用了DeepEqual，简单讲了DeepEqual）
- Redis基本数据结构
- Redis的List用过吗？底层怎么实现的？知道但是没用过，不知道怎么实现
- Mysql的索引有几种，时间复杂度
- InnoDb是表锁还是行锁，为什么（这里答不出来为什么，只说了行锁）
- Go的channel（有缓冲和无缓冲）
- 退出程序时怎么防止channel没有消费完，这里一开始有点没清楚面试官问的，然后说了监听中断信号，做退出前的处理，然后面试官说不是这个意思，然后说发送前先告知长度，长度要是不知道呢？close channel下游会受到0值，可以利用这点（这里也有点跟面试官说不明白）
- 用过什么消息中间件之类吗？没有
- 有什么问题吗？评价？后面还有面试，后面再问吧

**二面**

二面的面试官好像是部门技术总监，面完了加微信，可能需要Go的人，感觉很多不会然后给过了，面完面试官人超好，微信推荐我看书

- 生产者消费者模式，手写代码（Go直接使用channel实现很简单，还想着面试官会不会不让用channel实现，不用channel的可以使用数组加条件变量），channel缓冲长度怎么决定，怎么控制上游生产速度过快，这里没说出解决方案，只是简单说了channel长度可以与上下游的速度比例成线性关系，面试官说这是一种解决方案
- 手写循环队列
- 写的循环队列是不是线程安全，不是，怎么保证线程安全，加锁，效率有点低啊，然后面试官就提醒Go推崇原子操作和channel
- 写完代码面试官说后面问的问题回答就可以，不知道的话没关系
- Linux会不会，只会几个命令，面试官就说一共也就一百多个命令
- TimeWait和CloseWait原因
- 线段树了解吗？不了解，字典树？了解
- 看过啥源码，nsq（Go的消息中间件），简单问了我里面的waitgroup包证明我看过
- sync.Pool用过吗，为什么使用，对象池，避免频繁分配对象（GC有关），那里面的对象是固定的吗？不清楚，没看过这个的源码
- 有什么问题吗？评价？基础不错，Linux尚缺，Go的理解不够深入，高级数据结构不了解，优点是看源码
- 后面面试官讲了他们做的东西，主要是广告部分，说日均数据量至少百万以上，多达上亿，高并发使用Go支撑，有微服务，服务治理，说我需要学的东西挺多的

## **CVTE**

CVTE 面的是 C++ 开发，一面就挂了，记的面经不是很多

**一面**

- 证明二叉树的叶子节点跟度数为2的节点的关系
- 唯一索引和主键索引
- 智能指针
- 字符串解析为数字（考虑浮点型）

## **京东**

京东本来是现场面的，但运气好，几轮的面试官都允许改成电话面试，岗位是京东云部门的Golang开发工程师，很少有大公司明招golang，面试官说主要做docker和跟调度相关。收到offer后给三天的时间考虑，虽然非常想去京东，方向也非常感兴趣，最终还是希望跟女朋友留在深圳就放弃了京东的offer。

**一面**

其中穿插一小部分扩展，例如单点登录，tcp粘包

- 项目1
- 项目2
- 项目3
- 手写洗牌

**二面**

- 项目1处理粘包断包实现，面试官以为是negle算法有关，解释了下negle跟糊涂窗口综合征有关，然后面试官觉得其他项目是crud就没问了
- 看什么书？以前看redis设计与实现之类的，现在看linux相关
- goroutine调度用了什么系统调用，这个不会，面试官想从go问到操作系统，然后以为***作系统基础不好，就问了操作系统问题
- 进程虚拟空间分布，全局变量放哪里？答上来了，操作系统就不问了
- 有没有网络编程，有，怎么看连接状态？netstat，有哪些？ESTABLISHED，LISTEN等等，有异常情况吗？TIME_WAIT很多，为什么？大量短链接
- 介绍部门

**HR面**

- 优缺点