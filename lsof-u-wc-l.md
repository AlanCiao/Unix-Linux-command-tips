#计算每个用户打开的文件数
使用“`lsof -u user | wc -l`”命令可以显示`user`用户打开的文件数。  
举个例子：  

    [root@localhost nan]# lsof -u root | wc -l
	5293
显示`root`用户打开了`5293`个文件。

技巧出处：[https://twitter.com/nixcraft/status/271973489303502848](https://twitter.com/nixcraft/status/271973489303502848)。