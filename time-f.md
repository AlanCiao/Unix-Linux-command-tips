#度量执行一个命令花费的时间等参数
使用“`/usr/bin/time -f 'rss=%Mk etime=%E user=%U sys=%S in=%I out=%O' command`”命令可以度量执行一个命令花费的时间，占用的内存，文件I/O等参数.  
举个例子：  

    [root@localhost command]# /usr/bin/time -f 'rss=%Mk etime=%E user=%U sys=%S in=%I out=%O'  find /
	/data1/sun/tomcat7/webapps/metronic_v1.5.4/admin/resources/glyphicons_pro/glyphicons_pro/glyphicons/png/glyphicons_157_show_thumbnails_with_lines@2x.png
	/data1/sun/tomcat7/webapps/metronic_v1.5.4/admin/resources/glyphicons_pro/glyphicons_pro/glyphicons/png/glyphicons_143_database_ban@2x.png
	.....
	rss=5440k etime=0:03.13 user=0.03 sys=0.08 in=0 out=0
可以看到最后会打印出执行“`find /`”命令占用的内存，花费的时间等值：  

	rss=5440k etime=0:03.13 user=0.03 sys=0.08 in=0 out=0

技巧出处：[https://twitter.com/nixcraft/status/235491209743831040](https://twitter.com/nixcraft/status/235491209743831040)。