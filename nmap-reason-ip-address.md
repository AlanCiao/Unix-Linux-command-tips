#显示端口的状态及原因
使用“`nmap --reason ip-address`”命令可以显示当前`IP`地址上端口的状态及原因。  
举个例子：  

    [root@localhost nan]# nmap --reason 192.168.23.150

	Starting Nmap 6.46 ( http://nmap.org ) at 2015-01-13 15:17 CST
	Nmap scan report for localhost.localdomain (192.168.23.150)
	Host is up, received localhost-response (0.0000030s latency).
	Not shown: 995 closed ports
	Reason: 995 resets
	PORT     STATE SERVICE REASON
	22/tcp   open  ssh     syn-ack
	23/tcp   open  telnet  syn-ack
	111/tcp  open  rpcbind syn-ack
	3306/tcp open  mysql   syn-ack
	6699/tcp open  napster syn-ack
	
	Nmap done: 1 IP address (1 host up) scanned in 0.09 seconds

技巧出处：[https://twitter.com/nixcraft/status/272866836545163264](https://twitter.com/nixcraft/status/272866836545163264)。