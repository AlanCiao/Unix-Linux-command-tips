#显示文本文件内容的行号
使用`cat -n /file`命令可以显示文本文件内容的行号：  
举个例子：  

    [root@localhost command]# cat -n ./mem1.log
     1               total       used       free     shared    buffers     cached
     2  Mem:         32062       9922      22140          0        906       3451
     3  -/+ buffers/cache:       5563      26498
     4  Swap:        31999       9313      22686


技巧出处：[https://twitter.com/nixcraft/status/188694159203373056](https://twitter.com/nixcraft/status/188694159203373056)。