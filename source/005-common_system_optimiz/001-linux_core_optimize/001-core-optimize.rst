常用内核参数调优
#####################

参考网络资源：  http://blog.51cto.com/yangrong/1321594


http://blog.51cto.com/yangrong/1567427


:tcp_syn_retries:
    | 默认值: 5  建议值: 1
    | 对于一个新建连接，内核要发送多少个 SYN 连接请求才决定放弃。不应该大于255，默认值是5，对应于180秒左右时间。。(对于大负载而物理通信良好的网络而言,这个值偏高,可修改为2.这个值仅仅是针对对外的连接,对进来的连接,是由tcp_retries1决定的)




    ######################## 针对lvs，关闭网卡LRO/GRO功能
    # 现在大多数网卡都具有LRO/GRO功能，即网卡收包时将同一流的小包合并成大包 （tcpdump抓包可以看到>MTU 1500bytes的数据包）交给 内核协议栈；LVS内核模块在处理>MTU的数据包时，会丢弃；
    # 因此，如果我们用LVS来传输大文件，很容易出现丢包，传输速度慢；
    # 解决方法，关闭LRO/GRO功能，命令：
    # ethtool -k eth0 查看LRO/GRO当前是否打开
    # ethtool -K eth0 lro off 关闭GRO
    # ethtool -K eth0 gro off 关闭GRO










