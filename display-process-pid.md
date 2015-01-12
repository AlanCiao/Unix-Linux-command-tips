#显示运行进程的PID
在`Bash`中定义如下函数（函数参数为程序名）：  

    findpid() { ps axc|awk "{if (\$5==\"$1\") print \$1}"; }
执行效果：  

    [root@localhost ~]# findpid() { ps axc|awk "{if (\$5==\"$1\") print \$1}"; }
    [root@localhost ~]# findpid tail
    16049
    25206
    40701
    48132
技巧出处：[https://twitter.com/nixcraft/status/158835574508240896](https://twitter.com/nixcraft/status/158835574508240896)。
