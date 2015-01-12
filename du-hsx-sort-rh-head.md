#打印当前目录下占磁盘空间最多的文件
使用“`du -hsx * | sort -rh | head -n`”命令可以打印当前目录下占磁盘空间最多的`n`个文件：  
举个例子：  

    [root@localhost include]# du -hsx * | sort -rh | head -5
	63M     boost
	7.3M    c++
	5.9M    Qt
	4.3M    QtGui
	3.7M    pgsql

打印了占磁盘空间最多的`5`个文件（包含目录）。  

技巧出处：[https://twitter.com/nixcraft/status/201955934283632640](https://twitter.com/nixcraft/status/201955934283632640)。