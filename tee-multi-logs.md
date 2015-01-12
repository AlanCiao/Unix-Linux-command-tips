#把命令输出到多个日志文件
可以使用`tee`命令把命令输出到多个日志文件：  
举个例子：  

    [root@localhost command]# free -m | tee mem1.log mem2.log
             total       used       free     shared    buffers     cached
	Mem:         32062       9922      22140          0        906       3451
	-/+ buffers/cache:       5563      26498
	Swap:        31999       9313      22686
	[root@localhost command]# ls
	mem1.log  mem2.log
	[root@localhost command]# ls -alt
	total 16
	drwxr-xr-x  2 root root 4096 Jan 12 10:48 .
	-rw-r--r--  1 root root  230 Jan 12 10:48 mem1.log
	-rw-r--r--  1 root root  230 Jan 12 10:48 mem2.log
	drwxrwxrwx 15 root root 4096 Jan 12 10:47 ..
	[root@localhost command]# cat mem1.log
	             total       used       free     shared    buffers     cached
	Mem:         32062       9922      22140          0        906       3451
	-/+ buffers/cache:       5563      26498
	Swap:        31999       9313      22686
	[root@localhost command]# cat mem2.log
	             total       used       free     shared    buffers     cached
	Mem:         32062       9922      22140          0        906       3451
	-/+ buffers/cache:       5563      26498
	Swap:        31999       9313      22686

可以看到，`mem1.log`和`mem2.log`文件都保存了日志。  
技巧出处：[https://twitter.com/nixcraft/status/163974717311692801](https://twitter.com/nixcraft/status/163974717311692801)。