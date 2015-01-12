#Linux上kill占用某端口的进程
在`Linux`平台上`kill`占用某端口进程命令：  

    fuser -k port/tcp(udp)
举个例子：  

    [root@localhost redis-2.8.19]# ps -ef | grep redis
    root     10049 35207  0 17:33 pts/7    00:00:00 ./src/redis-server *:6379
    root     10116 35207  0 17:33 pts/7    00:00:00 grep redis             
    [root@localhost redis-2.8.19]# fuser -k 6379/tcp
    6379/tcp:            10049
    [1]+  Killed                  ./src/redis-server
可以看到，占用`6379`端口的进程被杀死了。  
技巧出处：[https://twitter.com/nixcraft/status/162914646125330432](https://twitter.com/nixcraft/status/162914646125330432)。