2021.10.19  16：30 34min

介绍一下协程？和线程的区别？具体协程是怎么调度的？

介绍一下项目。

程序运行的时候前台和后台的区别在哪里？

http的底层是tcp还是udp？

tcp和udp的区别？

四次挥手time_wait过多的时候会出现什么问题？

（我回答道跟SYN连接在一起了解）

-time_wait期间还能有新的socket连接吗？

回答：处于该状态的socket什么时候可以再次使用：

- 2MSL之后
- 如果处于2MS期间，重用连接那么要保证新连接的TCP的Seq也就是序列号要比之前的大
- 如果处于2MS期间，重用的连接要保证后续的时间戳要比之前的连接的时间戳更晚

只有满足上面的条件才不会在发生新连接上出现老连接的延迟的IP分组，满足第一个条件则不会出现延迟的IP分组，如果满足后面的条件那么延迟的IP分组即使出现在新连接上也会被直接丢弃进而不会影响现有通信数据。





有没有情况是，端口到了65535，time_wait的连接到10万的情况？

time_wait最多的个数是多少？

（我想到http2.0的多路复用。一个tcp连接传多个信息。



http的长连接和短链接的区别？

（我回答心跳包，长连接能持续传输信息，优缺点。



线程池项目讲一下？

（我提到争夺线程的时候，有惊群问题的考虑。



谈一谈锁？

乐、悲。

乐观：CAS和版本号，ABA问题。



8核的主机的线程池有多少线程合适？

-cpu密集型：核心数+1

-io密集型：核心数/(1-阻塞系数)



两个数据库引擎了解吗？讲一讲ｉｎｎｏｄｂ的索引结构。

（我讲了ｂ＋树的结构，以及如何防止笛卡尔积。



不知道为什么，面完秒挂。可能是ｋｐｉ面了吧。感觉自己回答的也还可以。