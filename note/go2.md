

# 2019秋招 | golang的面经 秋招总结 三（字节跳动、映客直播）

作者：打代码啦啦啦

链接：[https://www.nowcoder.com/discuss/145338](http://link.zhihu.com/?target=https%3A//www.nowcoder.com/discuss/145338%3Ftype%3D2%26order%3D3%26pos%3D15%26page%3D1)

来源：牛客网



## **趣丸**

趣丸的面试难度堪比bat，但是薪水偏低了

**一面**

- 为什么选pg
- go的new和make区别
- go怎么从源码编译到二进制文件
- go的调度模型
- go的锁如何实现，用了什么cpu指令
- go的runtime如何实现
- 看过sql的连接池实现吗，没有
- 最近学什么新技术？c++简单网络库

**二面**

- c++的map和go的map的区别（红黑树和hashtable）
- ctx包了解吗？有什么用？
- go什么情况下会发生内存泄漏？（他说ctx没有cancel的时候，这个真不知道）
- 怎么实现协程完美退出？
- 智力题：1000瓶酒中有1瓶毒酒，10只老鼠，7天后毒性才发作，第8天要卖了，怎么求那瓶毒酒？
- 简单dp题，n*n矩阵从左上角到右下角有多少种走法（只限往下和往右走）

**HR面**

- 瞎扯

## **映客直播**

映客是京东开奖那段时间投的补招，他们公司用的golang也挺多，可惜也是北京，薪水比京东好一点

**一面**

- 面经丢失

**二面**

- 实习项目
- 用channel实现定时器？（实际上是两个协程同步）
- channel的实现？不了解
- go为什么高并发好？讲了go的调度模型
- git回滚
- 看什么书，怎么学习
- redis的zset用什么实现，除了跳跃表
- 操作系统内存管理？进程通讯，为什么共享存储区效率最高
- http的状态码
- tcp和udp
- udp的头部
- http和tcp的关系

**三面**

- 怎么看一本书？
- 如果团队有一个人的任务做不完，你也很忙，你会怎么做？

## **Ucloud**

Ucloud是做服务器的，跟七牛云很像，但Ucloud主要是C++，七牛云主要是golang。一面完说通过，约二面，后面说那周深圳的总监没空，调下周，后面没消息，估计凉凉了

**一面**

- 实现一个hashmap，解决hash冲突的方法，解决hash倾斜的方法
- c++的模板跟go的interface的区别
- 怎么理解go的interface
- 100亿个数选top5，小根堆

## **字节跳动**

头条很早就笔试了，A了一道多，刚好赶上补招，给面试，拖了几周担心拖不了就面试了，面试中也有一些不会的，不过三面后加hr微信问过没过，hr说过了，第二天跟我联系，然后就担心没有部门捞（头条三面通过要有部门要才有offer），第二天就谈薪资收到offer了

**一面**

- go代码运行结果（闭包函数）
- git和svn区别，模型
- 唯一订单号问题，并发量高的话怎么解决
- hash表设计要注意什么问题
- 数组和为n的数组对
- 最大连续子数组和
- redis容灾，备份，扩容
- 跳跃表，为什么使用跳跃表而不使用红黑树

**二面**

- 输入url后涉及什么
- tcp怎么找到哪个套接字
- ipc方式，共享存储区原理
- 进程虚拟空间布局
- 进程状态转换
- 线程的栈在哪里分配
- 多个线程读，一个线程写一个int32会不会有问题，int64呢（这里面试官后来说了要看数据总线的位数，32位的话写int32没问题，int64就有问题）
- 判断二叉树是否为满二叉树
- lru实现
- 一个大整数（字符串形式表示的），移动字符求比它大的数中最小的

**三面**

- MVC优点
- 点赞系统设计

------

## **资源 ：**

## **博客**

- [legendtkl](http://link.zhihu.com/?target=http%3A//legendtkl.com/)：这个大佬写的博客挺有深度，主要也是go，可以看看
- [基础知识CyC2018](http://link.zhihu.com/?target=https%3A//github.com/CyC2018/CS-Notes)：一些面试的基础知识

## **书籍**

- 高性能mysql
- redis设计与实现
- Linux/UNIX系统编程手册
- Linux高性能服务器编程
- UNIX网络编程
- UNIX环境高级编程
- [编程之法：面试和算法心得](http://link.zhihu.com/?target=https%3A//github.com/julycoding/The-Art-Of-Programming-By-July)
- 剑指offer
- 图解http（简洁易懂）
- TCP/IP详解



**与作者交流：**[https://www.nowcoder.com/discuss/145338](http://link.zhihu.com/?target=https%3A//www.nowcoder.com/discuss/145338%3Ftype%3D2%26order%3D3%26pos%3D15%26page%3D1)

**更多笔经面经：**[https://www.nowcoder.com/discuss?order=0&type=2](http://link.zhihu.com/?target=https%3A//www.nowcoder.com/discuss%3Forder%3D0%26type%3D2)