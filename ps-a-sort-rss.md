#显示系统的内存使用
使用“`ps -A --sort -rss -o pid,comm,pmem,rss | less`”命令可以显示系统的内存使用。  
举个例子：  

    [root@home]$ ls -l -S *.d
     PID COMMAND         ％MEM  RSS
    1386 abrtd           0.1   4824
    1223 hald            0.0   3888
    1423 login           0.0   3420
    ......
可以看到打印了每个进程占用的内存百分比，以及`RSS`的大小。  
技巧出处：[https://twitter.com/nixcraft/status/288158831551332353](https://twitter.com/nixcraft/status/288158831551332353)。