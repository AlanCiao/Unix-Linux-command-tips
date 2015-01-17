#ls命令按文件size大小列举文件
使用“`ls -l -S *.d`”命令按文件`size`从大到小列举文件，而“`ls -l -S *.d | sort -k 5 -n`”按文件`size`从小到大列举文件：  
举个例子：  

    Nans-MacBook-Pro:Proc nanxiao$ ls -l -S *.d
    -rwxr-xr-x@ 1 nanxiao  staff  4988 Dec  7 11:51 crash.d
    -rwxr-xr-x@ 1 nanxiao  staff  3067 Dec  7 11:51 shortlived.d
    -rwxr-xr-x@ 1 nanxiao  staff  2491 Dec  7 11:51 rwbytype.d
    -rwxr-xr-x@ 1 nanxiao  staff  2452 Dec  7 11:51 pathopens.d
    -rwxr-xr-x@ 1 nanxiao  staff  2263 Dec  7 11:51 stacksize.d
    -rwxr-xr-x@ 1 nanxiao  staff  1684 Dec  7 11:51 kill.d
    -rwxr-xr-x@ 1 nanxiao  staff  1656 Dec  7 11:51 sigdist.d
    -rwxr-xr-x@ 1 nanxiao  staff  1651 Dec  7 11:51 threaded.d
    -rwxr-xr-x@ 1 nanxiao  staff  1583 Dec  7 11:51 mmapfiles.d
    -rwxr-xr-x@ 1 nanxiao  staff  1502 Dec  7 11:51 rwbbypid.d
    -rwxr-xr-x@ 1 nanxiao  staff  1494 Dec  7 11:51 rwbypid.d
    -rwxr-xr-x@ 1 nanxiao  staff  1476 Dec  7 11:51 sysbypid.d
    -rwxr-xr-x@ 1 nanxiao  staff  1331 Dec  7 11:51 pidpersec.d
    -rwxr-xr-x@ 1 nanxiao  staff  1331 Dec  7 11:51 syscallbypid.d
    -rwxr-xr-x@ 1 nanxiao  staff   283 Dec  7 11:51 filebyproc.d
    -rwxr-xr-x@ 1 nanxiao  staff   281 Dec  7 11:51 creatbyproc.d
    -rwxr-xr-x@ 1 nanxiao  staff   268 Dec  7 11:51 writedist.d
    -rwxr-xr-x@ 1 nanxiao  staff   267 Dec  7 11:51 newproc.d
    -rwxr-xr-x@ 1 nanxiao  staff   267 Dec  7 11:51 syscallbyproc.d
    -rwxr-xr-x@ 1 nanxiao  staff   264 Dec  7 11:51 readdist.d
    -rwxr-xr-x@ 1 nanxiao  staff   259 Dec  7 11:51 writebytes.d
    -rwxr-xr-x@ 1 nanxiao  staff   255 Dec  7 11:51 readbytes.d

    Nans-MacBook-Pro:Proc nanxiao$ ls -l -S *.d | sort -k 5 -n
    -rwxr-xr-x@ 1 nanxiao  staff   255 Dec  7 11:51 readbytes.d
    -rwxr-xr-x@ 1 nanxiao  staff   259 Dec  7 11:51 writebytes.d
    -rwxr-xr-x@ 1 nanxiao  staff   264 Dec  7 11:51 readdist.d
    -rwxr-xr-x@ 1 nanxiao  staff   267 Dec  7 11:51 newproc.d
    -rwxr-xr-x@ 1 nanxiao  staff   267 Dec  7 11:51 syscallbyproc.d
    -rwxr-xr-x@ 1 nanxiao  staff   268 Dec  7 11:51 writedist.d
    -rwxr-xr-x@ 1 nanxiao  staff   281 Dec  7 11:51 creatbyproc.d
    -rwxr-xr-x@ 1 nanxiao  staff   283 Dec  7 11:51 filebyproc.d
    -rwxr-xr-x@ 1 nanxiao  staff  1331 Dec  7 11:51 pidpersec.d
    -rwxr-xr-x@ 1 nanxiao  staff  1331 Dec  7 11:51 syscallbypid.d
    -rwxr-xr-x@ 1 nanxiao  staff  1476 Dec  7 11:51 sysbypid.d
    -rwxr-xr-x@ 1 nanxiao  staff  1494 Dec  7 11:51 rwbypid.d
    -rwxr-xr-x@ 1 nanxiao  staff  1502 Dec  7 11:51 rwbbypid.d
    -rwxr-xr-x@ 1 nanxiao  staff  1583 Dec  7 11:51 mmapfiles.d
    -rwxr-xr-x@ 1 nanxiao  staff  1651 Dec  7 11:51 threaded.d
    -rwxr-xr-x@ 1 nanxiao  staff  1656 Dec  7 11:51 sigdist.d
    -rwxr-xr-x@ 1 nanxiao  staff  1684 Dec  7 11:51 kill.d
    -rwxr-xr-x@ 1 nanxiao  staff  2263 Dec  7 11:51 stacksize.d
    -rwxr-xr-x@ 1 nanxiao  staff  2452 Dec  7 11:51 pathopens.d
    -rwxr-xr-x@ 1 nanxiao  staff  2491 Dec  7 11:51 rwbytype.d
    -rwxr-xr-x@ 1 nanxiao  staff  3067 Dec  7 11:51 shortlived.d
    -rwxr-xr-x@ 1 nanxiao  staff  4988 Dec  7 11:51 crash.d

技巧出处：[https://twitter.com/nixcraft/status/290535134485176321](https://twitter.com/nixcraft/status/290535134485176321)。