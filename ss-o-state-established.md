#显示指定网络协议的所有连接
使用“`ss -o state established '( dport = :protocol or sport = :protocol )'`”命令可以显示所有网络协议为`protocol`的链接。  
举个例子：  

    [root@localhost nan]# ss -o state established '( dport = :ssh or sport = :ssh )'
	Recv-Q Send-Q                        Local Address:Port                            Peer Address:Port
	0      0                            192.168.23.150:ssh                            10.228.155.38:49631    timer:(keepalive,87min,0)

把协议换成`http`：  

	[root@localhost nan]# ss -o state established '( dport = :http or sport = :http )'
	Recv-Q Send-Q                        Local Address:Port                            Peer Address:Port
	

技巧出处：[https://twitter.com/nixcraft/status/272857310689366016](https://twitter.com/nixcraft/status/272857310689366016)。