计算机网络
===
#*TCP问题
  ##*陈述三次握手
    ###*第一次：client向server发送请求报文，其中包含一个同步synchronization信号。client开始等候回复
    ###*第二次：server收到client的请求报文，返回一个应答报文，其中包含一个同步信号和一个应答报文
    ###*第三次：client收到server的应答报文，也向server发送一个应答报文段，并进入established状态，当server收到这个应答报文，也进入established状态，连接建立
