#按目录size大小列举目录
使用“`du --block-size=kB | sort -n`”或“`du --block-size=kB | sort -nr`”命令可以按目录`size`从小到大或从大到小列举目录。  
举个例子：  

    [root@localhost /]$ du --block-size=kB | sort -n
     0kB    ./dev/bsg
     0kB    ./dev/bus
    ......
    [root@localhost /]$ du --block-size=kB | sort -nr
     1179418kB    .
     937862kB    ./usr
    ......

技巧出处：[https://twitter.com/nixcraft/status/290924082088775681](https://twitter.com/nixcraft/status/290924082088775681)。