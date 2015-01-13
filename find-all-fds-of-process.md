#打印进程打开的文件数目
使用“`for p in $(pidof process); do echo "PID # $p has $(lsof -n -a -p $p|wc -l) fd opened."; done`”命令打印`process`进程打开的文件数目。    
举个例子：  

    [root@localhost /]# for p in $(pidof java); do echo "PID # $p has $(lsof -n -a -p $p|wc -l) fd opened."; done
	PID # 37747 has 139 fd opened.
	PID # 30279 has 117 fd opened.
	PID # 28033 has 204 fd opened.
	PID # 10501 has 211 fd opened.
	PID # 4998 has 442 fd opened.
显示了所有`java`进程打开的文件数目。  
技巧出处：[https://twitter.com/nixcraft/status/281010856706334720](https://twitter.com/nixcraft/status/281010856706334720)。