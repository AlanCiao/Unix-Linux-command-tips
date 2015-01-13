#根据文件修改时间查找文件
使用“`find folder -type f -ctime -n -print`”命令可以显示`folder`文件夹下最近`n`天修改过的文件。  
举个例子：  

    [root@localhost nan]# find /etc -type f -ctime -5 -print
	/etc/adjtime
	/etc/prelink.cache
也可以显示详细信息：  

	[root@localhost nan]# find /etc -type f -ctime -5 -exec ls -l {} \;
	-rw-r--r--. 1 root root 45 Jan 13 14:09 /etc/adjtime
	-rw-r--r-- 1 root root 646080 Jan 10 03:27 /etc/prelink.cache

技巧出处：[https://twitter.com/nixcraft/status/269719613720391682](https://twitter.com/nixcraft/status/269719613720391682)。