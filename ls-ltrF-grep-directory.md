#`ls`命令只显示目录
使用“`ls -ltrF --color | grep ^d`”命令可以只显示一个文件夹下面的目录。  
举个例子：  

    [root@localhost nan]# ls -ltrF --color | grep ^d
	drwxr-xr-x  8 1000 1000      4096 Jun 16  2014 x86_64-gdcproject-linux-gnu/
	drwxr-xr-x  8 1000 1000      4096 Oct 16 13:31 bashdb-4.1-0.5/
	drwxrwxr-x 20 1000 1000      4096 Nov 26 14:37 unixODBC-2.3.2/
	drwxrwxr-x 14 1000 1000      4096 Dec 10 09:32 expat-2.1.0/
	drwxr-xr-x 14 root root      4096 Dec 11 09:42 cmake-3.0.2/
	drwxr-xr-x  8 root root      4096 Dec 11 09:43 build_sysdig/
	drwxrwxr-x  6 root root      4096 Dec 16 16:18 redis-2.8.19/
	drwxr-xr-x  2 root root      4096 Dec 23 17:48 odbc_test/
	drwxr-xr-x 15 root root      4096 Dec 24 14:22 gdb-7.8.1/
	drwxr-xr-x 11 root root      4096 Dec 24 14:23 build_gdb/
	drwxr-xr-x  4 root root      4096 Jan  8 10:59 hiredis-master/
	drwxr-xr-x  2 root root      4096 Jan 13 10:25 command/


技巧出处：[https://twitter.com/nixcraft/status/257437865515044866](https://twitter.com/nixcraft/status/257437865515044866)。